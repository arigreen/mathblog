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
