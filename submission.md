HDAT9700: Assessment 1A - Chapters 2-3
================

### Submission instructions

This is an R Markdown document, an example of *literate programming*
which allows users to interweave text, statistical output and the code
that produces that output.

To complete your assignment:

  - Edit this file directly, interweaving text and R code as appropriate
    to answer the questions below. Remember to `Knit` the file to make
    sure everything is running smoothly. Detailed information on R
    Markdown is available
    [here](https://rmarkdown.rstudio.com/lesson-1.html), and there is a
    useful cheat sheet
    [here](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf).

  - Use Git to `commit` changes you make in this repo locally.

  - `Push` the repo, together with this edited `.Rmd` file, the
    corresponding `.md` file and any other relevant files to GitHub. You
    can check your rendered file in the GitHub repo—this is how it will
    apper for the person grading the assessment (note that the output
    specified at the top of this file is `github_document`. This format
    is designed to be read within GitHub). Please use appropriate code
    chunk options to suppress lengthy or superfluous output.

You should `commit` and `push` as often as necessary\! Your assessment
will only be graded on the most recent version of your repo at the
assessment due date.

Good luck\!

-----

### Overview

In this assignment you are provided with observational data on maternal
characteristics and birth outcomes. Your aim is to estimate the **total
causal effect** of maternal smoking on birth weight.

The data come from [Hosmer and Lemeshow
(2000)](https://books.google.com.au/books?hl=en&lr=&id=64JYAwAAQBAJ&oi=fnd&pg=PR13&dq=Hosmer,+D+and+S.+Lemeshow+\(2000\),+Applied+Logistic+Regression,+Wiley&ots=DtdN7_9plK&sig=aZ7GvUF2VmkhnJsLvg8Cc475Vb4&redir_esc=y#v=onepage&q&f=false)
and include observations on 189 mothers, including information on
smoking history, perinatal health and birth outcomes.

This dataset is shipped with the `COUNT` package in R, so you should
install this at the console first (we won’t use this package, it is just
a quick way to load the data into RStudio). You can then load the data
into your RStudio environment with the following code:

``` r
library("COUNT")
data(lbw)
```

To learn more about the dataset and variables you can access the help
file for the `lbw` dataframe:

``` r
?lbw
```

-----

### Assessment questions

1)  Draw a DAG to represent your concepual understanding of the causal
    relationship between maternal smoking and birth weight. Write a
    brief descriptive paragraph that highlights any backdoor path(s) and
    the observed variables that might be useful to close the path(s).
    (25%)

*Hint: **The DAG should be conceptual, not driven by the available
variables in the `lbw` dataset.** Not all variables that appear in the
dataset need to be on your DAG and not all nodes that are on your DAG
will necessarily be observed variables. You can draw your DAG using
whatever tool you prefer. Options include `ggdag()` in R,
[daggity.net](http://dagitty.net/dags.html), a screenshot from a DAG
drawn in MS Word etc, or even an embedded picture of a DAG drawn with
pen and paper.*

2)  Match smokers to non-smokers using a matching method of your choice
    and matching variables that are consistent with your DAG, to the
    degree that is possible with the available data. Briefly summarise
    the balance in both cases, drawing on appropriate numerical and
    graphical summaries. (25%)

3)  Fit the model `low ~ smoke` in (i) The raw data and (ii) the matched
    data. Briefly describe the model results. How does the estimated
    effect for smoking change between the two models and how do you
    interpret this? (25%)

4)  Briefly discuss the limitations of the model 3(ii) and argue whether
    or not the assumption of exchangeability is likely to hold. (25%)

-----

### Solution

-----

### Student declaration

***Instructions: Indicate that you understand and agree with the
following three statements by typing an x in the square brackets below,
e.g. \[x\].***

I declare that this assessment item is my own work, except where
acknowledged, and has not been submitted for academic credit elsewhere
or previously, or produced independently of this course (e.g. for a
third party such as your place of employment) and acknowledge that the
assessor of this item may, for the purpose of assessing this item: (i)
Reproduce this assessment item and provide a copy to another member of
the University; and/or (ii) Communicate a copy of this assessment item
to a plagiarism checking service (which may then retain a copy of the
assessment item on its database for the purpose of future plagiarism
checking).

  - [ ] I understand and agree

I certify that I have read and understood the University Rules in
respect of Student Academic Misconduct.

  - [ ] I understand and agree

I have a backup copy of the assessment.

  - [ ] I understand and agree
