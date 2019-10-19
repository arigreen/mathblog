---
layout: post
title: Problem Set 2.2 - Part 1
date: 2019-10-17
---

**Problems 1-10 are about elimination on 2 by 2 systems.**

## Problem 1
What multiple of $l_{21}$ of equation 1 should be subtracted from equation 2?

$
\begin{aligned}
2x + 3y &= 1 \\
10x + 9y &= 11
\end{aligned}
$

After elimination, write down the upper triangular system and circle the two
pivots.

## Solution 1
Subtracting **$\ell_{21}=5$** copies of equation 1 from equation 2 will eliminate $x$ from the
second equation, thereby making the system upper triangular. The pivots are
boxed.

$
A=
\left[ \begin{array}{cc|c}
2 & 3 & 1 \\
10 & 9 & 11
\end{array} \right]
\longrightarrow
\left[ \begin{array}{cc|c}
\boxed{2} & 3 & 1 \\
0 & \boxed{-6} & 6
\end{array} \right]
=U
$

## Problem 2
Solve the triangular system of Problem 1 by back substitution, $y$ before $x$.
Verify that $x$ times $(2,10)$ plus $y$ times $(3,9)$ equals $(1,11)$. If the
right side changes to $(4,44)$ what is the new solution?

$
\begin{aligned}
-6y &= 6 &\longrightarrow \boxed{y=-1} \\
2x + 3y &= 1 \longrightarrow 2x + 3(-1) = 1 & \longrightarrow \boxed{x=2}
\end{aligned}
$

## Solution 2

We can verify that $2(2,10) + (-1)(3,9) = (1,11)$.

Note that if changing the right side to $(4,44)$ is equivalent to multiplying it
by 4. Multiplying the left hand side by 4 results in the new solved equation
$8(2,10)+(-4)(3,9)=(4,44)$.

## Problem 3
What multiple of equation 1 should be subtracted from equation 2?

$
\begin{aligned}
2x - 4y &= 6 \\
-x + 5y &= 0
\end{aligned}
$

After this elimination step, solve the triangular system. If the right side
changes to $(-6,0)$, what is the new solution?

## Solution 3
Subtracting **$\ell=\frac{-1}{2}$** copies of equation 1 from equation 2 will eliminate $x$ from the
second equation, thereby making the system upper triangular. It's actually
easier to think of this as _adding_ $\frac{1}{2}$ copy of equation 1 to equation
2.

$
A=
\left[ \begin{array}{cc|c}
2 & -4 & 6 \\
-1 & 5 & 0
\end{array} \right]
\longrightarrow
\left[ \begin{array}{cc|c}
\boxed{2} & -4 & 6 \\
0 & \boxed{3} & 3
\end{array} \right]
=U \\
\boxed{y=1}, \boxed{x=5}
$

If the right side changes to $(-6,0)$ then $x=-5$ and $y=-1$.
::: note
The interesting thing here is that to solve the system when $\boldsymbol{b}$ is multiplied
by -1, we multiply the original solution by -1 as well.
:::

## Problem 4
What multiple $\ell$ of equation 1 should be subtracted from equation 2 to
remove c?

$
ax+by=f \\
cx+dy=g
$.

The first pivot is $a$ (assumed nonzero). Elimination produces what formula for
the second pivot? What is $y$? The second pivot is missing when $ad=bc$:
singular.

## Solution 4
To eliminate $cx$ from equation 2, we must find a multiple of equation 1 that
contains the term $cx$. Therefore, $\ell$ must be **$\frac{c}{a}$** because $\frac{c}{a}(ax)
= cx$, and when this is subtracted from equation 2 then $x$ will be eliminated.
Consequently, $\frac{c}{a}$ times the first equation gives $cx + \frac{bc}{a}y =
\frac{fc}{a}$; when this is subtracted from equation 2 we have $(d-\frac{bc}{a})y = g-\frac{fc}{a}$.
The second pivot is $\boxed{d-\frac{bc}{a}}$

To solve for $y$, multiply both sides of the equation by $a$ to get:

$
(da-bc)y = ga-fc \\
y = \frac{ga-fc}{da-bc}
$

::: note
We haven't learned the signifcance of the _determinant_ yet, but this exercise
shows us why things don't work properly when $da-bc=0$ because you cannot solve
for $y$.
:::
