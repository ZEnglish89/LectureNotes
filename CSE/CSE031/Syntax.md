
Compiling:
`gcc [filename].c -o [executablename]`
On linux, the executable will be a `.out` file, on windows it'll be `.exe`
The default name for the executable, if not specified, will simply be "a"
Print is "printf()"

To get the main function to accept arguments, declare it as follows:
`int main(int argc, char *argv[])`
argc is the number of strings on the command line, meaning the number of arguments passed in. Argc DOES count the ./app string, so `./sort myfile` will have `argc==2`

argv is a pointer to an array which contains the arguments as strings. This ALSO counts the ./app string, `argv[0]=="./app"`(or whatever your filename is, of course)
argc and argv are subject to the .length vs index disconnect, so when `argc==1`, `argv[]` will stop at index 0, not 1

Decimal numbers will be assumed as doubles, unless specified as floats by ending the number with f.
`1.2` is a double
`1.2f` is a float


`%d` is a format specifier specifying that whatever comes next will be printed as an integer
`%s` is the same but for strings
`%f` for floats
`%7.4f` or similar things specify how many digits you want the float to be printed to. 7.4 means 7 digits before the decimal and four beyond it. Extra/unnecessary digits will be filled in with 0s at the end to the right of the decimal point, but will be simply removed to the left of the point.

Every data type has its own specifier like this, they can easily be googled
When printing, the `%d` and `%s` statements will be replaced in order from left to right by the corresponding other arguments in the print statement, formatted appropriately for their types.
`printf("this is %s print statement, I am number %d","my",1)` would print "this is my print statement, I am number 1"
Format specifiers are trusted by the system, booleans will print 0 or 1 when you tell the computer that they're integers.

All objects or variables have a size, given by the `sizeof([variablename])` function

`-w` suppresses compile-time warnings

& returns the address of whatever variable it precedes.
`int x = 3;` allocates a memory location and stores 3 as its value. 
`int * p = &x;` creates a [[Pointer]] which is equal to the address for that memory location.
p = &x, * p = x = 3
Use the asterisk to declare pointers, and then preceding the pointer with another asterisk will dereference it, causing the computer to read the value(according to the pointer's data type) rather than the address.

`int *p;` makes a pointer of type int.
`int **p;` makes a pointer of type (pointer of type int).
This can be repeated ad infinitum.

The `typedef` variable allows you to create aliases for existing data types.
`typedef int anIntegerVariable` will now treat "anIntegerVariable" as being the same as "int," treating it as the same keyword.
You can also wrap a [[Struct]] with it:
`typedef struct myStruct` and then follow the end bracket of the struct with the new name.
If you don't rename a struct, you need to reference it as `struct Name` including the word struct every time.

`struct __attribute__((__packed__))` will "crush" the [[Struct]], removing the data padding. This is good for space efficiency, but will likely cause errors and reduce CPU efficiency.

`strcopy(a,b)` will copy the contents of string b onto string a.

For [[Dynamic Memory Allocation]], `free(ptr)` will free the memory which ptr is pointing to, allowing it to be used otherwise, without deleting ptr.