
In [[C]] there are three pools of memory:
Static storage: global and static variable storage, used for the entire run of the program.

The Stack: local variable storage and parameters and return addresses. Referred to in C as the "stack frame."

The Heap: [[Dynamic Memory Allocation]] or malloc: Data sits there until it is de-allocated.

When working in C, you need to know where you're storing each thing or shit hits the fan.

A program's address space contains four regions:
The stack: local variables, starts at high values and grows downwards, other data will be freed up for it as needed, within technical restraints.
The heap: space requested via `malloc`, below the stack, resized dynamically and grows upwards.
Static data: Initialized/uninitialized static and global variables, takes up the values directly below the Heap. Initialized takes up the low values of static, uninitialized takes the high values.
The Code/Text: Loaded upon program start, does not change. Takes up the lowest values.

Old architecture had the stack on the bottom at a predefined address, growing down, followed by the code and static, with the heap above the static growing up.