
Updating a probability given additional information: For example, in the following scenario, there is a 10% chance of you having the given disease, but KNOWING that you tested positive, you can update that probability to 8/17 or 47%.

"Sensitivity" is the likelihood of a false negative, an 80% sensitivity means that 80% of positive conditions will actually return a positive test.
"Specificity" is the likelihood of a false positive, a 90% specificity means that 90% of negative conditions will actually return a negative test.

If there is a 10% chance of the condition being positive, an 80% sensitivity, and a 90% specificity:

There will be more false positives(9%) than accurate positives(8%)
There will be a large number of false negatives(2%) compared to the number of positive conditions(10%)

Sensitivities and specificities which intuitively seem very accurate have the potential to still return very unreliable results.

Lab tests will only be accepted with stats above 99%, but things like rapid at-home tests for diseases like covid can still have stats this poor(that's why repeated testing was pushed so hard, because the tests were fundamentally likely to throw errors)

Notation in terms of events and compliments: D = have disease, D<sup>C</sup> = Do not have disease, T = Test positive, T<sup>C</sup> = Test negative,
$P(D | T) = P(D \cap T)/P(T)$ or the probability of having the disease and testing positive divided by the probability of testing positive.

D | T is read as "D given T"

For all situations: $P(A | C) = P(A\cap C)/P(C)$
This is [[Baye's Theorem]].

$P(A \cup C) = P(A) + P(C) - P(A \cap C)$
Use that to solve for anything you need in Conditional Problems, either the union or intersection will be given most of the time.