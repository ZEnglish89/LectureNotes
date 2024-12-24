
When given two strings, this algorithm will find the longest common sequence that the strings share in common, even if one or both strings have characters separating the elements of the subsequence.

It uses the [[Dynamic Programming]] paradigm.

This operates in time $O(mn)$ if one string has $n$ characters and the other has $m$.

Pseudocode:
```
LCS(X,Y):
	for(int i=0;i<=m;i++):
		C[i][0] = 0;
	for(int j=0;j<=n;j++):
		C[0][j] = 0;
	for(int i=1;i<=m;i++):
		for(int j=1;j<=n;j++):
			if X_i[i] = Y_j[j]:
				C[i][j] = C[i-1][j-1]+1;
			else:
				C[i][j] = max(C[i][j-1],C[i-1][j]);
	return C[m][n];
```

I'm not wholly sure how to describe what variable corresponds to what. This is contained within Lecture 23.