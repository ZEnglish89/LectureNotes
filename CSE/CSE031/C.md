C compilers take C code and convert it into an "architecture specific" machine code, effectively just binary

This is as opposed to languages like Java, which converts to "architecture **in**dependent" bytecode, running on something similar to a virtual machine.

Being converted into machine code makes C extremely efficient, but it also means that the compiled executable is tied to the operating system, and cannot be passed between machines running different systems. The original code must instead be compiled anew for each machine that is running a different operating system or architecture.

Most "functional" programming languages, for example Scheme, interpret the code directly

C is purely a compiled language, Java is a compiled and interpreted language, and Scheme is a purely interpreted language.

The machine itself can ONLY read the machine code, the binary which C is converted into.

The effective difference is WHEN your program is converted to machine instructions.

In languages like C, the compilation process consists of compiling .c files into .o files, then linking those .o files into executables. "Assembling" is done in the background automatically. Once the code is compiled, it is EXTREMELY efficient, because the code is already in the most efficient configuration for the machine to run. Compile time is where the main time loss comes in, but innovations have helped with that. For example, in multi-file programs, recompiling the code will now only recompile files which have been modified since the previous compilation, reducing redundancy. If not for this feature, many programs would be prohibitively inefficient to work with.
The process of recompiling for each new machine and after each round of revisions to a program is slow, but once the product is complete it is more efficient than it would be otherwise.

C does not have object abstraction, data is separate from methods.
C has low-level libraries, many things that would be taken for granted in languages like Python have to be written manually.
Memory management in C is manual, not automatic(and is slightly lower-level than even C++)
C is less memory/RAM-dependent than most other languages.
Arrays in C initialize to "garbage(meaning whatever random items were already stored in that memory, usually it's unintelligible)," not 0, because there is a memory and processing cost to cleaning that memory and initializing it to 0, it is more efficient to leave it as garbage if you do not need it set to 0.
All local variables do not initialize, until they are explicitly defined. They may still contain random data left over from previous operations on the machine. This includes [[Pointer]]s, the memory which they point to does not get initialized, only the memory to store the address being pointed to.

If variables are not manually initialized in C, there is a change that they will hold garbage, like discussed above with arrays.

`0==FALSE`, anything other than 0 evaluates to TRUE
Booleans are NOT included in C by default, they come with the header file `<stdbool.h>`

Decimals will be assumed as doubles unless they are specified as floats. Floats are 4 bytes, doubles are 8 bytes, so the difference is size vs data efficiency.

C compilers are not as helpful as other languages when they throw errors; they aren't great at describing what's wrong and how you can fix it.
The compiler warning you at compile time does not mean the code will not work or an error will be thrown at runtime. Read the warnings, but ignoring them if you decide the warning is not significant to the outcome is absolutely an option. `-w` suppresses the warnings. Only do this if you are absolutely certain the warnings are immaterial.

Numbers will default to be read as integers if they are not specified to be a different type(such as wrapping them in apostrophes to be a char)

"Flow control" or branch code, is very similar to other languages, containing if/else, while, for, switch, etc

All objects or variables have a size, given by the `sizeof([variablename])` function. Sizes are given in the number of bytes that object or variable contains/uses.
`sizeof()` returns a long unsigned integer, not a regular integer, to allow it to still function when used to check the size of extremely large data structures.
Chars are 1 byte.
Ints are 4 bytes.
Longs are 8 bytes.
Arrays of datatypes are `[size of the data type] * [length of the array]`

C allows casting of any type to any other type without checking for its validity.