
Memory is sorted into the Stack, the Heap, the Data, and the Text.

Global and Static parts of the code get put in the Text segment, along with the actual machine code for the system.

The Heap is used whenever the "new" keyword(In [[C]] this is instead the "malloc" keyword) is used, that keyword allocates a specific amount of space on the heap. This is capped at whatever the Operating System allows you to use, eventually the OS will refuse to allocate any further and will kill the program instead. Memory which is allocated on the Heap MUST be freed afterwards, it is not freed by default.

The Stack is used by default, and will pull from the RAM until it can no longer handle more. Linking multiple machines can make your stack functionally infinite, hehe.

`malloc(size)` will allocate memory equal to the size you pass in(use `sizeof` heavily) and return a void pointer to the beginning of the allocated memory.

Do your [[Garbage Collection]].
