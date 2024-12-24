Detect errors in strings of digits by adding an extra digit at the end, which is evaluated using a function. If the final digit is wrong, then the rest of the string can be assumed to also be wrong.

For bar code scans(Universal Product Codes), the final digit will be calculated so that the sum of all the digits in the bar code ends in a 0. That way, if the scanner returns a string where 
"sum of string"(not congruent) 0 (mod 10), then that means the scanner made an error of some kind.
![[Pasted image 20231108170602.png]]
Apparently, research has determined that this specific function, with those coefficients, is optimal. I do not fully understand why, but it's not particularly relevant, just good to know.

Without this system, the scanner would continue to feed the faulty, mis-scanned number into the rest of the system, which could either throw errors elsewhere or charge a customer for the incorrect product, things of that nature.

This is just an example of a practical way to use congruence.