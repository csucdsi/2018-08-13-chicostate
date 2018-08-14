# Day 1

## Workshop Introduction
* Instructor/helper introductions
* SWC code of conduct
* Sticky note use explanation
* Schedule
* Peer learning environment
        - Hack MD (have our collaborative document open at all times. If they want to make an account they can have a second one open to write notes in)
        - Full notes will be available after the workshop(?)


## Data Organization in Spreadsheets (RO)
**link to instructor notes**
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

#### [01 Intro to R and R Studio(RO)](https://u2ng.github.io/swc-r-notes/01-intro-r-rstudio.html) (45+10)
* R/Rstudio setup
* Download gapminder data  [Link](https://raw.githubusercontent.com/resbaz/r-novice-gapminder-files/master/data/gapminder-FiveYearData.csv)
* Intro to rstudio
* Intro to basic R functions (math, comparisons, variable assignments, simple vectors, manage environment, installing packages, creating new project)

#### [15 Producing Reports with knitr](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/15-knitr-markdown/) (60+15 min)
* walk through basic rmarkdown html lesson
* connect markdown script with HackMD
* demo/show others: knit to PDF, _google "rmarkdown gallery"_  website, homework, final chem report
* go back, hide code. eval=false. control size of graphics.


#### [03 Seeking Help](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/03-seeking-help/) (10+10 min)
* Just go through swcarpentry lesson on 2nd screen.
* explain each piece of a help file (read through an easy one, and a complex one)
* Ask for topic to explore using CRAN Task Views
        - If not chosen, show "statistical genetics" and explain what Bioconductor is
* Put "other ports of call" links into HackMD
* Challenge #2 & #3 (copy to Hack MD) **(10 min)**

#### [04 Data Structures](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/04-data-structures-part1/) (40+15 min)
* provide cats data in hack md for copy/paste
* write up (and draw) each data type on the whiteboard
* file-> new file -> text file. Save as `data/feline-data.csv`
* Challenge 1:4, 7(copy to Hack MD) **(15 min)**

#### [05 Exploring Data Frames](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/05-data-structures-part2/) (20+10 min)
* gapminder forward. No cats
* read in using read.csv and provide the file, AND provide the url directly.

#### [09 Vectorization](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/09-vectorization/) (10+15)
* element wise opearations
* challenge #1
* comparison, logical, functions (compare log to mean)

#### [10 Functions Explained](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/10-functions/) (15? min)
* what's a function: https://norcalbiostat.github.io/MATH130/04_functions_recode.html
* ask them what to put to remove NA's from data prior to mean
* defining user written functions
* challenge #1 depending on audience interest & time

----

# Day 2

## The Unix Shell (RO)
**link to instructor notes**
[https://github.com/U2NG/swc-shellnotes/blob/master/2016-09-SWC-shell-notes_complete_final.md]
(https://github.com/U2NG/swc-shellnotes/blob/master/2016-09-SWC-shell-notes_complete_final.md)    

* **Introducing the Shell**   
* **Files and directories**    
Challenge - absolute vs relative paths
* **Working with files and directories (creating things)**     
Challenge - renaming files
* **Pipes and filters**    
Challenge - what does ``sort -n`` do?    
Challenge - piping commands together
* **Shells scripts**    
* **Loops** last?    
Challenge - saving a file to a loop part 1   
Challenge - aving a file to a loop part 2
* **Finding things** (usually don't get to this lesson)



## Data Visualization and manipulation with R (RAD)
Setup: Make a `data` folder , and `code` in your workshop folder. Put the gapminder data in `data`. 
* Divergence to functions. Show SWC function code. Emphasize/point that this is power of R is rolling your own functions. 

#### [08 Creating Publication-Quality Graphics with ggplot2](http://swcarpentry.github.io/swc-releases/2016.06/r-novice-gapminder/08-plot-ggplot2/)
* Read objectives
* State 3 main plotting systems (base, lattice, ggplot)
* Open new Rmarkdown file - give it a nice title.
        - Delete template material, keep header and first code chunk
        - Save this code file **into your code folder**
        - read in gapminder data into first code chunk. Start by copying what you did yesterday, but you have to modify the path. "data/gapminder.csv"
        - Show `ls` and `rm` works in R also. 
* Copy to Hack: `ggplot(data = gapminder, aes(x = gdpPercap, y = lifeExp)) + geom_point()`
        - copy this to your RMD file, in a new code chunk. 
        - what was the problem? 
* Load the ggplot2 library by clicking the button. We're doing it this way on purpose for now. 
* Run this code chunk, make the picture, and explain the syntax.
* Knit. Why didn't it work?
        - fix adding libary to code file. 
        - show how to hide messages (customize r code chunks)
* Challenge 1 & 2 - copy question and code to Hack MD
* Layers 
    - To demonstrate how the layers work, let's look at the relationship between the calendar year on the x axis and life expectency on the y. Send to Hack `ggplot(data = _____, aes(x=____, y=____)) + geom_point()` -- fill in the blanks
    - now add lines - not quite what we wanted right? 
    - connect the dots within country by adding `by=country` to the aestetic
    - countries are grouped within continents right? so let's add a `color=continent` aestetic.
    - aestetics inside the main ggplot function apply to all layers. -- move color aestetic to lines only
    - layers are applied in order: swap the ordering of the points and lines. 
  
**Statistical Plots**
Copy to Hack: `ggplot(data = gapminder, aes(x = gdpPercap, y = lifeExp, color=continent)) + geom_point()`
  - add layer `scale_x_log10()`
  - set alpha in points _helper please add these layers to the above plot as we cover them_
  - add lm smoother
  - add another smoothing layer, no method, color=red (purpose, assess linearity)
  - add shape by continent
  - **challenge** Change the size of the points so that they are proportional to the country `pop`. 
     Hint: Use `aes()` inside `geom_point()`


 Guidelines
 * start small! Add one layer at a time.
 * easy to make overly complicated and hard to read graphs. 
 
**Paneling / faceting**
Copy to Hack
```{r}
starts.with <- substr(gapminder$country, start = 1, stop = 1)
az.countries <- gapminder[starts.with %in% c("A", "Z"), ]
ggplot(data = az.countries, aes(x = year, y = lifeExp, color=continent)) +
  geom_line() + facet_wrap( ~ country)`
```

Too many other things to show, explain. 
 
   
**Help resources**
* cookbook for R - graphics section
* R Studio has add-ins https://github.com/calligross/ggthemeassist 
* Intro to R "full data viz tutorial": https://norcalbiostat.github.io/MATH130/full_data_viz_tutorial.html 
* #ggplot2 and #rstats hashtag on twitter

 
        

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

## Creating websites with R Markdown and GitHub (RAD)

1. Make new repo in github. Initalize with a readme
2. Open R Studio
3. Create a new project
    - version control - git
    - Need to provide repo url.
4. Back to Github. Click green clone or download. Copy repo address. Paste into R Studio
    - open in new session
5. Start a new R text file. Copy the following code into this file. Save as `_site.yml`

```
name: "name"
output_dir: "."
navbar:
title: "CLASS TITLE"
left:
    - text: "Schedule"
      icon: fa-database
      href: http://example.com

right:
    - text: "Syllabus"
    icon: fa-info-circle
    href: syllabus.html

output:
    html_document:
    theme: yeti
        highlight: tango  
```

6. Start a new R Markdown file.
    - Give it a title
    - delete template text.
    - Write "hello world"
    - Save as `index.Rmd`

7. Restart R Studio
    - Click the `build` tab in the upper right.
    - Click build website.

You can see the preview in the viewer window, but let's make it live!

8. Git tab - diff
    - `ctrl+A` to select all.
    - check `stage` button
    - commit message "initial site build"
    - commit + push

9. Go back to GitHub
    - Repo settings
    - Github pages - source master - save
    - Scroll back down to GH pages. Click on URL to your live site.

10. Explain
    - what the `_site.yml` file does
    - how to add additional pages
    - file structure limitations
    - options: master vs gh-pages branch vs docs folder
    - output directory: docs (check that this works!)

11. Going further
    - blogdown + Hugo + netlify
    - show Bookdown as well (math 456 notes, from academic website, math 315 final projects html buttons)
