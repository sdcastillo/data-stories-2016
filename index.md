---
layout: page
title: Telling Stories with Data
description: PUBHLTH 490ST, Spring 2016 at UMass Amherst. Regression, visualization, and data stories in R.
samwiki: true
---

<section class="sw-lede" aria-labelledby="sw-about-title">
  <div class="sw-lede-copy">
    <h2 id="sw-about-title">A course site you can still read</h2>
    <p>This is the public site for Telling Stories with Data, PUBHLTH 490ST, from Spring 2016 at the University of Massachusetts Amherst. Nicholas Reich taught it, and Chu-Yuan Luo was the TA. Class met Tuesdays and Thursdays, 2:30–3:45. What you have here is the overview, schedule, slides, labs, and project briefs the course actually used.</p>
    <p>It was a second course after an introduction such as BIOSTATS 391B, STAT 240, STAT 501, ResEcon 212, or PSYCH 240, and a faster path for someone who already had AP Statistics or another college introduction. The work is summarizing, visualizing, modeling, and analyzing real data, with biological and biomedical examples when the datasets support them.</p>
    <p>The modeling sequence is simple and multiple linear regression, least squares, interpretation and inference, goodness of fit, diagnostics, and model selection. From there the term goes to bootstrap inference, smooth splines, an introduction to logistic regression, an introduction to longitudinal data, and Poisson regression if the calendar reached it. Computing is in R, and by the end of the term the programming is meant to be yours, not a walkthrough you only watch.</p>
    <p>Start with the pages that are already rendered in this repository: the <a href="{{ '/assets/labs/lab1-ipod-shuffle/lab1-ipod-shuffle-individual.html' | relative_url }}">iPod shuffle lab</a>, the visualization lectures on <a href="{{ '/assets/lectures/data-viz-principles/data-viz-principles-and-EDA.html' | relative_url }}">principles</a>, <a href="{{ '/assets/lectures/data-viz-ggplot/data-viz-ggplot.html' | relative_url }}">ggplot2</a>, and <a href="{{ '/assets/lectures/data-viz-NHANES/Presentation-NHANES.html' | relative_url }}">NHANES</a>, and the <a href="{{ '/assets/lectures/lecture6-confidence/lady-slides.html' | relative_url }}">confidence slides</a>. The <a href="{{ '/pages/schedule.html' | relative_url }}">schedule</a> and the <a href="{{ '/pages/slides.html' | relative_url }}">slides page</a> are the map for the rest of the term, including the regression labs and the deadlines.</p>
    <p>The assignments ask for a short story, not every model that happens to fit. <a href="{{ '/pages/project1.html' | relative_url }}">Project 1</a> is a reproduction of a published analysis that already shares its data and code, plus a follow-up report. The <a href="{{ '/pages/project.html' | relative_url }}">final project</a> is a small group: a shared data summary, one analysis from each person, and at least one regression model, written in RMarkdown or knitr so the numbers come from R. Due dates, Piazza, and the Arnold House office hours belong to that semester. The texts were Daniel Kaplan’s <a href="http://www.mosaic-web.org/go/StatisticalModeling/">Statistical Modeling: A Fresh Approach</a> and the free <a href="http://www.openintro.org/stat/index.php">OpenIntro Statistics</a>. This archive sits on <a href="https://sdcastillo.github.io/samwiki/">SamWiki</a>.</p>
  </div>
  <aside class="sw-find" aria-labelledby="sw-find-title">
    <h2 id="sw-find-title">What you’ll find</h2>
    <ul>
      <li><strong>Linear and logistic regression</strong> Least squares, diagnostics, model selection, and an introduction to Poisson regression.</li>
      <li><strong>Uncertainty</strong> Confidence, hypothesis tests, and inference with the bootstrap.</li>
      <li><strong>Visualization</strong> Principles of graphics, ggplot2, and a multivariate look at NHANES.</li>
      <li><strong>Labs in R</strong> iPod shuffle, simple and multiple regression, FEV, hypothesis tests, and the Titanic.</li>
      <li><strong>A data story</strong> A short group write-up and one individual analysis, with a regression model in the argument.</li>
    </ul>
  </aside>
</section>

#### Course summary
The aim of this course is to provide students with the skills necessary to tell interesting and useful stories in real-world encounters with data. Students will learn fundamental concepts and tools relevant to the practice of summarizing, visualizing, modeling, and analyzing data. Students will learn how to build statistical models that can be used to describe multidimensional relationships that exist in the real world. Specific methods covered will include linear, logistic, and Poisson regression. This course will introduce students to the R statistical computing language and by the end of the course will require substantial independent programming. To the extent possible, the course will draw on real datasets from biological and biomedical applications. This course is designed for students who are looking for a second course in applied statistics/biostatistics (e.g. beyond BIOSTATS 391B or STAT 240), or an accelerated introduction to statistics and modern statistical computing. 

<img src="{{ '/cover-image.png' | relative_url }}" alt="Course cover: Telling Stories with Data, with a cartoon figure on a path toward a sign that reads This way to the data." width="600"/>


---

#### Course Details

**Course number**: PUBHLTH 490ST 

**Instructor**: [Nicholas Reich](http://reichlab.github.io)

**TA**: Chu-Yuan Luo

**Office hours**: Wednesdays 11:30-12:30 (Instructor), or Mondays 12-1pm (TA, in 211 Arnold House), or by appointment

**Prerequisites**: <br> 
One of any of the following introductory stats courses taught at UMass: BIOSTAT 391B, STAT 240, STAT 501, ResEcon 212, PSYCH 240. If you have not taken an intro stats course at UMass but still want to enroll in this course, you are encouraged to petition the instructor for permission, especially if any of the following apply: (a) you have taken AP Stats in high school, (b) you have taken a college-level intro stats course just not one of the ones listed above, or (c) you are confident in your quantitative skills and your ability to succeed in a fast-paced, advanced introductory course.

**Lectures**: Tu/Th, 2:30pm&ndash;3:45pm

**Required books** <br>
&nbsp; &nbsp; Kaplan D. 2012. [Statistical Modeling: A Fresh Approach](http://www.mosaic-web.org/go/StatisticalModeling/). 

**Recommended book (free download)** <br>
&nbsp; &nbsp; Diez D, Barr C, and &Ccedil;etinkaya-Rundel M. 2012. [OpenIntro Statistics, 3rd Ed.](http://www.openintro.org/stat/index.php)


**Topics covered**<br>
&nbsp; &nbsp; Simple and multiple linear regression <br>
&nbsp; &nbsp; Least squares estimation, interpretation and inference about linear regression <br>
&nbsp; &nbsp; Goodness of fit, model diagnostics<br>
&nbsp; &nbsp; Model selection<br>
&nbsp; &nbsp; Inference using bootstrapping<br>
&nbsp; &nbsp; Smooth splines<br>
&nbsp; &nbsp; Logistic regression (introduction)<br>
&nbsp; &nbsp; Longitudinal data analysis (introduction)<br>
&nbsp; &nbsp; Poisson regression (introduction, time permitting)<br>

---

The [source for the website](https://github.com/nickreich/data-stories-2016) 
