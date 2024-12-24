Hey I'm learning about these in Data Structures!

Sorts pieces of data into separate lists based on some large category of some kind, rather than having them all in the same list.

For example, while sorting students by their student ID number, a hash function would sort the students into ten lists, with one list for each possible final digit of the number(0-9). In other words, the hash function would be h(n) = n mod 10, where n is the student's ID number.

h(n) = n mod k is a very common hash function, where k is the number of smaller lists.

Because the different lists are based off of some parameter, the total list can be guaranteed to be at least partially sorted at all times, and which smaller list each data point can be found in is known, so to find any particular data point in the total data-set, only one of the smaller lists needs to be sorted/searched, allowing [[Algorithm]]s with [[Time Complexity]] greater than O(1) to still be usable even with extremely high n-values.


As defined in this class: A hashing function h assigns memory location h(k) to the piece of data k.

The ultimate goal would be to have one-to-one and onto mapping, which would result in a list that is entirely automatically sorted, which would eliminate the need for both sorting and searching algorithms.
Realistically, it will have only one output for each input, but it will have multiple inputs for each output. This is imperfect, but it does mean that the sorting and/or searching algorithms will be used with smaller values of n than they otherwise would, reducing the costliness of their complexity.

Two inputs being mapped to the same output is referred to as a "collision."
There are a variety of ways to handle collisions, depending on the applications in use.
In programming, each hash location would have an ArrayList, so if a collision occurs then the two inputs would just be together in that ArrayList.
Linear probing is one way to handle collision: k will just be mapped to h(k)+1 if h(k) is taken. If h(k)+1 is taken, then h(k)+2, etc. I don't particularly like this because it seemingly handles collisions by causing more collisions. However, if the number of memory locations is equal to the number of inputs, it is not catastrophic, because this still makes linear search vastly more effective than a version without hashing. In cases with relatively small numbers of memory locations and relatively large numbers of inputs, the ArrayList method is definitely better.

The greater the number of memory locations your hashing function allows for, the better the [[Time Complexity]], but the worse the Space Complexity.