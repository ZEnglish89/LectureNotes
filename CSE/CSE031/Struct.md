
Allow user-defined data types, just like in C++

Declaring a structure does not allocate any memory, memory is only allocated when you create an instance of that structure.

The size of a struct is dependent on the order the component variables are declared in. If they are declared in an inefficient order, there will be padding of extra memory between them(Research "Data Structure Alignment").
Your RAM/CPU wants your Struct to be a multiple of 4 bytes, it will add padding to ensure that happens. If you have a struct which actually IS a multiple of 4 bytes, and it is declared in descending order of variable size, there will be no padding.
As a general rule, declaring the variables in descending order of size will be most efficient.
At minimum, the size of a struct will be the sum of the sizes of its component parts.

The "packed" keyword(see [[Syntax]]) will remove the padding from your struct(called "crushing" it), which will make it more space-efficient, but will cause problems with your Alignment, potentially breaking things and making your CPU less efficient.

User defined data types are the same as primitive data types, so if you declare a struct p and then declare a new struct q as q=p, q will become a copy of p, and changing q will not change p. They operate on pass by value, not pass by reference.
If you build a large struct, keep in mind that every time you pass it anywhere you'll be making a copy, which will strain your system. Consider passing by reference and using pointers.


Renaming structs using `typedef`(see [[Syntax]]) is extremely useful, it removes the need to include the word "struct" when you reference the data type in the future.
You can also use `typedef` to rename pointers! So if you have a `Node` struct, you can rename `Node*` to `List`, so now you can declare new linkedlists quicker and easier.
`char*` can become `String`, etc!

Using [[Dynamic Memory Allocation]] on a struct will allocate space for one iteration of your struct, one of each variable contained within it.