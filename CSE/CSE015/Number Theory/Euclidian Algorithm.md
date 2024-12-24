
An [[Algorithm]] used to compute the [[Greatest Common Divisor]] of two numbers; based on the idea that gcd(a,b)=gcd(b,c) when a>b and c = a mod b

In psuedocode:
	procedure gcd(a,b: positive integers)
	x:=a
	y:=b
	while y != 0
		r:= x mod y
		x:= y
		y:= r
	return x
gcd(a,b) is the x which is returned.

The Euclidian Algorithm has [[Time Complexity]] O(log b).