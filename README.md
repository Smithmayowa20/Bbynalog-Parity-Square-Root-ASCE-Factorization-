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



M = E^(I x) E^-(5 * 10^6 F(x))^2
‎<br>

‎Let F(x) is the sum of 6 filter sine sums;
‎<br>

‎F1[x] + F2[x] + F3[x] + F4[x] + F5[x] + F6[x]
‎<br>

‎Where;
‎<br>

‎F1[x] = Sum[Sin^2[Pi 10^k x^(1/4)],{k,0,442}]
‎<br>

‎F2[x] = Sum[Sin^2[Pi 10^k x^(2/4)],{k,0,288}]
‎‎<br>

‎F3[x] = Sum[Sin^2[Pi 10^k x^(3/4)],{k,0,138}]
‎‎<br>

‎F4[x] = Sum[Sin^2[Pi 10^k d/x^(1/4)],{k,0,438}]
‎‎<br>

‎F5[x] = Sum[Sin^2[Pi 10^k d^2/x^(2/4)],{k,0,288}]
‎‎<br>

‎F6[x] = Sum[Sin^2[Pi 10^k d^3/x^(3/4)],{k,0,138}]
‎‎<br>

‎and d is a 300 digit semi-prime number.
‎‎<br>

Cosindering the filter F(x), the number of x from 10^600 to 10^604 that have values lesser than 10^(-5) for a random 300 digit d can be calculated thus;
<br>
<br>
<br>



1. Consequence of "F[x] < 10^-5"

If

F[x] < 10^-5

then necessarily

F1[x] < 10^-5.

Since every term in "F1" is nonnegative,

Sin[Pi*10^442*x^(1/4)]^2 < 10^-5

and hence

Abs[Sin[Pi*10^442*x^(1/4)]] < 10^(-5/2).

Define

epsilon = ArcSin[10^(-5/2)]/Pi;

Then

N[epsilon, 30]

gives

0.00100658591973769

Therefore

Abs[
    10^442*x^(1/4) -
    Round[10^442*x^(1/4)]
] < epsilon

and consequently, for some integer "n",

Abs[x^(1/4) - n] < epsilon/10^442;

Define

deltaMax = epsilon/10^442;

so that

N[deltaMax, 20]

gives

1.00658591973769*10^-445

Thus

Abs[x^(1/4) - n] <
    1.00658591973769*10^-445.

---

2. Convert the fourth-root condition into an x-width

Write

x^(1/4) = n + delta

with

Abs[delta] < deltaMax;

Then

x = (n + delta)^4

and

(n + delta)^4 - n^4 ==
    4*n^3*delta +
    6*n^2*delta^2 +
    4*n*delta^3 +
    delta^4;

Therefore

Abs[x - n^4] <=
    4*n^3*deltaMax +
    6*n^2*deltaMax^2 +
    4*n*deltaMax^3 +
    deltaMax^4;

Because

10^600 <= x <= 10^604

the fourth-power centers satisfy approximately

10^150 <= n <= 10^151;

Using the largest possible center,

nMax = 10^151;

gives the conservative radius

R =
    4*nMax^3*deltaMax +
    6*nMax^2*deltaMax^2 +
    4*nMax*deltaMax^3 +
    deltaMax^4;

Numerically,

N[R, 30]

gives approximately

4.026343679*10^8

Thus the number of possible integer "x" values around one fourth-power center is bounded by

perCenterBound =
    2*Floor[R] + 1;

or approximately

8.05268736*10^8

Hence

perCenterBound ~ 8.05*10^8.


---

3. The role of the random 300-digit "d"

The fourth filter is now

F4[x_] :=
    Sum[
        Sin[Pi*10^k*d*x^(-1/4)]^2,
        {k, 0, 438}
    ];

Near a fourth-power center,

x^(1/4) ~ n,

so the argument of the sine is approximately

Pi*10^k*d/n.

The high-k terms force

d/n

to be extremely close to an integer at the corresponding decimal scales.

Under the sufficiently tight simultaneous tolerance supplied by the filter, the relevant centers are therefore associated with divisors of "d":

n | d

with

10^150 <= n <= 10^151.

Define the number of relevant divisor centers by

divisorCenters =
    Select[
        Divisors[d],
        10^150 <= # <= 10^151 &
    ];

and

D = Length[divisorCenters];

Thus

D =
    Number of divisors n of d
    satisfying 10^150 <= n <= 10^151.


The value of "D" depends on the prime factorization of the particular 300-digit integer "d".

---

4. Candidate upper bound for arbitrary "d"

The conservative candidate count is

candidateBound =
    D*(2*Floor[R] + 1);

Since

2*Floor[R] + 1 ~ 8.05268736*10^8,

we obtain

candidateBound ~
    8.05268736*10^8*D.

Therefore,

N[candidateBound, 20]

is approximately

8.05268736*10^8*D

where

D = Length[
    Select[
        Divisors[d],
        10^150 <= # <= 10^151 &
    ]
];

---

5. General result

For an arbitrary 300-digit integer "d",

10^299 <= d < 10^300

the argument gives

F[x] < 10^-5

implies

x^(1/4)

is within approximately

1.00658591973769*10^-445

of an integer.

Consequently, around each admissible fourth-power center, there are at most approximately

8.05268736*10^8

integer candidates.

If

D =
    Length[
        Select[
            Divisors[d],
            10^150 <= # <= 10^151 &
        ]
    ];

then the conservative global candidate bound is

candidateBound =
    D*(2*Floor[R] + 1);

or approximately

candidateBound ~
    8.05268736*10^8*D.

Thus the general scaling is

Ncandidate[d] <
    8.05268736*10^8 *
    NumberOfRelevantDivisors[d].

The important distinction is that

8.05268736*10^8

is the per-center neighborhood size, whereas

D

depends on the particular 300-digit integer "d".


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