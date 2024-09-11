# Week 4 instructions

## Pre-assignment 1: choose a dataset
This can be anything*! I recommend using a dataset you collected or are working with for research or a class project. If you need inspiration I can give you any number of cool surface processes datasets! 

(*)Well, ok, not anything - the only requirement is a dataset that contains at least one column of numerical data (better if it's two, see below). This activity will be more fun and intuitive if it is a ["wide"](https://en.wikipedia.org/wiki/Wide_and_narrow_data) dataset, and the wider the better!

## Pre-assignment 2: get inspired with an example
I have included an example of my attempt at re-creating a [figure](https://github.com/jmdelvecchio/geol437-fa24/blob/main/0923/Richardson_et_al_Fig2.png) from a publication using [data](https://github.com/jmdelvecchio/geol437-fa24/blob/main/0923/2019149_TableDR1.csv) supplied in the supplement (which is sometimes very difficult or impossible if the authors are bad at sharing their data; more on that later) with `richardson.ipynb`. You can see that, though it takes a little time and coding, you can (1) load data, (2) "clean" it (eliminate errant symbols and correct data types), and (3) plot it nicely just like in the paper! 

## Deliverable for Week 4

You will be responsible for creating an <b>informative</b> and <b>publication-worthy</b> plot of a dataset special to you. Your steps are to:
1. load a dataset that contains at least one column of numerical data from a `.csv` or `.txt` file into `pandas` (or, if you are feeling adventurous, use data from an online repository and download from the URL)
2. perform any data "cleaning" (convert strings to numbers, replace symbols or weird numbers with `np.nan`, etc.) using scripting*
3. perform at least one calculation on at least one column of numerical data (e.g. bare minimum is converting temperatures in F to C)
4. use `matplotlib` and/or `pandas` built-in plotting to make a plot where data are displayed on not just the x and y axes but an additional data layer in the form of symbol color (`c` axis), size, shape, etc. My hint for you here is to use a dataset with at least two numerical columns such that a scatterplot of the primary relationship is made with a secondary relationship acting as the `c` axis. 

Please turn in a <b>zipped folder</b> containing <b>both</b> the dataset and the `.ipynb` file used to create your figure (unless using a URL). 

(*)I challenge you to do as much as possible with code instead of "by hand" in Excel etc., but I understand if it's easier to clean your data in Excel when you are just learning. I trust you to make the call that's right for you!