---
layout: post
title: Problem Set 2.2 - Part 2
date: 2019-10-19
---

**Problems 11-20 study elimination on 3 by 3 systems (and possible failure).**

## Problem 11
A system of linear equations can't have exactly two solutions. Why?
- If $(x,y,z)$ and $(X,Y,Z)$ are two solutions, what is another solution?
- If 25 planes meet at two points, where else do they meet?

## Solution 11
The solution to a system of linear equations must be either: no solution, a single point, or at the very least
a line. It could also be a 3 or higher dimensional space.
- If $(x,y,z)$ and $(X,Y,Z)$ both lie on the same plane, then all other points
on that plane are also solutions. For example, the point halfway between those
two is $(x+X,y+Y,z+Z)$. If they do not lie on the same plane, then all
points in the space must be solution.
- If 25 planes meet at two points, they must also meet at the line that contains
    those two points.
::: note
Remember, an easy way to find a 3rd point on the same plane as 2 other points is
to take the point in the middle of the first two!
:::

## Problem 12
Reduce this system to upper triangular form by two row operations:

$
\begin{aligned}
2x+3y+z&=8\\
4x+7y+5z&=20\\
-2y+2z&=0
\end{aligned}
$

## Solution 12
$
\begin{aligned}
A = &
\left[ \begin{array}{ccc|c}
2 & 3 & 1 & 8 \\
4 & 7 & 5 & 20 \\
0 & -2 & 2 & 0
\end{array} \right] \\
 \xrightarrow{R_2=R_2-2R_1}
& \left[ \begin{array}{ccc|c}
2 & 3 & 1 & 8 \\
0 & 1 & 3 & 4 \\
0 & -2 & 2 & 0
\end{array} \right] \\
\xrightarrow{R_3=R_3+2R_2}
& \left[ \begin{array}{ccc|c}
\boxed{2} & 3 & 1 & 8 \\
0 & \boxed{1} & 3 & 4 \\
0 & 0 & \boxed{8} & 8
\end{array} \right]
=U
\end{aligned}
$

By back substitution, we see that $\boxed{z=1}$. Substituting,
$1$ for $z$ in equation 2 gives $\boxed{y=1}$, and substituting $y$ and $z$
into equation 1 gives $\boxed{x=2}$.

::: note
An easy exercise of Gaussian elimination. I learned how to write text over the
arrows, and it was fun getting them aligned to look pretty!
:::

## Problem 13
Apply elimination, circle the pivots, and use back substitution to solve the
following equations.

$
\begin{aligned}
2x-3y&=3\\
4x-5y+z&=7\\
2x-y-3z&=5
\end{aligned}
$

## Solution 13
$
\begin{aligned}
A = &
\left[ \begin{array}{ccc|c}
2 & -3 & 0 & 3 \\
4 & -5 & 1 & 7 \\
2 & -1 & -3 & 5
\end{array} \right] \\
 \xrightarrow{R_2=R_2-2R_1}
& \left[ \begin{array}{ccc|c}
2 & -3 & 0 & 3 \\
0 & 1 & 1 & 1 \\
2 & -1 & -3 & 5
\end{array} \right] \\
\xrightarrow{R_3=R_3-R_1}
& \left[ \begin{array}{ccc|c}
2 & -3 & 0 & 3 \\
0 & 1 & 1 & 1 \\
0 & 2 & -3 & 2
\end{array} \right] \\
\xrightarrow{R_3=R_3-2R_2}
& \left[ \begin{array}{ccc|c}
\boxed{2} & -3 & 0 & 3 \\
0 & \boxed{1} & 1 & 1 \\
0 & 0 & \boxed{-5} & 0
\end{array} \right]
=U
\end{aligned}
$

By back substitution, we see that $\boxed{z=0}$. Substituting,
$0$ for $z$ in equation 2 gives $\boxed{y=1}$, and substituting $y$ and $z$
into equation 1 gives $\boxed{x=3}$.

::: note
This is getting repetitive, but didn't someone smart say that repetition is the
key to success? Also, it was easy to copy and paste the katex from the previous
question and just change the numbers!
:::

## Problem 14
Which number $d$ forces a row exchange, and what is the triangular system (not
singular) for that $d$? Which $d$ makes this system singular (no third pivot)?

$
\begin{aligned}
2x+5y+z&=0\\
4x+dy+z&=2\\
y-z&=3
\end{aligned}
$

## Solution 14
If $d=0$ then we will need to exchange rows 2 and 3 to avoid a 0 in the second
pivot location:

$
\begin{aligned}
A = &
\left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
4 & 0 & 1 & 2 \\
0 & 1 & -1 & 3
\end{array} \right] \\
\xrightarrow{R_2\leftrightarrow R_3}
& \left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
0 & 1 & -1 & 3 \\
4 & 0 & 1 & 2
\end{array} \right] \\
\xrightarrow{R_3=R_3-2R_1}
& \left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
0 & 1 & -1 & 3 \\
0 & -10 & -1 & 2
\end{array} \right] \\
\xrightarrow{R_3=R_3+10R_2}
& \left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
0 & 1 & -1 & 3 \\
0 & 0 & -11 & 32
\end{array} \right]
=U
\end{aligned}
$

Back substitution:

$
\begin{aligned}
z &= -\frac{32}{11} \\
y &= \frac{1}{11} \\
x &= \frac{27}{22} \\
\end{aligned}
$

To find a value for $d$ which makes the matrix singular with no third pivot,
let's assume that $d$ is not zero and begin elimination:

$
\begin{aligned}
A = &
\left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
4 & d & 1 & 2 \\
0 & 1 & -1 & 3
\end{array} \right] \\
\xrightarrow{R_2 = R_2 - 2R_1}
& \left[ \begin{array}{ccc|c}
2 & 5 & 1 & 0 \\
0 & d-10 & -1 & 2 \\
0 & 1 & -1 & 3
\end{array} \right] \\
\end{aligned}
$

Since the third column of $R_2$ and $R_3$ is identical, the matrix will be
singular if the second column is identical as well. Thus, if $d-10 = 1$ then
the matrix is singular: it will be singular if $\boxed{d=11}$.

::: note
Calculating the elimination here was quite tiring. These exercises are getting
repetitive indeed!
:::

## Problem 15
Which number $b$ leads to a later row exchange? Which $b$ leads to a missing
pivot? In that singular case find a nonzero solution $x,y,z$.

$
\begin{aligned}
x + by \hphantom{+2z}    &=0\\
x - 2y -z &=0\\
\hphantom{x+2} y +z &=0
\end{aligned}
$

In the first step of elimination we will subtract $R_1$ from $R_2$, leaving $-(2+b)$ in
the second pivot position. If $b$ is **-2** this will require a row exchange.

For any other value of $b$, the second pivot will be $-(2+b)$. To eliminate $y$
from the third equation, we set $R_3 = R_3 - \frac{1}{-(2+b)}R_2 = R_3 +
\frac{1}{2+b}R_2.$

For this to result in a singluar matrix, $R_{33}$ must be zero after $R_3$ is
updated. That is, $1 + \frac{1}{2+b}R_{22} = 0$. Substituting $-1$ for $R_{22}$
we have:

$
\begin{aligned}
1 + \frac{1}{2+b}(-1) &= 0 \\
1 - \frac{1}{2+b}&=0 \\
b&=-1
\end{aligned}
$

One valid solution is $\boxed{x=1, y=1, z=-1}$.

## Problem 16
a) Construct a 3 by 3 system that needs two row exchanges to reach a triangular
    form and a solution.

b) Construct a 3 by 3 system that needs a row exchange to keep going, but breaks
    down later.

## Solution 16
a) If $R_{11}$ is zero, we'll immediately need to do a row exchange. Assuming
$R_{21}$ is nonzero, we'll exchange the first two rows. At this point, we'll need
to make sure that $R_{22}$ is a zero, so we'll want the original $R_{11}$ to be
zero. Thus, one such matrix is:

$
\begin{bmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 1
\end{bmatrix}
$

Another such matrix, with fewer 1's, is

$
\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
1 & 0 & 0
\end{bmatrix}
$

There cannot be any matrix with fewer 1's that satisfies the requirements.ere
cannot be any matrix with fewer 1's that satisfies the requirements. This
matrix will be transformed to the identity matrix $I$.

b) A simple example of a matrix that breaks down after the first row exchange
succeeds is a matrix with only two nonzeros. Such a matrix must be singular
because there cannot be 3 pivots. For example:

$
\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$

Exchanging the first two rows yields pivots in those rows, but there is no way to get
a pivot in the third row.

::: note
When solving this problem, I enjoyed working through the logical progression of what must or must not be
true.
:::

## Problem 17
If rows 1 and 2 are the same, how far can you get with elimination (allowing row
exchange)? If columns 1 and 2 are the same, which pivot is missing?

## Solution 17
Assume rows 1 and 2 are the same. Then, subtracting row 1 from row 2 will result
in an all-zero row 2. We can exchange row 2 with row 3, and eliminate x from the
new row 2, but when we then examine row 3 elimination will fail because there
will be a zero in the third pivot location.

If columns 1 and 2 are the same, then $R_{11} = R_{12}$ and $R_{21} = R_{22}$.
Thus, eliminating $R_{21}$ will set $R_{22}$ to zero as well, forcing us to exchange row 2
with row 3. The resulting $R_{21}$ and $R_{22}$ will also be identical, so eliminating
$R_{21}$ will lead to a zero at $R_{22}$. At this point, there will be no lower
rows with a nonzero in the second column, so we will be unable to find a second
pivot.

## Problem 18
Construct a 3 by 3 example that has 9 different coefficients on the left side,
but rows 2 and 3 become zero in elimination. How many solutions to your system
with $\boldsymbol{b} = (1,10,100)$ and how many with $\boldsymbol{b}=(0,0,0)$?

## Solution 18
As long as $R_{2}$ is some multiple $c$ of $R_{1}$, subtracting $c$ copies of $R_1$
from $R_2$ will set $R_{2} = 0$. Similarly, $R_{3}$ must be a multiple $d$ of
$R_1$ so that the operation $R_3=R_3-dR_1$ sets $R_3$ to 0. Therefore, one such example of a matrix is:

$
\begin{bmatrix}
1 & 2 & 3 \\
4 & 8 & 12 \\
5 & 10 & 15
\end{bmatrix}
$

There will be infinite solutions if $\boldsymbol{b} = 0$. In fact, there are no
non-solutions. For any other value of $\boldsymbol{b}$, however, there are no
solutions.

::: note
Initially I created a matrix with 9 variables $a,...,j$ and solved the algebraic
equations for elimination. This led to a correct solution, but the arithmetic
was more complex. It's fun how there are multiple ways to reach the same
solution.
:::

## Problem 19
Which number $q$ makes this system singular and which right side $t$ gives it
infinitely many solutions? Find the solution that has $z=1$.

$
\begin{aligned}
x+4y-2z&=1 \\
x+7y-6z&=6 \\
\hphantom{x+}3y+qz&=t
\end{aligned}
$

## Solution 19

By inspection, eliminating $x$ from equation 2 leaves $3y-4z=5$, and
subtracting this from equation 3 leaves $(q+4)z=t-5$. The system is singular if
$\boxed{q=-4}$. Solutions exist when $t=5$. If $z=1$ then $y=3$ and $x=-9$.

## Problem 20
Three planes can fail to have an intersection point, even if no planes are
parallel. The system is singular if row 3 of $A$ is a ? of the first two rows.
Find a third equation that can't be solved together with $x+y+z=0$ and
$x-2y-z=1$.

## Solution 20
The system is singular if the third row is a **linear combination** of the first
two. For example, adding one copy of the first equation and 2 copies of the
second equation gives $3x-3y-z = 2$. Changing the right-side to any other value
gives a system with no solution.

::: note
This exercise was surprisingly hard for me to visualize. The solution manual
made an interesting observation that these three planes form a trangle. This
makes it easier to visualize, because it is easy to see that the sides of a triangle do not all
intersect at a single point.
:::
