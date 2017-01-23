# Visualizing-Diabetes-Prediction-
Visualizing Type 2 Diabetes risk with a multivariate logistic regression using d3.js


<div class="topbar">

<div class="topbar-inner">

<div class="container-fluid">[Michael Moliterno](/)

*   [cv/résumé](https://michaelmoliterno.github.io/docs/Michael_Moliterno_CV.pdf)
*   [blog](/category/blog.html)

[[archives]](/archives.html) [[tags]](/tags.html)

</div>

</div>

</div>

<div class="container-fluid">

<div class="sidebar">

<div class="well">

<div class="social">

#### Find me:

*   [GitHub](https://github.com/michaelmoliterno)
*   [LinkedIn](https://www.linkedin.com/in/michaelmoliterno)

</div>

#### My go-to resources:

*   [python](http://python.org/)
*   [pandas](http://pandas.pydata.org/)
*   [scikit learn](http://scikit-learn.org/stable/documentation.html)
*   [d3.js](https://github.com/mbostock/d3/wiki)

</div>

</div>

<div class="content">

<div class="article span16">

<div class="page-header">

# Visualizing Diabetes Prediction with d3.js

</div>

<div class="well small">Permalink: [Visualizing Diabetes Prediction with d3.js](/visualizing-diabetes-prediction-with-d3js.html) by [Michael Moliterno](/author/michael-moliterno.html)  
tags: [logistic regression](/tag/logistic-regression.html) [d3.js](/tag/d3js.html) [data visualization](/tag/data-visualization.html)</div>

<div>

### Predicting the Risk of Type 2 Diabetes

I recently revisited [an old Kaggle competition](https://www.kaggle.com/c/pf2012-diabetes) that challenged entrants to use electronic health records (EHR) from Practice Fusion's database to identify patients diagnosed with Type 2 Diabetes. Given a set of ~10,000 electronic health records, I developed a set of classifiers for Type 2 Diabetes. While my classifiers were not quite as good as the winning models, I was happy with my results; I think would have placed in about the middle of the leaderboard if I had entered when the competition was active (a post on the classifier development will be posted to the blog shorty).

### d3.js = Visualization

To borrow from Mike Bostock (co-creator/co-developer of d3.js):

> D3.js is a JavaScript library for manipulating documents based on data. D3 helps you bring data to life using HTML, SVG and CSS. D3’s emphasis on web standards gives you the full capabilities of modern browsers without tying yourself to a proprietary framework, combining powerful visualization components and a data-driven approach to DOM manipulation.

Check out the full [d3.js documentation](https://github.com/mbostock/d3/wiki) to see all of the implementation and configuration options. Here are some of [Mike Bostock’s best examples](http://bl.ocks.org/mbostock).

### Visualizing Classifiers

One of the challenges in using machine learning is communicating results to colleagues and decision makers that are not data nerds. Support Vector Machines (SVMs) and random forests are nearly impossible to visualize in high dimensions. Decision trees are fairly easy to visualize, but they are not particularly useful in many cases. As I was mulling over this limitation and thinking about useful visualizations to build in d3.js, I came up with an idea for visualizing a multivariate logistic regression.

By keeping one variable on an axis (e.g. BMI), and allowing other variables to be modified with sliders (e.g. age) and radio buttons (e.g. gender), we can see a dynamic logistic regression curve (which we can think of as a risk profile for Type 2 Diabetes). Even cooler, we can see how the risk profile changes as other explanatory variables are modified.

### Logistic Regression with d3.js

Below is d3.js visualization of a simplified version of a logistic regression models that I developed. The most accurate models I developed had 20+ features, but I decided to keep it simple for the visualization (which I think makes it more usable and intuitive).

<iframe src="/images/diabetes_logistic_regressions_d3_small.html" width="710" height="570"></iframe>

Some of the features that took a bit of time to build were:

*   the brush on the bottom that allows you to zoom into a smaller range on the BMI axis (try it!)
*   the updating values on each axis (when the brush is created and moved)
*   the risk values and corresponding points that track the curves
*   the age slider and gender radio buttons that sent updates to the SVG
*   and of course, the dynamic logistic regression curves that adjust as input variables are updated

You can check out the source to the [d3 code on my github](https://github.com/michaelmoliterno/d3).

</div>

<div>

## Comments

<footer>

Powered by [Pelican](http://getpelican.com/).

© Michael Moliterno

</footer>

</div>

</div>

</div>

</div>
