
The basic purpose of a CPU is to execute instructions, which are simple operations that are built-in to the CPU.

Different CPUs implement different sets of instructions, the set is referred to as the "Instruction Set Architecture" or ISA.

Early in computing, the idea was to add more and more instructions to ISAs, to make CPUs more capable. This is the CISC philosophy: Complex Instruction Set Computer.
However, as the complexity and quantity of CPU instructions increased, inefficiencies were revealed: More complex instructions would consume more power and produce more heat. The tiny surface area of CPUs made dissipating the heat exponentially more difficult, and the amount of power simply became impractical.

Moore's Law: Every two years, CPU speed doubles. It was followed for quite some time, but eventually things began to plateau due to heat and power restrictions.

Alternatively, there is RISC, Reduced Instruction Set Computing.
A small and efficient instruction set, with the capability to run massive amounts of those instructions at massive speeds, enables similar speeds without the same heat and power requirements.

MIPS is a semiconductor company that pioneered RISC architecture.

In MIPS Assembly, there are 32 registers(0-31), each of which is 32 bits large. 32 Bits, or four Bytes, is called a Word in assembly(hence the "load word," "save word," etc instructions).

Registers are also given a name: $16-$23 are $s0 - $s7, called the "save" registers.
$8 - $15 are $t0 - $t7
$24 - $25 are $t8 - $t9
Do I get why this is? Nope but I'm not gonna worry about that yet.

In higher-level languages like [[C]], variables are declared first and given a type, such as int or char.
Variables are then locked into being that specific data type, with the exception of casting.
Registers do not follow this rule, they are plain spaces for binary data to be stored in, regardless of type.
The instructions which are called to operate on a register will then decide how to handle the data.