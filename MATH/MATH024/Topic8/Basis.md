
A basis for a [[Vector Space]] is a collection of vectors having two properties at once, called Basis Vectors:
1. Those vectors have [[Linear Independence]]
2. Those vectors [[Span]] the [[Vector Space]]

$\hat{e}_1=(1,0)$ is Linearly Independent, but it does not span $\mathbb{R}^2$.

$[(1,0),(0,1),(1,1)]$ span $\mathbb{R}^2$, but they are not Linearly Independent.

The Pivot Columns(See [[Gauss Elimination]]) are exactly the columns which form a Basis.

The number of Basis Vectors is called the dimension.
Despite the infinite number of basis vectors(because they may be rewritten), dimension is an intrinsic part of that space. Additional vectors beyond the dimension will be redundant, see [[Span]].
So the dimension of a [[Vector Space]] is the same as the Rank of the [[Matrix]] which is the same as the number of Pivot Columns???

In $\mathbb{R}^n$ a basis has at *least* $n$ vectors that [[Span]] $\mathbb{R}^n$, and at the same time has at *most* $n$ vectors that have [[Linear Independence]].
That means that for a set $\mathbb{R}^n$ of dimension $n$, there are exactly $n$ basis vectors.
Any Linearly Independent set in $\mathbb{V}$ can be extended into a basis by adding appropriate vectors as necessary.
Any Spanning set in $\mathbb{V}$ can be reduced to a basis by deleting appropriate(redundant) vectors as necessary.

A Basis is a maximal Linearly Independent Set. It cannot be made any larger without losing [[Linear Independence]].
A Basis is a minimally [[Span]]ning set. It cannot be made any smaller without ceasing to [[Span]].