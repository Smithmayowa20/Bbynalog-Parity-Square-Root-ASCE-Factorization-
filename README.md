# Bbynalog-Parity-Square-Root-ASCE-Factorization-









BBYNALOG PARITY, SQUARE ROOT & ALLI-SMITH CONTINOUS EXPRESSION FACTORIZATION
by ALLI-SMITH MAYOWA OLAJIDE




ABSTRACT
In this paper we implement Parity, Square root and Alli-Smith Expression(A.S.E) systems – for polynomial factorization of a semi-prime number into its component prime numbers, we make use of easily summable/integratable multi-variable polynomial equations to achieve this objective. The time complexity for this new method to find a prime factor of a co-prime number is O(log n), We also utilize this method to solve for integer solutions to several Diophantine Equations.





OUTLINE:
1). Introduction
2). Parity Factorization
3). Alli-Smith Continous Expression Factorization(A.S.C.E)
4). Square Root Method
5). Logarithmic Function Method
6). Conclusion
7). Acknowledgement




INTRODUCTION






























PARITY FACTORIZATION


M = 2^(f (x y - d))
Sum[M,{x,2,M},{y,M + 1,d}]
Where;
d is the semi-prime number to be factored,
f is a large number to reduce the size of the fractional values which are the output of 2^(-k) when (x y - d) is negative.
M is Floor[Sqrt[d]]

We can detect the if there are co-factors for the semi-prime d in the x and y sum intervals by checking the parity of the total sum, if the total sum is even then there is no factor of the semi-prime d in that interval but if it is odd then there is a factor of d in that interval, this is because the result of all positive integer values of k in 2^k are even and 2^0 is 1 which is odd, and the sum of N even number is even but the sum of (N - 1) even number plus an odd number is odd.

Sum[M,{x,2,M},{y,M + 1,d}] = Sum[2^(N())/(2^(f y) - 1),{y,M+1,d}]














ALLI-SMITH CONTINOUS EXPRESSION FACTORIZATION(A.S.C.E)






























SQUARE ROOT METHOD


Let Expression_1 = Sqrt[ (f (x y – d)^2)^2 + 1],

Where;

d is a semi-prime number
f is 10^a and a is a large number that is at least Log_10(d * d)


Let S_ =  Series[Sqrt[m^2 + 1], {x, Infinity, 1}],

Where;

m = (f (x y – d)^2)
S_ = m 

Expression_2 = m


Let S.R.M = Sum[Expression_1, {x, 1, d}, {y, 1, d}] – Sum[Expression_2, {x, 1, d}, {y, 1, d}])

S.R.M is the total number of integer factor multiplicative combinations (x * y) that equal d. 

S.R.M/2 is the total number of unique integer factor multiplicative combinations (x * y = y * x) that equal d.




LOGARITHMIC FUNCTION METHOD


Let Expression 1 = Log[ f (x y - d)^2 + 2]
Let Expression 2 = Log[ f (x y - d)^2 + 3]

Where;
d is a semi-prime number.
f = 10^a and a is a large number that is at least Log_10(d * d).

Let L.F.M = (Sum[Expression_1, {x, 1, d}, {y, 1, d}] – Sum[Expression_2, {x, 1, d}, {y, 1, d}])/(Log[2] - Log[3])

L.F.M is the total number of integer factor multiplicative combinations (x * y) that equal d. 

L.F.M/2 is the total number of unique integer factor multiplicative combinations (x * y = y * x) that equal d.

This method exploits the fact that the difference in a unit interval of the logarithm function of x is far larger at small x values compared to the difference in a unit interval at large x values;
‎
i.e 
Log[(x=0) + 2] - Log[(x=0) + 3] > (10^Inf) (Log[(x=Inf) + 2] - Log[(x=Inf) + 3])
‎
because 
Log[(x=Inf) + 2] - Log[(x=Inf) + 3]) = 0





CONCLUSION






























ACKNOWLEDGEMENT
I would like to thank, appreciate, revere, and worship Lord God Almighty, for helping me with the knowledge and guidance for this research paper. Without whom I could not even lift a pen to paper, thoughtless of forming and expressing my thoughts via words.