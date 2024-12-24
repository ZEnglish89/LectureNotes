An algorithm for performing [[Matrix]] multiplication faster under [[Asymptotic Analysis]] than the naive method, at the cost of vastly increased space complexity.
It operates under [[Divide and Conquer]].

Time complexity $O(n^{log_2(7)})\approx O(n^{2.81})$, compared to the naive method's $O(n^3)$.

It does this by splitting the Matrices up into submatrices, summing or differing them to combine needed properties, and then completing only seven multiplications rather than eight.
The specifics of how this is achieved are over my head, but the point is that the matrices are divided up and combined piecemeal rather than multiplied straightforwardly all at once.