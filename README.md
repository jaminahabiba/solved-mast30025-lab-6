Download Link: https://assignmentchef.com/product/solved-mast30025-lab-6
<br>
Questions 1–7 use the ‘sleep’ dataset, which you can download from the course website. This dataset contains (among other things) data on the body weight (kg) and brain weight (g) of 62 mammals. Use the following commands to read the data:

<em>&gt; mammals &lt;- read.csv(“../data/sleep.csv”)</em>

<em>&gt; mammals$BodyWt &lt;- log(mammals$BodyWt)</em>

<em>&gt; mammals$BrainWt &lt;- log(mammals$BrainWt)</em>

This creates a data frame, mammals, with components (among others) named BodyWt and BrainWt, then applies a logarithmic transformation to both BodyWt and BrainWt.

<ol>

 <li>Fit a linear model explaining brain weight from body weight, using the lm</li>

</ol>

Display the summary of the fitted model, and then create a scatter plot of the data and superimpose the fitted regression line on it. Does it look like a reasonable fit?

Use diagnostic plots to assess if the model assumptions are satisfied.

<ol start="2">

 <li>Using the fitted model or otherwise, obtain:

  <ul>

   <li>The least squares estimator of the parameters, <strong>b</strong>;</li>

   <li>The vector of residuals, <strong>e</strong>;</li>

   <li>The residual sum of squares, <em>SS<sub>Res</sub></em>;</li>

   <li>The regression sum of squares, <em>SS<sub>Reg</sub></em>;</li>

   <li>The estimator for the variance of the errors, <em>s</em><sup>2</sup>;</li>

   <li>The standardised residuals;</li>

   <li>The leverages of the points;</li>

   <li>The Cook’s distances of the points;</li>

   <li>95% confidence intervals for each of the parameters.</li>

  </ul></li>

 <li>Find a 95% confidence interval for a mammal weighing 50 kg.</li>

 <li>Find a 95% prediction interval for a mammal weighing 50 kg.</li>

 <li>Find and draw a 95% joint confidence region for the parameters.</li>

 <li>Test the following hypotheses, using the anova

  <ul>

   <li><em>H</em><sub>0 </sub>: <em>β </em>= 0</li>

   <li><em>H</em><sub>0 </sub>: <em>β</em><sub>1 </sub>= 0</li>

   <li><em>H</em><sub>0 </sub>: <em>β</em><sub>0 </sub>= 0</li>

   <li><em>H</em><sub>0 </sub>: <em>β </em>= (2<em>,</em>1)</li>

  </ul></li>

 <li>By visualising the raw data, justify the use of a double logarithmic transformation. Write downthe final model for the (untransformed) brain weight vs. body weight.</li>

 <li>In this question we consider the hypothesis <em>H</em><sub>0 </sub>: <em>β </em>= <em>β</em><sup>∗</sup>. The test statistic for this hypothesis is</li>

</ol>

<em>.</em>

1

<ul>

 <li>Show that</li>

</ul>

(<strong>b</strong>−<em>β</em><sup>∗</sup>)<em><sup>T</sup>X<sup>T</sup>X</em>(<strong>b</strong>−<em>β</em><sup>∗</sup>) = (<strong>y</strong>− <em>X</em><em>β</em><sup>∗</sup>)<em><sup>T</sup></em>(<strong>y</strong>− <em>X</em><em>β</em><sup>∗</sup>) − (<strong>y</strong>− <em>X</em><strong>b</strong>)<em><sup>T</sup></em>(<strong>y</strong>− <em>X</em><strong>b</strong>)<em>.</em>

That is, it is the <em>SS<sub>Res </sub></em>for the null model minus the <em>SS<sub>Res </sub></em>for the full model. Also show that

(<strong>b</strong>−<em>β</em><sup>∗</sup>)<em><sup>T</sup>X<sup>T</sup>X</em>(<strong>b</strong>−<em>β</em><sup>∗</sup>) 6= <strong>y</strong><em><sup>T</sup>X</em>(<em>X<sup>T</sup>X</em>)<sup>−1</sup><em>X<sup>T</sup></em><strong>y</strong>−<em>β</em><sup>∗</sup><em>X<sup>T</sup>X</em><em>β</em><sup>∗</sup><em>.</em>

That is, in this case we can not write it as the <em>SS<sub>Reg </sub></em>for the full model minus the <em>SS<sub>Reg </sub></em>for the model under <em>H</em><sub>0</sub>.

<ul>

 <li>Show directly that (<strong>b</strong>−<em>β</em><sup>∗</sup>)<em><sup>T</sup>X<sup>T</sup>X</em>(<strong>b</strong>−<em>β</em><sup>∗</sup>) and <em>SS<sub>Res </sub></em>are independent, that is without using our existing results that <strong>b </strong>and <em>SS<sub>Res </sub></em>are independent.</li>

</ul>

Hint: set <strong>q </strong>= <strong>y</strong>− <em>X</em><em>β</em><sup>∗ </sup>then

<ol>

 <li>Show that (<strong>b</strong>−<em>β</em><sup>∗</sup>)<em><sup>T</sup>X<sup>T</sup>X</em>(<strong>b</strong>−<em>β</em><sup>∗</sup>) = <strong>q</strong><em><sup>T</sup>X</em>(<em>X<sup>T</sup>X</em>)<sup>−1</sup><em>X<sup>T</sup></em><strong>q</strong>.</li>

 <li>Show that <em>SS<sub>Res </sub></em>= <strong>q</strong><em><sup>T</sup></em>[<em>I </em>− <em>X</em>(<em>X<sup>T</sup>X</em>)<sup>−1</sup><em>X<sup>T</sup></em>]<strong>q </strong>and hence that these two quadratic forms are independent.<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/811.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/811.png?w=980&amp;ssl=1" data-recalc-dims="1">

  </noscript>6</li>

</ol>