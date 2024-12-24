
Once you have results to test your hypothesis against, you can calculate the probability that you achieved a result at least as extreme as those you received. The more unlikely that results of that extremity become, the stronger the results discredit your hypothesis. The reverse is of course also true, the more likely the stronger the evidence supports the hypothesis.

For example, when dealing with the German Tank problem: If you believe the population to be 500, and you receive serial numbers of 29, 42, 13, and 41, then you can test the hypothesis by finding the probability that four samples from a population of 500 have a maximum of 42.
$P(max<=42) = (42/500)^4 = 4.9787 \times 10^{-5}$, which is extremely unlikely.

The "Null Hypothesis" is the hypothesis being tested.
The "Alternative Hypothesis" is the alternative to the null hypothesis. These MUST be complementary and mutually exclusive; the alternative hypothesis must be written such that there is no possibility of both hypotheses being false.

p-value: The probability that a test statistic is "at least as extreme" as the observed value within the test.

Before conducting hypothesis testing, set an acceptable confidence level: Choose a minimum p-value for which you would still accept the null hypothesis.

If the calculated p-value is below the confidence level, reject the null hypothesis. Otherwise, accept it.
This system cannot be used to prove a null hypothesis true, simply to conclude that there is not strong evidence against it.

Rejecting a true hypothesis is a "type 1 error."
Failing to reject a false hypothesis is a "type 2 error."

The p-value is the probability of making a type 1 error, given that the hypothesis is true.
Given that the hypothesis is false, the probability of making a type 2 error is 1-p.