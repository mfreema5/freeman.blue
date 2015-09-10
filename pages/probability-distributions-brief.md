#Probability Distributions Brief
##an introduction to how probability curves are view in sideways statistics


###Measuring foo

Let's jump straight into a fictional example.

You're a quality assurance technician at ACME's chemical plant.  There's a tanker car full of the company's newest product, SnaFoo&copy;, waiting to be certified and shipped.  Your task is to determine the amount of foo in the SnaFoo&copy;.

You take five samples from the rail car, and run them through the lab's Foo-inator 2000&trade;.  The following table are the results, reported in seuss/geisel (s/g). 

Sample |  1  |  2  |  3  |  4  |  5
-------|-----|-----|-----|-----|-----
foo    | 850 | 680 | 670 | 700 | 750


So, how much foo is there?  How confident are you that you know the true foo content?

We'll start to visualize the data with a simple line chart; see Figure 01.  The scale is the amount of foo in the sample, and each large dot is the result of one sample.  (The dots, by the way, are 10 units across, because our Foo-inator 2000&trade; rounds everything off to the nearest 10.)  The lowest result was 670 s/g, the highest was 850 s/g, and the rest of the dots are spread unevenly between between those two.

Next we calculate the mean value of the results&mdash;it's 730 s/g, and the standard deviation is roughly 70.  Now that we have a mean and standard deviation, we can calculate a probability distribution for our results.  That's Figure 02.

The dots for each of the samples are also in Figure 02.  Instead of a dot, though, the mean value is marked by the line that goes from the baseline up to the highest part of the curve, bisecting the area under the curve.  The standard deviation isn't directly represented in Figure 02.  However, since it's what defines the exact shape of the curve of the probability distribution, the standard deviation is indirectly represented.

So, we ask again, how much foo is there?  The highest point in the probability curve is the value with the highest probability of being the true amount of foo.  (The “true” amount is the amount we would measure if we used an infinitely precise and perfectly accurate instrument&mdash;something our Foo-inator 2000&trade; is light-years away from being.)  That highest point is also the mean value from our five samples.  So, we could report that as the amount of foo in the rail-car load of SnaFoo&copy;.

But how confident are we that the mean really is the true value?  The height of the curve at that highest point is 0.5%.  So, we can say that the amount of foo is 730.0 s/g, with 0.5% confidence.  Not a very high confidence level, that.

But, there's another problem: the Foo-inator 2000&trade; rounds everything off to the nearest 10.  Reporting 730.0 s/g implies that we know the amount of foo is above 729.9 s/g, and is also below 730.1 s/g.  However, we don't know that, since the Foo-inator 2000&trade; would report anything between 725 and 735 as “730”.

The dashed lines and shaded area around the mean in Figure 02 are that same region&mdash;the span between 725 and 735 that the Foo-inator 2000&trade; reports as “730”.  So, instead of talking about the percentage represent by the height of the curve at any point, let's consider the *area* of the curve bounded by those dashed lines.  Of the total area under the curve, that middle shaded region is 5.4%.

So, we could report that the amount of foo is between 725 and 735 s/g, with a confidence of 5.4%.  Which is a lot better than our 0.5% confidence in 730.0 s/g, but it's still not very confident.

To be able to report an amount of foo with a higher confidence we have to make that shaded region larger, by spreading the dashed lines apart.  The next graphic, Figure 03, shows some larger shaded regions.  The area bounded by the two dashed lines closes to the mean is 25% of the total.  Between the next two is 75%, which includes the 25% of the first area.  And the next pair outward contain an area that's 95% of the total (and includes the previous areas).

Where do those pairs of dashed lines fall?  They're at:
 
 area | min | max
------|-----|----
 25%  | 706 | 754
 75%  | 645 | 815
 95%  | 585 | 875

We can therefore report with 95% confidence that the amount of foo in the latest batch of SanFoo&copy; is between 585 and 875 s/g.  (Though, this would likely be reported as 730 s/g ± 145 s/g.)

###Everything is foo

The point here is this: you ran some sample, and calculated a single mean value.  But it's very likely that the mean value you calculated was *not* the true value.  In fact, we determined that there was a 99.5% probability that it wasn't.

That mean value is still a useful result, however, because it helps define a range within which the true value most likely falls.

Linear regressions and correlation calculations are the same way.  You put a lot of samples into some software package, and you get some discrete numbers in return.  But most of the time those numbers are *not* the “true” value, in the sense of being infinitely precise and perfectly accurate.  Rather, those numbers mark some region of values, within which lays that essentially unknowable true value.

In sideways statistics, those discrete values are considered to simply mark the middle of a curve of probabilities of the true value.  They aren't a result *per se*, but rather are a way to identify an area of probable results.

However, in sideways statistics, probability curves and their areas are used in a way that differs in one important aspect from the way they were used in the SnaFoo&copy; example here.  In sideways statistics, areas under the curve are often measured starting from one side of the curve, instead of being measured outward from the middle.  Figure 04 shows the same size areas as in the previous graphic (Figure 03), but here they are measured starting from the left side of the curve.  That's why instead of having six dashed lines marking of the different areas, Figure 04 has only three.  But otherwise the meaning of the areas is the same&mdash;it's a measure of the probability of some value being in that region.







