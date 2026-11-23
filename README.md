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


We have

\[
F(x)=F_1+\cdots+F_6,
\]

with

\[
F_1(x)=\sum_{k=0}^{442}\sin^2(\pi10^kx^{1/4}).
\]

Since every term is nonnegative,

\[
F(x)<10^{-5}
\quad\Longrightarrow\quad
F_1(x)<10^{-5}.
\]

Therefore every individual term satisfies

\[
\sin^2(\pi10^{442}x^{1/4})<10^{-5}.
\]

Hence

\[
\left|\sin(\pi10^{442}x^{1/4})\right|<10^{-5/2}.
\]

Let

\[
\epsilon
=
\frac{\arcsin(10^{-5/2})}{\pi}
=
1.0065859197\times10^{-3}.
\]

Then

\[
\boxed{
\left\|10^{442}x^{1/4}\right\|<\epsilon
}
\]

and therefore

\[
\boxed{
\left\|x^{1/4}\right\|
<
1.0065859197\times10^{-445}.
}
\]

Now write

\[
x^{1/4}=n+\delta,
\qquad |\delta|<1.0065859197\times10^{-445}.
\]

Then

\[
x=(n+\delta)^4.
\]

For small \(\delta\),

\[
(n+\delta)^4-n^4
=
4n^3\delta+6n^2\delta^2+4n\delta^3+\delta^4.
\]

The relevant \(n\)-range is

\[
10^{150}\le n\le10^{151}.
\]

Using the largest \(n=10^{151}\), the leading half-width is

\[
R
=
4(10^{151})^3
(1.0065859197\times10^{-445}),
\]

giving

\[
\boxed{
R\approx4.026343679\times10^8.
}
\]

Thus, around each fourth power \(n^4\), the \(F_1\) condition permits at most approximately

\[
2R+1
\approx
8.05268736\times10^8
\]

integer \(x\)'s.

But the six filters drastically reduce the centers

The reciprocal filter

\[
F_4(x)
=
\sum_{k=0}^{438}
\sin^2\left(\pi10^{k+300}x^{-1/4}\right)
\]

forces \(x^{1/4}\) to be extremely close to a divisor of \(10^{300}\).

For \(d=10^{300}\),

\[
n\mid10^{300}
\]

and

\[
10^{150}\le n\le10^{151}.
\]

There are exactly

\[
\boxed{432}
\]

such divisors.

Therefore the crude \(F_1\)-based candidate bound is

\[
432(2R+1),
\]

so

\[
432(8.05268736\times10^8)
\approx
\boxed{3.47876\times10^{11}}.
\]

So I want to correct one thing from the earlier discussion:

\[
\boxed{\text{\(10^8\) is the approximate width per fourth-power center, not the total six-filter count.}}
\]

The rigorous statement we established is approximately

\[
\boxed{8.05\times10^8\text{ possible integer }x\text{ per admissible divisor center}}
\]

and, with 432 divisor centers,

\[
\boxed{N_{\rm candidates}<3.48\times10^{11}}.
\]

The actual number satisfying all six filters and \(F(x)<10^{-5}\) can be substantially smaller. The \(10^8\) figure by itself is therefore a local neighborhood upper bound, not the final survivor count.


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