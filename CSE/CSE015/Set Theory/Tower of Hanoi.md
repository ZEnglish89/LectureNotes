Can be solved using a recurrence relation.

{H<sub>n</sub>} denotes the number of moves needed to solve the puzzle when there are n disks.

To move all but the bottom disk to peg 3, it takes H<sub>n-1</sub> moves.
It then takes an additional one move to move the bottom disk to peg 2, and H<sub>n-1</sub> moves again to move all the other disks on top of it.
Therefore H<sub>n</sub> = 2H<sub>n-1</sub> +1 moves, with an initial condition of H<sub>1</sub> = 1.
This can be solved with H<sub>n</sub> = 2<sup>n</sup> - 1 moves.
