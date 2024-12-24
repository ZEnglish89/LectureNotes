The act of gathering data from a phenomenon which is not fully understood, in an attempt to model it such that the model can be used to make additional, accurate predictions.

"Drawing repeated results from a fixed, underlying, and unknown distribution."

Samples are considered [[Independent]] and Identically Distributed(IID) if they:
1) Come from the same fixed distribution(Identically Distributed).
2) Are [[Independent]](duh I suppose).

The average of a large number of samples of distribution X will be the same as the "true" average of X.
The variance will be equal to $Var(X)/n$ where n is the number of samples.
This is the [[Central Limit Theorem]].

Attempting to find the original distribution via averages is not completely reliable: As a result of reducing the variance, the distribution of the average will bias towards the mean.

As such, as the number of samples increases, the distribution of the average approaches a normal distribution, a bell curve, rather than the "true" distribution.