# Get started

# Registering

*(Time: approx 30 minutes)*

- [ ]  Get a W&M research computing account! [https://www.wm.edu/offices/it/services/researchcomputing/acctreq/](https://www.wm.edu/offices/it/services/researchcomputing/acctreq/)
- [ ]  Register for Google Earth Engine - [register without a cloud project](https://code.earthengine.google.com/register)
- [ ]  [Register for a Planet Labs education account](https://www.planet.com/markets/education-and-research/#apply-now) (I should be able to hook you up with my grant eventually but start here)
- [ ]  [Create a GitHub account](https://github.com/join) if you don’t have one

# Get the PyCoGSS repo into W&M’s JupyterHub

*(Time: approx 15 minutes)*

- [ ]  Fork the [getting-started](https://github.com/pycogss/getting-started) repo from GitHub
- [ ]  log in to W&M’s JupyterHub [https://jupyterhub.wm.edu/](https://jupyterhub.wm.edu/). Click “Start My Server”, and choose Default Notebook.
- [ ]  Under “Other” navigate to “Terminal.”
- [ ]  Clone the repo using `git clone https://github.com/[YOUR USERNAME]/pycogss/getting-started.git`
- [ ]  Navigate to the newly downloaded `pycogss-getting-started`directory

# Complete warmup notebooks 1 and 2

Complete mini-assignments in the notebooks. Ask Joanmarie for assistance. When you’re done, let Joanmarie know. 

*Notebook 1 approximate time: 2 hours?*

*Notebook 2 approximate time: 6 hours?*

---

Now let’s play on the real computers!

# Use VS Code to access HPC

Detailed borrowed from [NCEAS’s Scalable and Reproducible Approaches to Arctic Research course](https://learning.nceas.ucsb.edu/2023-03-arctic/#setting-up) (an excellent resource!)

1. First, [download VS Code](https://code.visualstudio.com/) if you do not already have it installed. You’ll also need to download the [Remote - SSH extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack).
2. To connect to the server using VS Code follow these steps, from the VS Code window, open the command pallette (Cmd + Shift + P).
3. Enter “Remote SSH: Connect to Host”

![Untitled](Get%20started%20dbce70ea6ce04c2798e3e8da7cce5205/Untitled.png)

1. select “Add New Host”
2. enter the ssh command to connect to the host:

```python
ssh [wm_username]@astral.sciclone.wm.edu
```

For example, you can do `ssh jdelvecchio01@astral.sciclone.wm.edu` if you’re me. You’ll only have to do this step once.

1. Select the SSH config file to update with the name of the host. You should select the one in your user directory (eg: `/Users/jclark/.ssh/config`)
2. Click “Connect” in the popup in the lower right hand corner
    - Note: If the dialog box does not appear, reopen the command palette (Control+ Shift + P), type in “Remote-SSH: Connect to Host…”, choose e.g. astral.sciclone.wm.edu from the options of configured SSH hosts, then enter your password into the dialog box that appears
3. Enter your password in the dialog box that pops up at the top of the screen. When you are connected, you will see in the lower left hand corner of the window a green bar that says “SSH: astral.sciclone.wm.edu.”

![Untitled](Get%20started%20dbce70ea6ce04c2798e3e8da7cce5205/Untitled%201.png)

After connecting to the server, in the extensions pane (View > Extensions) search for, and install, (1) Python, (2) Jupyter, and (3) Jupyter Keymap (note that these extensions will be installed on the server, and not locally)

If you ever have an issue finding your Python interpreter within your environment, you might have to add it manually:

1. in VS Code bring up the palette by Ctrl+Shift+P
2. Search “Python: Select Interpreter”
3. Click “Enter interpreter path” and then “Find” to go to your directories
4. From here navigate to .*conda* and then *envs*, where you will find a folder for the environment you want to use
5. Within this environment directory go to *bin* and then scroll down until you find python.11 or whatever the latest version of Python that environment has. Select that. it should work now!

# Make a symbolic connection to the `watersheds` directory

This is where we should dump all our data!! 

In the Terminal (open in VS Code by Ctrl + ` ), enter:

```python
ln -s /sciclone/data10/watersheds watersheds
```

Now in your “Explorer” on the left side in VS Code, you should see a directory called “watersheds.” You can now bring files in and out of this space manually. You can also always point a download or saved file to `/sciclone/data/watersheds`with, for example:

```python
df.to_csv('/sciclone/data10/watersheds/example.csv')
```

And you should make directories there too:

```python
aoi_path = Path('/sciclone/data10/watersheds', str(aoi_name))
```

# Set up conda environments on HPC

1. Add two lines to your `.bashrc` file:

```bash
source "/usr/local/anaconda3-2021.05/etc/profile.d/conda.csh"

module load anaconda3
```

1. Open a new terminal (Control + ` on Windows and then the “+” symbol on the terminal tray). Despite adding the line to the `bashrc` file (which means “run this script every time I log on to the terminal), It doesn’t seem to like `module load anaconda3` and I don’t know why. You have to do that in the terminal, I guess. So type `module load anaconda3.`  If no error message emerges, you’re good!

1. Create a test conda environment (And write `y` any time you have to install):

```python
conda create -n test python=3.12
```

1. Activate that test environment with `conda activate test`. `(test)` should now appear in front of the name of the computer you’re on.

# Build a conda environment to do research with Earth Engine

1. Use the following lines to build a conda environment called `gee` which will have all the useful modules

```python
conda create -n gee python=3.12
conda activate gee
conda install -c conda-forge geemap ipyleaflet geedim numpy geopandas rioxarray
conda install conda-forge::gdal
```

# Run the `aoi-2-data` notebook

1. Fork the PyCoGSS recipes repo at https://github.com/pycogss/pycogss_recipes.git
2. While on the HPC cluster via VS Code, activate a conda environment with `git`, clone your fork to your workspace, and then navigate to the `aoi-2-data` directory
3. Load up the notebook in the directory and execute all the `import` lines to ensure your environment has all the necessary modules
4. At the `ee.Authenticate()` step, you’ll have to open up a browser window with a Chrome profile that has been registered for Earth Engine. You might have to do stuff with making a cloud project. Hopefully it doesn’t yell at you in this step (it didn’t for me but I didn’t take screen shots when I was doing it so I can’t show you what mine looked like. I think i made a “dummy” cloud project essentially). If you’re good to go you will get a long hash key to copy and paste into the box at the top of VS Code (like how you enter your password). Hit “Enter” on that, and you should successfully authenticate.  
5. Modify the `HYBAS_ID` of the watershed of your choosing 
6. Make sure you are saving to `/sciclone/data10/watersheds`

# Some extra links - Local install

This is really for Joanmarie who was installing VS Code to run locally on Windows. 

[https://onezero.blog/how-to-set-up-python-and-visual-studio-code-ide-for-data-science/](https://onezero.blog/how-to-set-up-python-and-visual-studio-code-ide-for-data-science/)

[https://stackoverflow.com/questions/66869413/visual-studio-code-does-not-detect-virtual-environments](https://stackoverflow.com/questions/66869413/visual-studio-code-does-not-detect-virtual-environments)