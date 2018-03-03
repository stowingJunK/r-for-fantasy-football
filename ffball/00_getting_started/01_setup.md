# Getting Started
https://www.r-project.org/


## Installing R
R is available on most computers running Linux, Mac OS X, or Windows. According to their website, the Comprehensive R Archive Network (CRAN) "is a network of ftp and web servers around the world that store identical, up-to-date, versions of code and documentations for R". In essence, CRAN directs you to the most reliable places to download the most recent versions of R. The current release is R 3.4.3 as of November 30, 2017, of which will be compatible with the content of this repository. Click the link below, navigate to the download page for your operating system, and follow the instructions for installing the R, which contains the basic necessities of writing and running R code.

* [The Comprehensive R Archive Network](https://cran.r-project.org/ "CRAN Homepage")

The screenshots on this page were captured on the Windows version of R, but can also be referenced for R installed on other operating systems.

## R Console
There are several methods to write and run code after having installed and located R. The most vanilla way of processing code is by using the command line.

![cmd_line]

In the above, I compute the sum of 2+2. 

## R GUI
Similarly you can access the R console within the R GUI, which comes packaged with your download.

![gui]

In addition to a different theme, the GUI also allows you to create, write, save, and source script files.

![script]

Writing your R code in a script rather than in the console allows you to save your work and run your computations in the future. Code entered in the console is lost after closing the window.


## R Studio
While the R GUI is the bare minimum for writing lasting code, I personally prefer the added features within R Studio, a commercially sold integrated development environment (IDE) for R. Luckily, the open source version of R Studio is free for home usage. You can download R Studio here:

* [R Studio](https://www.rstudio.com/products/rstudio/download/ "R Studio Download")

If you've used anything like Anacadona for developing Python code or MATLAB, you will be familiar with this interface. R Studio not only has a sleeker feel, but, at a glance, there are also windows for monitoring variables, file directories, and plots. You can also write R Markdown files and publish reports that integrate computer language (R code) with human-readable language (i.e. English), which will be covered in a later section.

![rstudio]

Congratulations! You now have the basic tools for writing your first lines of R code. In the next section, [the Basics](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_the_basics/01_introduction.md), I begin to cover the basic building blocks and synthax required to write the most basic R code.

[cmd_line]: https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/00_getting_started/r_cmd_line.PNG "R Command Line"
[gui]: https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/00_getting_started/r_gui.PNG "R Gui"
[script]: https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/00_getting_started/r_gui_new_script.PNG "R Gui New Script"
[rstudio]: https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/00_getting_started/r_studio.PNG "R Studio"
