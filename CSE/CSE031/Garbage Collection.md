If allocated memory([[Dynamic Memory Allocation]]) no longer has a reference to it, it is garbage, and is no longer usable. To avoid generating garbage, `free` pointers before you change them to point to something else, so that you don't abandon memory like that.

Many languages will automatically "collect" your garbage for you. C doesn't care.

Memory can be tracked either recursively or iteratively.

Recursively: find all pointers that are available, then track down to the memory they point to, and find all pointers within that memory, etc. Recursive techniques have the potential to use even more memory in the process of garbage collection. This can be harmful, because they are typically only used when you are already running out of memory.

The iterative method uses "reverse pointers."

Method 1: Reference counting: For every chunk of dynamically allocated memory, keep a count of the number of pointers that are pointing to it. This is handled via assignment operator overloading, and allows garbage collection to be very quick, but has a lot of overhead and decreases the speed of assignments.

Method 2: Mark and Sweep: Continue allocating memory until there is none left, then find what memory you cannot reach. Chunks of memory are like nodes in a tree, and pointers are the edges in that tree. Traverse the tree after all memory is allocated, returning a list of the unreachable nodes. This traversal traditionally uses recursion, but it was already discussed above that recursion is undesirable for this situation. "Reverse pointers," can be used here again.

Method 3: Copying Garbage Collection: Divide memory into two spaces, and only have one in use at any time. When the active space is exhausted, traverse it, copying all objects to the other space, then switch which space is active. Garbage cannot be copied because there is no way to reach it, so it is simply lost in the process and can be written over at a future time. This copying process uses "forwarding pointers" to keep different chunks of memory coordinated.