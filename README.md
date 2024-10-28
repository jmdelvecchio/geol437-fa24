# GEOL 437 - Computers and Geology 

<b>Instructor</b>: Dr. Joanmarie Del Vecchio

<b>Location</b>: McGlothlin-Street Hall 219

<b>Meeting times</b>: Mondays 5:00-6:50pm 

<b>Office Hours</b>: Mondays 4-5pm or [by appointment](https://outlook-sdf.office.com/bookwithme/user/c70b4576f7544299af54ec9b68670b62@wm.edu/meetingtype/f4v96J1x9E-Jp4VOFoVCwQ2?bookingcode=48efa718-3b3f-481a-ba01-343b80a738c7&anonymous&ep=mlink)

# Class format

To take advantage of hands-on coding with peers and a mentor, this class will be run largely as a <i>flipped classroom</i>. Instructional material will be made available ahead of time in the form of tutorial Jupyter Notebooks and/or recorded lectures with screen captures. You will be expected to come to class having completed any pre-meeting assignments, which will review or teach new skills to be implemented or improved upon during the class meeting. 
At William and Mary, each credit hour of face-to-face instruction [requires a student work two hours out of class student work](https://www.wm.edu/offices/ce/policies/academic-affairs-student-life/academic-credit-hour.php). This means that for this two credit-hour class, you should be spending <b>four hours</b> a week on pre-meeting activities and wrapping up in-class assignments. 

# Learning objectives

The primary goal for students for this course is to learn to <b>think algorithmically</b>. But what does that mean? I'd break it down as follows:

1. <b>Learn</b> coding (and specifically Python) tools for common scientific tasks and <b>identify</b> appropriate uses for these tools  

2. <b>Break down</b> complex scientific tasks (e.g. collecting and organizing data, apply a transformation to a dataset, synthesize results) into a logical flow of calculations or data manipulations using code

3. <b>Implement</b> functions and methods that transform data for scientific tasks by understanding inputs and outputs for these algorithms 

4. <b>Create</b> original analyses and/or data visualizations from "real world" data, either from student research or a topic of interest
# Grading

Let's begin by saying that this class is intended to help you build useful and transferrable skills for research and industry - therefore <b>you will get out of this class what you put into it!</b> It's also a 400 level class, so you are expected to know how to manage your time and deadlines (but be in touch if you'd like to talk strategies). Therefore grading will be relatively simple:
* 60% of your grade will come from completing weekly tutorial material. These will be graded on a scale of (2) satisfactory, (1) unsatisfactory, and (0) missing. You will depart class Monday evening with a head start from your in-class work and instructions on what is "satisfactory," and you will have until 5pm the next Monday to turn in the assignment. Because you will work on the assignment in class, <b>late assignments will not be accepted</b>, but I will <b>drop your two lowest assignment grades</b> this semester.
* 40% of your grade will come from a capstone project in which you generate publication-worthy analyses and figures for a dataset or system close to your heart 

# Class schedule
10/14/2024 - see changes below!

This schedule is <b>highly</b> subject to change based on class interest - I picked these topics, but if I sense we need more time on something or want to go in a totally different direction, we might! 

| Date   |      Topic      |  Pre-assignment |
|:----------:|:-------------:|:------:|
| 9/02/2024 |  No class - Labor Day|[Account registration](https://github.com/jmdelvecchio/geol437-fa24/tree/main/0902)|
| 9/09/2024 |Python, `numpy`, and `matplotlib` basics|[Week 2 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/0909)|
| 9/16/2024 |`pandas`, your Excel alternative|[Week 3 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/0916)|
| 9/23/2024* |`pandas` and plotting practice|[Week 4 example and instructions](https://github.com/jmdelvecchio/geol437-fa24/tree/main/0923)|
| 9/30/2024 |Conditionals and iterating|[Week 5 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/0930)|
| 10/07/2024 |Geospatial data - vector and raster data|[Week 6 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/1007)|
| 10/14/2024 |Geospatial data II|[Week 6 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/1007)|
| 10/21/2024 |Photogrammetry|[Week 7 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/1014)|
| 10/28/2024 |Statistics and plotting - `scikit-learn` and `seaborn`|[Week 8 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/1028)|
| 11/04/2024 |Numerical solutions - forward model|[Week 9 activities](https://github.com/jmdelvecchio/geol437-fa24/tree/main/1104)|
| 11/11/2024 |HPC intro and project work time||
| 11/18/2024*|Project work time||
| 11/25/2024 |Image segmentation / classification||
| 12/02/2024 |Project lightning talks||

(*)Denotes dates where Joanmarie will be out of town - you are encouraged to gather as a class and work through assignments

Each week will have a corresponding folder in the GitHub repo - this will be where your assignments and instructions will live (each week will have its own `README.md`)

# Honor code etc
The university prides itself on creating the nation’s first Honor Code. The Code provides an environment in which trust can thrive and a level playing field for students, ensuring students are evaluated based on their own effort and ability and in which students can be taken at their word. The Code reflects the university’s value of integrity—in our words and our deeds. As an instructor, I strive to provide an environment that promotes integrity. Reasonable measures taken to protect us from temptation are not antithetical to the Honor Code; thus, I reserve the option to proctor exams, provide multiple copies of exams for distribution, and restrict the technology tools students can possess while taking exams. I support the Honor Code and am obligated to report concerns for review and resolution by the Honor Council. As it is your obligation to resolve any perceived lack of understanding of my expectations in advance of submitting any work, I encourage you to contact me with any questions about my course and testing policies. You also are welcome to contact me if you have concerns that any fellow students are not fulfilling their obligation to uphold the Honor Code. All work submitted in this course, whether in draft or final form, must be your own and must be cited appropriately.

Now for the course-specific material:

## Unauthorized Aid/Collaboration
Rarely do geoscientists or data scientists code alone (or entirely from memory or the official docs), and I want to acknowledge that by <i>permitting and even encouraging a certain level of collaboration on assignments</i>. Here's a spectrum:
- I <b>fully endorse</b> asking a classmate for assistance in understanding an error message and how to resolve it. 
- I <b>encourage</b> you to share tips and tricks about skills like plot formatting, efficient list comprehension, helpful functions, with the caveat that <b>you will not simply copy and paste from each other</b> but rather help each other fully embrace the power of computational methods. 
- I will <b>insist</b> that you first consult Google and related resources (StackExchange, StackOverflow, etc) before turning to a classmate or myself when you are stuck. If you use a code snippet from one of the above websites, <b>add the URL as a comment in your code</b>. 
- I <b>do not permit</b> the use of generative AI without express permission from Joanmarie, which includes a discussion and understanding of the benefits and drawbacks to using ChatGPT's coding skills (tl;dr: it definitely steals from repos without permission and is sometimes wrong, but maybe you are truly a 1 in 1,000 instance where truly no one else has asked your question on StackExchange). <b>I will consider mindless copy-and-paste from ChatGPT plagiarism</b>. 99% of what we are doing in this class can be troubleshooted with Google. 

## Plagiarism
Plagiarism is “the presentation, with intent to deceive, or with disregard for proper scholarly procedures of a  ignificant scope, of any information, ideas or phrasing of
another as if they were one’s own without giving appropriate credit to the original source.” (<i>the faculty resource that lists this definition does not, in fact, cite this definition...</i>). See above, and know that I can copy and paste your code to search for where you may have lifted it from, so please don't do that. 

# Community 
The W&M Geology Department welcomes, supports, engages, and celebrates the broad range of backgrounds and experiences in our community. We affirm our individual and collective responsibility for creating and fostering a respectful, cooperative, inclusive, and equitable campus environment for all individuals, regardless of race, ethnicity, nationality, culture, religion, political beliefs, gender, gender identity / expression, sexual orientation, age, disability, or marital, parental, or veteran status.  All people have the right to be addressed and referred to in accordance with their personal identity.  In this class, you will have the chance to indicate the name that you prefer to be called and the pronouns with which you would like to be addressed.

# Student Accessibilty Services
William & Mary accommodates students with disabilities in accordance with federal laws and university policy. Any student who feels they may need an accommodation based on the impact of a learning, psychiatric, physical, or chronic health diagnosis should contact Student Accessibility Services staff at 757-221-2512 or at sas@wm.edu to determine if accommodations are warranted and to obtain an official letter of accommodation. For more information, please see www.wm.edu/sas.

# Mental and Physical Wellbeing
William & Mary recognizes that students juggle different responsibilities and can face challenges that make learning difficult.  There are many resources available at W&M to help students navigate emotional/psychological, physical/medical, material/accessibility concerns, including:
- The W&M Counseling Center at (757) 221-3620.  Services are free and confidential. 
- The W&M Health Center at (757) 221-4386.
- To seek assistance for interpersonal, academic, and wellness challenges, please contact Care Support Services at wm.edu/care (care@wm.edu).
- For a list of other [resources](https://www.wm.edu/offices/wellness/resources/index.php) available to students, see [here](https://nam11.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F18Vl-71Z8AQMgzlWSTJUH5xAm65xS7OQf-BsrGRx-kJQ%2Fedit%3Fusp%3Dsharing&data=05%7C02%7Cjdelvecchio01%40wmedu.mail.onmicrosoft.com%7Cee2d7e702add43daa63d08dcc20dda1d%7Cb93cbc3e661d40588693a897b924b8d7%7C0%7C0%7C638598611987121814%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=bEdzmpSL4xkrhWvXi9U7Q4U5M2JXW1GGQwaVA8acUPA%3D&reserved=0)
