
"Data Multiplexor"

A system which takes in a number of inputs as well as a [[Control Signal]]. One of the inputs will be outputted, and which one that is will be determined by the control signal.
Most commonly it'll just be picking between two inputs, so A and B, where the CS is a single bit. So if the CS = 0, A will be output, and B will be output if CS = 1.

If there are four inputs, you need a two-bit control signal: 00, 01, 10, 11

These are used extremely commonly to make decisions within a circuit.

On diagrams, they're written as trapezoids.

Cannot be set to allow nothing through or everything through, they must choose exactly one of their options. In some cases, like with the Write Muxes, they can pass nothing through, but they must sacrifice one of their options in order to make "nothing" a choice.