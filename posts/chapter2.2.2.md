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
the matrix is singular: it will be singular if $\boxed{d=11}$,

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
