---
layout: page
title: What the notes argue
description: Five arguments the Spring 2016 labs and lectures actually ask you to make.
samwiki: true
---

<p class="sw-note">These are not a second syllabus. Each one is a claim already written into a lecture or a lab in this repository: the dataset, the comparison, and the mistake the assignment is trying to make visible.</p>

<section class="sw-section sw-insight" id="simpson">
  <div class="sw-section-head">
    <h2>The overall line can be the wrong story</h2>
    <p>Lecture 1 · state SAT scores, 1994–95</p>
  </div>
  <p class="sw-note">The opening lecture defines a narrative as an account that puts events in order and establishes a connection between them. The SAT example is the warning that a connection depends on the grouping.</p>
  <p class="sw-note">The slides plot average total SAT score against estimated public-school teacher salary for states. Then they cut the percent of students taking the SAT at 22, 49, and 81 and draw a separate line inside each group, with the overall line still on the page. The lecture asks what you can conclude, and it names the disagreement <a href="https://en.wikipedia.org/wiki/Simpson%27s_paradox">Simpson’s paradox</a>. The next frames drop the statistical name and show the same risk as a joke: U.S. spending on science against suicides by hanging, and pool drownings against the number of Nicolas Cage films. A correlation is not yet the grouping the story belongs to.</p>
  <p class="sw-meta">Source: <a href="{{ '/assets/lectures/lecture1-intro-regression/lecture1-intro-regression.pdf' | relative_url }}">Lecture 1 slides</a> and <a href="{{ '/assets/lectures/lecture1-intro-regression/simpsons-paradox-sat-scores.R' | relative_url }}">the SAT code</a>.</p>
</section>

<section class="sw-section sw-insight" id="shuffle">
  <div class="sw-section-head">
    <h2>A fair shuffle does not look fair</h2>
    <p>Lab 1 · the iPod, adapted from CATALST</p>
  </div>
  <p class="sw-note">The lab opens with Steve Jobs on a thousand songs in a pocket, then with Carl Bialik’s Wall Street Journal piece from 21 September 2006. Mads Haahr, who runs Random.org, orders an iPod engraved “God Plays Dice” because users do not believe shuffle is random.</p>
  <p class="sw-note">The definition in the lab has two parts. In a long run, each song shows up about equally often. And the next song cannot be predicted from the last one: song 5 does not always follow song 3. Landon Curt Noll is quoted to the effect that people are bad at recognizing randomness, and that a favorite song feels overplayed because you notice it. Before any calculation, the lab asks what a non-random sequence would look like, and whether you can be 100 percent sure a playlist was not generated at random. A single finite playlist cannot buy that certainty. Randomness here is a property of the process, not a look you can confirm by inspection.</p>
  <p class="sw-meta">Source: <a href="{{ '/assets/labs/lab1-ipod-shuffle/lab1-ipod-shuffle-individual.html' | relative_url }}">individual lab</a> and the <a href="{{ '/assets/labs/lab1-ipod-shuffle/lab1-ipod-shuffle-group.html' | relative_url }}">group version</a>.</p>
</section>

<section class="sw-section sw-insight" id="compared-to-what">
  <div class="sw-section-head">
    <h2>Compared to what?</h2>
    <p>Visualization lecture · 25 January 2016</p>
  </div>
  <p class="sw-note">The principles lecture, adapted from the Johns Hopkins Data Science Specialization and from swirl, treats a graphic as a piece of evidence rather than a chart type. Evidence is always relative to some other account, so the first question on the slide is “Compared to what?”</p>
  <p class="sw-note">The six principles that follow are the rest of the standard. Show the mechanism you think is operating. Show more than two variables, which the slide calls escaping flatland, because the real world is multivariate. Integrate words, numbers, and pictures instead of letting the software choose the analysis. Document labels, scales, and sources so the graphic tells a complete story. And content is king: the presentation stands or falls on the quality of what it contains. Exploratory graphs have a separate job list on the next section: understand the data, find a pattern, suggest a model, debug an analysis, and only then communicate a result. The NHANES and ggplot2 lectures are the practice set for that list.</p>
  <p class="sw-meta">Source: <a href="{{ '/assets/lectures/data-viz-principles/data-viz-principles-and-EDA.html' | relative_url }}">principles and EDA</a>, <a href="{{ '/assets/lectures/data-viz-ggplot/data-viz-ggplot.html' | relative_url }}">ggplot2</a>, <a href="{{ '/assets/lectures/data-viz-NHANES/Presentation-NHANES.html' | relative_url }}">NHANES</a>.</p>
</section>

<section class="sw-section sw-insight" id="null">
  <div class="sw-section-head">
    <h2>The null is a world you can simulate</h2>
    <p>Lady tasting tea · Lab 5 on FEV</p>
  </div>
  <p class="sw-note">The March 2016 confidence slides retell Fisher’s lady tasting tea from 1935. She claims she can tell whether milk or tea was poured first. The exercise turns each guess into a coin. <code>rflip(10)</code> is one lady and ten cups. <code>do(5000) * rflip(10)</code> is five thousand ladies who are only guessing. The question on the slide is how often a fair coin yields 9 or 10 heads, and what to make of the rumor that the original lady got all ten. The reusable loop is written out: compute your metric on the real data, compute it on one random dataset, compute it on many, and ask whether randomness describes the original result.</p>
  <p class="sw-note">Lab 5 runs that loop inside a regression. The FEV file, loaded from Vanderbilt through <code>Hmisc::getHdata</code>, has 654 people and six variables. Forced expiratory volume is the outcome. A boxplot of FEV by smoking status is high enough among current smokers that the lab asks why before you interpret it. The model is <code>fev ~ age + smoke + height + sex</code>. Shuffling <code>smoke</code> builds a world where that coefficient is zero because the association has been broken, and <code>do()</code> refits the model many times. The fraction of shuffled coefficients farther from zero than the real coefficient is a permutation p-value. <code>summary()</code> prints the t-approximation to the same question. The extra credit then fits the same equation twice and runs <code>anova()</code> with <code>smoke</code> in a different position. The p-value for smoking moves. The equation did not. The lab sends you to Kaplan, sections 15.2 and 15.3, for why sequential tests depend on order.</p>
  <p class="sw-meta">Source: <a href="{{ '/assets/lectures/lecture6-confidence/lady-slides.html' | relative_url }}">confidence slides</a>, <a href="{{ '/assets/labs/lab5-inference/lab5.pdf' | relative_url }}">Lab 5</a>, <a href="{{ '/assets/labs/lab4-fev/lab4-fev.pdf' | relative_url }}">Lab 4 on choosing among FEV models</a>.</p>
</section>

<section class="sw-section sw-insight" id="missing">
  <div class="sw-section-head">
    <h2>Dropping missing rows drops people</h2>
    <p>Titanic lab · missing-data lecture · Challenger quiz</p>
  </div>
  <p class="sw-note">Lab 6 and the missing-data lecture use the same passenger table. Age is missing often enough that the lab has you create <code>age_mis</code> and tabulate it against sex before you delete anyone. The lecture’s three labels are precise. Missing completely at random means nothing observed or unobserved is related to the gap. Missing at random means the gap can depend on what you measured. Missing not at random means it depends on what you never saw. The slide cites Burton and Altman (2004) for the reporting rule: quantify how complete the covariates are, show the pattern, and say what the analysis did about it. <code>na.pattern</code> and Amelia’s <code>missmap</code> are the tools on that slide.</p>
  <p class="sw-note">The lab then filters to passengers whose age is present, and it says the quiet part: this is rarely a good assumption, and the remaining rows may no longer represent everyone on the ship. The worked logistic example in the lab source is <code>survived ~ age * sex + pclass</code> on that filtered table. A predicted probability from <code>predict(..., type = "response")</code> is a probability for that smaller group. The April quiz is the other half of reading a logistic model. Twenty-three shuttle launches, damage as a function of temperature centered at 60°F, so the intercept is the log-odds at 60 degrees rather than at zero. The probability is the inverse logit of the linear predictor. One of the three figures draws the slope with the sign reversed. Fitting the model is not the same as reading which curve you were handed.</p>
  <p class="sw-meta">Source: <a href="{{ '/assets/labs/lab6-titanic/lab6-titanic.pdf' | relative_url }}">Lab 6</a>, <a href="{{ '/assets/lectures/lecture9-missing-data/lecture9-missing-data.pdf' | relative_url }}">missing-data slides</a>, <a href="{{ '/pages/quiz-logistic.pdf' | relative_url }}">logistic quiz</a>.</p>
</section>
