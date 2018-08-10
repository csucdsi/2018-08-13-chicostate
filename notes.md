# Materials
* whiteboard markers (have)
* sticky notes (purchase/find)
* roster (print)
* nametags (purchase)
* guest wifi password (call ITSS morning of)



# Day 1

## Workshop Introduction
* Instructor/helper introductions
* SWC code of conduct
* Sticky note use explanation
* Schedule
* Peer learning environment


## Data Organization in Spreadsheets (RO)
**link to lesson materials**
[https://github.com/U2NG/2018-dc-data-org-notes/blob/master/index.md](https://github.com/U2NG/2018-dc-data-org-notes/blob/master/index.md)
* **Introduction**    
Discussion about using spreadsheets (for what?) and things that were frustrating or sad?    
* Types of spreadsheet programs
* Problems with Spreadsheets
* Using spreadsheets for data entry and cleaning
* **01-Formatting tables**    
Exercise 1 - reformatting data and identifying problems or common mistakes
* **03-Dates as data**    
Exercise 2 - working with date formatting    
Exercise 3 - working with time formats    
Exercise 4 - saving dates as CSV format Problems
* **04-quality control**    
Show data validation GUI function walkthrough   
Exercise 5 - Sorting columns    
Exercise 6 - conditional formatting    
* **05-Exporting**    
Why xlsx is not a good idea and CSV and TSV are recommended    
Save as CSV walkthrough    
Mention R packages that can read xls files e.g. readxl, XLconnect, xlsx etc.   



## Intro to R and Markdown (RAD)

#### [01 Intro to R and R Studio(RO)](https://u2ng.github.io/swc-r-notes/01-intro-r-rstudio.html)
* R/Rstudio setup
* Download gapminder data  [Link](https://raw.githubusercontent.com/resbaz/r-novice-gapminder-files/master/data/gapminder-FiveYearData.csv)
* Intro to rstudio
* Intro to basic R functions (math, comparisons, variable assignments, simple vectors, manage environment, installing packages, creating new project)
#### [03 Seeking Help](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/03-seeking-help/) (10+10 min)
* explain each piece of a help file (read through an easy one, and a complex one)
* Ask for topic to explore using CRAN Task Views
        - If not chosen, show "statistical genetics" and explain what Bioconductor is
* Challenge #2 & #3
#### [04 Data Structures](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/04-data-structures-part1/) (40+15 min)
* provide cats data in hack md for copy/paste
* write up (and draw) each data type on the whiteboard
* file-> new file -> text file. Save as `data/feline-data.csv`
* Challenge 1:4, 7
#### [05 Exploring Data Frames](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/05-data-structures-part2/) (20+10 min)
* gapminder forward. No cats
* read in using read.csv and provide the file, AND provide the url directly.
#### 09 Vectorization
#### 10 Functions Explained
#### 15 Producing Reports with knitr
* walk through basic rmarkdown html lesson
* demo/show others: pdf, slides, homework, website
* go back, hide code.

----

# Day 2

## The Unix Shell (RO)


## Data Visualization and manipulation with R (RAD)

#### 08 Creating Publication-Quality Graphics with ggplot2
#### 13 Dataframe Manipulation with dplyr

----

# Day 3

## Projects and Version Control in R (RO)
Goal: learn terminology (push/pull/repo/clone/commit), and setup a repo, cloned to computer using R projects
[lesson notes link](https://github.com/U2NG/2018-git-notes)
* Overview (ppt slides)
* git config
* git init
* git status, git add, git commit
* git push (remotes 'master' in git)

[RStudio Git Supplement](https://swcarpentry.github.io/git-novice/14-supplemental-rstudio/index.html)
* setup Git in RStudio

## Creating websites with R and Markdown (RAD)
* provide minimum necessary files
* build locally, change/edit, rebuild, commit & push
* turn on gh-pages - see live site

* options: master vs gh-pages branch vs docs folder
    - output directory: docs (check that this works!)
* Going further: blogdown + Hugo + netlify
* show Bookdown as well (math 456 notes, from academic website, math 315 final projects html buttons)
