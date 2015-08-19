#Important Insignificance
##An example of understanding statistics by looking at them sideways

When is an insignificant result important?  When you check for the wrong significance.

Note: This discussion employs visual aids I call “sideways statistics”.  They are explained [here](sideways-stats.html).

Say you're about to run an linear regression.  You've already determined the expected size of effect, you've set the significance bar at an alpha of 0.05, and with those two you've determined the sample size to give you a statistical power of 0.84.  Figure 01 shows your statistical experiment as designed.

[Figure 01](images/large/basic-alpha-beta-es-n.svg)

The minimum correlation that is statistically significant is marked by the line that bisects the population probability curve on the right side of the graphic.  Since you set alpha to 0.05, 5% of the area bounded by the population probability curve extends below the null line.

That's all the same in the next graphic, Figure 02, but the arrow is pointing to the line that marks the results of your analysis.  It has failed to be large enough to qualify as statistically significant.

[Figure 02](images/large/alpha-beta-es-n-with-result.svg)

Most people would assume that the analysis was a bust and that without a statistically significant correlation, you can't really say anything definitive about the results.  But that isn't true.

Let's move on to Figure 03, in which the minimum statistically significant correlation has been removed, so that now the curve on the right side of the graphics is the population probability curve that's centered on the **result** from your hypothetical analysis.  That result is not “statistically significant” at ‘p<.05’ because more than 5% of the area between that curve and the vertical baseline is below the horizontal null line.

[Figure 03](images/large/insignificant-result.svg)

But that's going on at the bottom of the population probability curve.  Let's consider the top of that curve, where there's been a new line added to the graph, one that's marked with an arrow.  Below that line is 95% of the area between the population probability curve and the vertical baseline.  Which means you can say, with a confidence of ‘p<.05’, that the population correlation is *no higher than that line*.

Therefore, another way to look at the results of your analysis is to say that you have found a statistically significant “upper bound” for the population correlation.  Whether or not that is a useful thing to know depends on what real-world phenomena your data is tracking.

So, for example, if your data is tracking the effectiveness of some new investment strategy by correlating its implementation to the change in overall returns, it might be fairly straight-forward to determine the minimum impact required to make it worthwhile to use the new strategy.  Whatever correlation matches to that impact becomes the minimum correlation that supports using the new strategy.

In a scenario such as that, a null-hypothesis significance test would likely be useless to you.  If it wasn't readily apparent&mdash;or at least highly probable&mdash;that the new strategy would improve outcomes, no one would even be trying.  That there will be an improvement is something of a foregone conclusion; what matters is the degree of the improvement.  And what matters to you is the confidence with which you can state that the correlation you find through your analysis is either higher or lower than the minimum correlation that supports using that new strategy.

If we combine this hypothetical scenario with the hypothetical results from earlier, we can say that it doesn't matter that the resulting correlation didn't achieve statistical significance compared to null.  What matters in this case is whether or not the upper bound we found is lower than the minimum correlation that supports using the new procedure.  Because if it is, we can say with a confidence of ‘p<.05’ that the new strategy isn't worth implementing.  Even though we can't say (with the same confidence) that the correlation isn't significantly different than zero.

So, what would it look like if we designed our experiment from the beginning to check for something such as that?  That is, let's test to see if we can say, with 95% confidence, that a correlation is lower than some value that we interpret as the minimum **important** correlation?

Instead of the sample probability curve on the left side of the graph being centered around the expected effect size, it would be centered around the value that's the minimum important correlation.  Then, the population probability curve on the right side of the graph would be positioned so that 95% of the area between it and the vertical baseline would be below the minimum important correlation.  The line that bisects the population probability curve is therefore the maximum correlation that demonstrates that the correlation does not meet your criteria for importance.  See Figure 04.

[Figure 04]()

This sort of analysis is called [NAME]?  Check your preferred reference for how to actually crunch the numbers (e.g., [CITE…]).




+++++
Previously…

Hopefully this is not news to you, if you've had any training in statistics.  Because statistical significance can be tested the same way between *any* two correlations.  It's common to set one of those correlation equal to zero, a.k.a., null, and thus you get “null-hypothesis significance testing”.

Like many mathematical models involving zero, null-hypothesis significance testing represents something of a special case.  By checking against the null hypothesis, you are in fact comparing the correlation you found to all the correlations you might have found due to sampling error alone.  More specifically, you're making sure that the correlation you found is at least larger than the largest correlation you might have found due solely to sampling error.

This is why it is meaningless to run a null-hypothesis significance test on a data set which contains the entire population of subjects.  There is no sampling error, because there is no difference between the sample being used and the population, so any correlation you might find cannot be due to sampling error.

To understand that visually, consider Figure ##, which simply shows the effect that increasing the sample size, N, has on the minimum statistically significant correlation of an analysis.  In the figure, sample size increases from right to left.  The shape of the population probability curve tightens as the sample size increases.  Therefore, the mid-line of that curve gets closer to the null line; in other words, with a larger sample size, a lower correlation can be significant.

And when the sample size grows so large as to comprise the entire population, N effectively becomes infinite, the population probability curve collapses into a line, that is coincident with the null line&mdash;therefore, when there is no sampling error, *the minimum statistically significant correlation is zero*.








