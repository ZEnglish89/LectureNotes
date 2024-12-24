
Memory addresses are written in unsigned hexadecimal, and are typically very large.

The smallest addressable value in RAM is a byte. Individual bits can be accessed, but they will not have memory addresses.
As such, addresses increment by four, because each bit still matters, but only bytes, which occur every four bits, are addressed.

Memory can be thought of as one huge array, where each byte is an item in the array. Under this metaphor, the memory address of an item or byte is the index of that array which the item or byte can be found at.

The VALUE is the item which is stored at a particular memory address, the address is the representation of the location. This distinction is crucial.

Pointers are a data type which stores a memory address, meaning that the pointer "points" to the memory location which the address corresponds to. In practice, pointers are unsigned longs, they simply tell the computer to read the long as an address.
When you call a pointer directly, it refers to the memory address. If you **dereference** a pointer, it will instead read out the value stored at the corresponding memory location.
The type of pointer(int, char, etc) will tell the computer what data type it should read the value as (the number 60 vs the ASCII code 60, for example).

& returns the address of whatever variable it precedes.
`int x = 3;` allocates a memory location and stores 3 as its value. 
`int * p = &x;` creates a pointer which is equal to the address for that memory location.
p = &x, * p = x = 3
Use the asterisk to declare pointers, and then preceding the pointer with another asterisk will dereference it, causing the computer to read/write the value(according to the pointer's data type) rather than the address.

void pointers can point to any data type, they simply must be casted to a pointer of a specific type when they are dereferenced.
All pointer types can be casted to types other than they were declared as, but the compiler will throw a warning first.

When first declared, pointers will point to nonsense. Sometimes this is "nil," sometimes this is a random value, it's an unpredictable mess. Your options are to: point it to an existing object, or allocate new memory for it to point to. 
You can manually set a pointer to store an address, like `int *p=1000;` but there isn't really a reason to do so, and odds are you won't be able to dereference it. 1000 specifically you cannot dereference because that address is reserved by the operating system and not accessible by the user. If you specify an address that you actually have access to, you can use it, but again, there's just no point to doing this. In effect, you've just created an unsigned long in hex, not a pointer.

Creating a pointer to an address does NOT allocate the memory at that space, it only allocates the space for the address to be held in(the pointer itself)
The pointer and the memory it's pointing to are TWO SEPARATE THINGS, the pointer itself has an address.
`int x = 3;`
`int *p=&x;`
`int **j=&p;`
Will make p a pointer of type int which contains the address of x, which contains a value of 3.
j will be a pointer of type (pointer of type int) which contains the address of p, which contains a value of (the address of x, which contains a value of 3).

`&p` will give you the address at which p is being stored.
Because arrays are read-only, if c is an array, `&c==c` and there is no way to access the address at which c is stored.