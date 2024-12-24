One of the basic principles of Algorithm Design(and also just of life), the strategy of breaking a large problem up into several smaller problems, and optimizing the solutions of those smaller problems individually.

This allows solutions to be modular, making each individual section easier to debug/optimize and compatible with more than just a single environment.

Often the breaking of these problems can be done recursively, so that rather than breaking up the problem into *different* problems, the *dataset* can be broken up and the same solution can take place on each section of it, before combining the sections.

For example, you can Divide and Conquer integer multiplication by pairing off the digits and adding the products of each pair, which is the traditional method learned in elementary school.
Via [[Asymptotic Analysis]], this method runs at a time complexity of $O(n^2)$.