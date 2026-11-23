# BBYNALOG PARITY, SQUARE ROOT & ALLI-SMITH CONTINOUS EXPRESSION FACTORIZATION
by ALLI-SMITH MAYOWA OLAJIDE




## ABSTRACT
In this paper we implement Parity, Square root and Alli-Smith Expression(A.S.E) systems – for polynomial factorization of a semi-prime number into its component prime numbers, we make use of easily summable/integratable multi-variable polynomial equations to achieve this objective. The time complexity for this new method to find a prime factor of a co-prime number is O(log n), We also utilize this method to solve for integer solutions to several Diophantine Equations.





### OUTLINE:
1). Introduction
2). Parity Factorization
3). Alli-Smith Continous Expression Factorization(A.S.C.E)
4). Square Root Method
5). Logarithmic Function Method
6). Conclusion
7). Acknowledgement


<br>
<br>
<br>

## INTRODUCTION


























<br>
<br>
<br>



## PARITY FACTORIZATION


M = 2^(f (x y - d))
Sum[M,{x,2,M},{y,M + 1,d}]
Where;
d is the semi-prime number to be factored,
f is a large number to reduce the size of the fractional values which are the output of 2^(-k) when (x y - d) is negative.
M is Floor[Sqrt[d]]

We can detect the if there are co-factors for the semi-prime d in the x and y sum intervals by checking the parity of the total sum, if the total sum is even then there is no factor of the semi-prime d in that interval but if it is odd then there is a factor of d in that interval, this is because the result of all positive integer values of k in 2^k are even and 2^0 is 1 which is odd, and the sum of N even number is even but the sum of (N - 1) even number plus an odd number is odd.

Sum[M,{x,2,M},{y,M + 1,d}] = Sum[2^(N())/(2^(f y) - 1),{y,M+1,d}]












<br>
<br>
<br>


## ALLI-SMITH CONTINOUS EXPRESSION FACTORIZATION(A.S.C.E)



M = Sin[(x + 1)/2 + Pi/2] E^-(5 * 10^6 F(x))^2
‎<br>

‎Let F(x) is the sum of 6 filter sine sums;
‎<br>

‎F1(x) + F2(x) + F3(x) + F4(x) + F5(x) + F6(x)
‎<br>

‎Where;
‎<br>

‎F1(x) = Sum[Sin^2[Pi 10^k x^(1/4)],{k,0,442}]
‎<br>

‎F2(x) = Sum[Sin^2[Pi 10^k x^(2/4)],{k,0,288}]
‎‎<br>

‎F3(x) = Sum[Sin^2[Pi 10^k x^(3/4)],{k,0,138}]
‎‎<br>

‎F4(x) = Sum[Sin^2[Pi 10^k d/x^(1/4)],{k,0,438}]
‎‎<br>

‎F5(x) = Sum[Sin^2[Pi 10^k d^2/x^(2/4)],{k,0,288}]
‎‎<br>

‎F6(x) = Sum[Sin^2[Pi 10^k d^3/x^(3/4)],{k,0,138}]
‎‎<br>

‎and d is a 300 digit semi-prime number.
‎‎<br>

Cosindering the filter F(x), the number of x from 10^600 to 10^604 that have values lesser than 10^(-5) can be calculated thus;
<br>




Consider the unnormalized six-filter function

[
F(x)=F_1(x)+F_2(x)+F_3(x)+F_4(x)+F_5(x)+F_6(x),
]

where

[
F_1(x)=\sum_{k=0}^{442}\sin^2\left(\pi 10^k x^{1/4}\right),
]

and the other five filters are nonnegative as well.

We consider integer x in

[
10^{600}\le x\le10^{604}.
]

1. The condition F(x)<10^{-5}

Since every term in every filter is nonnegative,

[
F(x)<10^{-5}
]

implies in particular

[
F_1(x)<10^{-5}.
]

Because F_1 is a sum of nonnegative terms, every individual term must satisfy

[
\sin^2\left(\pi10^{442}x^{1/4}\right)<10^{-5}.
]

Therefore

[
\left|\sin\left(\pi10^{442}x^{1/4}\right)\right|
<10^{-5/2}.
]

Define

[
\epsilon

\frac{\arcsin(10^{-5/2})}{\pi}.
]

Numerically,

[
\boxed{
\epsilon

1.0065859197\times10^{-3}.
}
]

Hence

[
\left|10^{442}x^{1/4}\right|<\epsilon,
]

where |y| denotes the distance from y to the nearest integer.

Dividing by 10^{442},

[
\boxed{
\left|x^{1/4}\right|
<
1.0065859197\times10^{-445}.
}
]

---

2. x must lie extremely close to a fourth power

Write

[
x^{1/4}=n+\delta,
]

where n is an integer and

[
|\delta|
<
1.0065859197\times10^{-445}.
]

Then

[
x=(n+\delta)^4.
]

Expanding,

[
(n+\delta)^4

n^4+4n^3\delta+6n^2\delta^2
+4n\delta^3+\delta^4.
]

Thus

[
|x-n^4|
\le
4n^3|\delta|
+6n^2|\delta|^2
+4n|\delta|^3
+|\delta|^4.
]

The relevant fourth-power centers satisfy

[
10^{150}\le n\le10^{151},
]

because

[
10^{600}\le n^4\le10^{604}.
]

The dominant term in the width is therefore

[
R

4(10^{151})^3
(1.0065859197\times10^{-445}).
]

Hence

[
\boxed{
R\approx4.026343679\times10^8.
}
]

So the F_1 condition alone permits approximately

[
2R+1
]

integer values of x around each admissible fourth-power center.

Therefore

[
\boxed{
2R+1
\approx8.05268736\times10^8.
}
]

Thus the 10^8 figure is the approximate number of possible integer x's in the F_1-neighborhood of one fourth-power center.

---

3. The reciprocal filter restricts the fourth-power centers

The fourth filter is

[
F_4(x)

\sum_{k=0}^{438}
\sin^2\left(
\pi10^{k+300}x^{-1/4}
\right).
]

For x^{1/4}\approx n, this becomes a condition on

[
\frac{10^{300}}{n}.
]

The extremely small tolerance enforced by F_4 forces n to divide 10^{300}.

Therefore the relevant centers satisfy

[
n\mid10^{300},
]

with

[
10^{150}\le n\le10^{151}.
]

Since

[
10^{300}=2^{300}5^{300},
]

every positive divisor has the form

[
n=2^a5^b,
\qquad
0\le a,b\le300.
]

Counting those satisfying

[
10^{150}\le2^a5^b\le10^{151}
]

gives exactly

[
\boxed{432}
]

admissible divisor centers.

---

4. Total candidate upper bound

For each of the 432 admissible centers, the F_1 condition permits at most approximately

[
8.05268736\times10^8
]

integer values of x.

Consequently,

[
N
<
432(8.05268736\times10^8).
]

Therefore

[
\boxed{
N<3.47876\times10^{11}.
}
]

This is a candidate upper bound obtained from the F_1 neighborhood width and the 432 possible divisor centers.

---

5. Important distinction

The quantity

[
\boxed{10^8}
]

is not the final number of integers x satisfying all six filters.

It is approximately the number of integer x's allowed by the F_1 condition around one admissible fourth-power center.

The resulting bounds are therefore

[
\boxed{
\text{per-center width}\approx8.05\times10^8
}
]

and

[
\boxed{
\text{432 centers}\quad\Longrightarrow\quad
N<3.48\times10^{11}.
}
]

The other filters F_2,F_3,F_5,F_6 impose additional restrictions, so the actual number of six-filter survivors can be substantially smaller.

Thus 3.48\times10^{11} should be regarded as a conservative candidate upper bound, not as the exact count.


‎Sum[M,{x,10^600,10^604}]


























<br>
<br>
<br>


## SQUARE ROOT METHOD


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


<br>
<br>
<br>

## LOGARITHMIC FUNCTION METHOD


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


<br>
<br>
<br>


## CONCLUSION




























<br>
<br>
<br>

## ACKNOWLEDGEMENT
I would like to thank, appreciate, revere, and worship Lord God Almighty, for helping me with the knowledge and guidance for this research paper. Without whom I could not even lift a pen to paper, thoughtless of forming and expressing my thoughts via words.