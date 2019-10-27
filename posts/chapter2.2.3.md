---
layout: post
title: Problem Set 2.2 - Part 3
date: 2019-10-23
---
## Problem 21
Find the pivots and the solution for both systems
($A\boldsymbol{x}=\boldsymbol{b}$ and $K\boldsymbol{x}=\boldsymbol{b}$):

$
\begin{aligned}
2x+\hphantom{2}y\hphantom{+2z+2t} &=0 \\
\hphantom{2}x+2y+\hphantom{2}z\hphantom{+2t} &=0 \\
\hphantom{2x+2}y+2z+\hphantom{2}t &=0 \\
\hphantom{2x+2y+2}z+2t &=5
\end{aligned}
\qquad
\begin{aligned}
2x-\hphantom{2}y\hphantom{+2z+2t} &=0 \\
-x+2y-z\hphantom{+2t} &=0 \\
\hphantom{2x+2}-y+2z-t &=0 \\
\hphantom{2x+2y2}-z+2t &=5
\end{aligned}
$

## Solution 21
$
\begin{aligned}
A = &
\left[ \begin{array}{cccc|c}
2 & 1 & 0 & 0 & 0 \\
1 & 2 & 1 & 0 & 0 \\
0 & 1 & 2 & 1 & 0 \\
0 & 0 & 1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_2 = 2R_2 - R_1}&
\left[ \begin{array}{cccc|c}
2 & 1 & 0 & 0 & 0 \\
0 & 3 & 2 & 0 & 0 \\
0 & 1 & 2 & 1 & 0 \\
0 & 0 & 1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_3 = 3R_3 - R_2}&
\left[ \begin{array}{cccc|c}
2 & 1 & 0 & 0 & 0 \\
0 & 3 & 2 & 0 & 0 \\
0 & 0 & 4 & 3 & 0 \\
0 & 0 & 1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_4 = 4R_4 - R_3}&
\left[ \begin{array}{cccc|c}
\boxed{2} & 1 & 0 & 0 & 0 \\
0 & \boxed{3} & 2 & 0 & 0 \\
0 & 0 & \boxed{4} & 3 & 0 \\
0 & 0 & 0 & \boxed{5} & 20
\end{array} \right]
=U\longrightarrow
\begin{aligned}
\boxed{t=4} \\
\boxed{z=-3} \\
\boxed{y=2} \\
\boxed{x=-1} \\
\end{aligned}
\end{aligned}
$

$
\begin{aligned}
K = &
\left[ \begin{array}{rrrr|c}
2 & -1 & 0 & 0 & 0 \\
-1 & 2 & -1 & 0 & 0 \\
0 & -1 & 2 & -1 & 0 \\
0 & 0 & -1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_2 = 2R_2 + R_1}&
\left[ \begin{array}{rrrr|c}
2 & -1 & 0 & 0 & 0 \\
0 & 3 & -2 & 0 & 0 \\
0 & -1 & 2 & -1 & 0 \\
0 & 0 & -1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_3 = 3R_3 + R_2}&
\left[ \begin{array}{rrrr|c}
2 & -1 & 0 & 0 & 0 \\
0 & 3 & -2 & 0 & 0 \\
0 & 0 & 4 & -3 & 0 \\
0 & 0 & -1 & 2 & 5
\end{array} \right] \\
\xrightarrow{R_4 = 4R_4 + R_3}&
\left[ \begin{array}{rrrr|c}
\boxed{2} & -1 & 0 & 0 & 0 \\
0 & \boxed{3} & -2 & 0 & 0 \\
0 & 0 & \boxed{4} & -3 & 0 \\
0 & 0 & 0 & \boxed{5} & 20
\end{array} \right]
=U\longrightarrow
\begin{aligned}
\boxed{t=4} \\
\boxed{z=3} \\
\boxed{y=2} \\
\boxed{x=1} \\
\end{aligned}
\end{aligned}
$

::: warning
In the solutions manual, Strang reports that the pivots should be
$2,\frac{3}{2},\frac{4}{3},\frac{5}{4}$. The bottom right cell of Strang's
matrix is $5$ instead of my $20$, so our solutions are the same.
I do not yet know if the distinction between Strang's pivots and mine is important.
:::

## Problem 22
If you extend Problem 21 following the $1,2,1$ pattern or the $-1,2,-1$ pattern,
what is the fifth pivot? What is the $n$th pivot? ("$K$ is my favorite matrix" --
Strang")

## Solution 22
Using my pivots, the fifth pivot is $5$ and the $n$th pivot is $n$. Using
Strang's, they would be $\frac{6}{5}$ and $\frac{n+1}{n}$.

::: note
I wonder why Strang likes this matrix so much. He even has it in cupcake form!
![cupcakes](http://www-math.mit.edu/~gs/PIX/cupcakematrix.jpg)
:::

## Problem 23
If elimination leads to $x+y=1$ and $2y=3$, find three possible original
problems.

## Solution 23
Clearly, $x+y=1$ and $2y=3$ are possible original equations.

Suppose the $x$ coefficient in the second equation was originally $1$. Then, the
elimination would subtracted one copy of the first equation, so it must have
originated as $x+3y=4$. Similarly, if the $x$ coefficient in the second equation
was originally $2$, elimination would have subtracted two copies of the first
equation, so we must have started with $2x+4y=5$.

## Problem 24
For which two numbers $a$ will elimination fail on $
A=
\left[\begin{smallmatrix}
a & 2 \\ a & a\end{smallmatrix}\right]
$?

## Solution 24
Elimination fails if $a=2$ because both rows will be identical, and if $a=0$ because there will be no second
pivot.

## Problem 25
For which three numbers $a$ will elimination fail to give three pivots?

$
A=\begin{bmatrix}
a & 2 & 3 \\
a & a & 4 \\
a & a & a
\end{bmatrix}
$ is singular for which three values of $a$?

## Solution 25
$A$ is singular if $a=0$ because there is no third pivot.

$A$ is singular if $a=2$ because the first two columns are identical.

$A$ is singular if $a=4$ because the bottom two rows are identical.

## Problem 26
Look for a matrix
$\left[\begin{smallmatrix}
a & b \\ c & d\end{smallmatrix}\right]$
that has row sums $4$ and $8$, and column sums $2$ and $s$.

$
\begin{aligned}
a + b &= 4 \\
c + d &= 8 \\
a + c &= 2 \\
b + d &= s
\end{aligned}
$

The four equations are solvable only if $s$ = ?
Then, find two different matrices that have the correct row and column sums.
Write down the 4 by 4 system $A\boldsymbol{x}=\boldsymbol{b}$ with
$\boldsymbol{x}=(a,b,c,d)$ and make $A$ triangular by elimination.

## Solution 26
Let's make a 4x4 matrix whose columns represent $a,b,c,d$ and the right hand
side is the sum of each pair of variables as described above.

$
\begin{aligned}
A=&
\left[ \begin{array}{cccc|c}
1 & 1 & 0 & 0 & 4 \\
0 & 0 & 1 & 1 & 8 \\
1 & 0 & 1 & 0 & 2 \\
0 & 1 & 0 & 1 & s
\end{array} \right] \\
\xrightarrow{R_2\leftrightarrow R_3}&
\left[ \begin{array}{cccc|c}
1 & 1 & 0 & 0 & 4 \\
1 & 0 & 1 & 0 & 2 \\
0 & 0 & 1 & 1 & 8 \\
0 & 1 & 0 & 1 & s
\end{array} \right] \\
\xrightarrow{R_2=R_2-R_1}&
\left[ \begin{array}{cccc|c}
1 & 1 & 0 & 0 & 4 \\
0 & -1 & 1 & 0 & -2 \\
0 & 0 & 1 & 1 & 8 \\
0 & 1 & 0 & 1 & s
\end{array} \right] \\
\xrightarrow{R_4=R_4+R_2}&
\left[ \begin{array}{cccc|c}
1 & 1 & 0 & 0 & 4 \\
0 & -1 & 1 & 0 & -2 \\
0 & 0 & 1 & 1 & 8 \\
0 & 0 & 1 & 1 & s-2
\end{array} \right] \\
\xrightarrow{R_4=R_4-R_3}&
\left[ \begin{array}{cccc|c}
1 & 1 & 0 & 0 & 4 \\
0 & -1 & 1 & 0 & -2 \\
0 & 0 & 1 & 1 & 8 \\
0 & 0 & 0 & 0 & s-10
\end{array} \right]=U
\end{aligned}
$

We can see that there can only be a solution if $s=10$.
To find solution matrices, assume a value for $d$ and then infer the other
values. For example, if $d=0$ then $c=8$ and $b=10$ and $a=-6$.

$
\begin{bmatrix}
-2 & 6 \\
8 & 0
\end{bmatrix}
$

Another example matrix where $d=1$:

$
\begin{bmatrix}
-5 & 9 \\
7 & 1
\end{bmatrix}
$


