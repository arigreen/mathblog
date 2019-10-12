---
layout: post
title: Problem Set 2.1 - Part 1
date: 2019-10-01
---

**Problems 1-8 are about the row and column pictures of $Ax = b$.**

## Problem 1

With $A = I$ \(the identity matrix\) draw the planes in the row picture. Three sides of a box meet at the solution $\boldsymbol{x} = (x, y, z) = (2, 3, 4)$:

$
\begin{array}{cc}
   1x+0y+0z&=2 \\
   0x+1y+0z&=3 \\
   0x+0y+1z&=4
\end{array}
\quad
\text{or}
\quad
\begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
\end{bmatrix}
\begin{bmatrix} x \\ y \\ z
\end{bmatrix}=
\begin{bmatrix} 2 \\ 3 \\ 4\end{bmatrix}.
$

Draw the vectors in the column picture. Two times column 1 plus three times column 2 plus four times column 3 equals the right side $\boldsymbol{b}$.


## Solution 1

Row picture:
```
    TODO: Add a 3d graphs for the row and column pictures.
```
The row picture consists of three perpendicular planes: $x=2$, $y=3$, and $z=4$.

The column picture consists of three vectors, each of length 1:
$\boldsymbol{i} = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$, $\boldsymbol{j} = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}$,
and $\boldsymbol{k} = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$.

$
2\boldsymbol{i} + 3\boldsymbol{j} + 4\boldsymbol{k} = \boldsymbol{b}
$

## Problem 2.
If the equations in Problem 1 are multipled by $2, 3, 4$ they become $D\boldsymbol{X} = \boldsymbol{B}$:

$
\begin{array}{cc}
    2x+0y+0z&=4 \\
    0x+3y+0z&=9 \\
    0x+0y+4z&=16&
\end{array}
\text{or}
\quad
\begin{bmatrix}
    2 & 0 & 0 \\
    0 & 3 & 0 \\
    0 & 0 & 4
\end{bmatrix}
\begin{bmatrix} x \\ y \\ z
\end{bmatrix}=
\begin{bmatrix} 4 \\ 9 \\ 16\end{bmatrix}=\boldsymbol{B}.
$

Why is the row picture the same? Is the solution $\boldsymbol{X}$ the same as $\boldsymbol{x}$? What is changed in the column picture -- the columns or the right combination to give $\boldsymbol{B}$?

## Solution 2
The row picture is the same because the same planes satisfy the equations as in Problem 1. $\boldsymbol{X}$ is the same as $\boldsymbol{x}$. In the column picture, the vectors $\boldsymbol{I}$, $\boldsymbol{J}$, and $\boldsymbol{K}$ are 2, 3, and 4 times longer respectively than they were in solution 1. The right combination of vectors to give $\boldsymbol{B}$ remains the same.

## Problem 3
If equation 1 is added to equation 2, which of these are changed: the planes in the row picture, the vectors in the column picture, the coefficient matrix, the solution? The new equations in Problem 1 would be $x=2$, $x+y=5$, $z=4$.

## Solution 3
The second plane in the row picture will be changed, since $x+y=5$ is a new plane.

The first column vector will be changed, since it will be $\boldsymbol{i} = \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix}$.

The coefficient matrix will be changed to $\begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$

The solution does not change. $x=2$, $y=3$, and $z=4$.

## Problem 4
Find a point with $z=2$ on the intersection line of the planes $x+y+3z=6$ and $x-y+z=4$. Find the point where $z=0$. Find a third point halfway between.

## Solution 4
$
z = 2
\qquad
\begin{aligned}
  x+y+3z&=6 \\
  x+y+3(2) &= 6 \\
  x + y &= 0
\end{aligned}
\qquad
\begin{aligned}
  x-y+z &= 4 \\
  x-y+2 &= 4 \\
  x-y &=2
\end{aligned}
$

We can now see that $(1, -1, 2)$ satisfies both equations.

$
z = 0
\qquad
\begin{aligned}
  x+y+3(0)&=6 \\
  x+y &= 6
\end{aligned}
\qquad
\begin{aligned}
  x-y+z &= 4 \\
  x-y =4
\end{aligned}
$

We see that $(5, 1, 0)$ satisfies both equations. Midway between these 2 points is $(3, 0, 1)$.

## Solution 5
If $x, y, z$ satisfy the first two equations then they also **must satisfy the third equation**.

$\boldsymbol{L}$ is the line where $y=1$ and $x+z=1$. Points on $\boldsymbol{L}$ include \($0,1,1)$, $(1,1,0)$, and $(2,1,-1)$.

## Problem 6

Move the third plane in Problem 5 to a parallel plane $2x + 3y + 2z = 9$. Now the three equations have no solution. Why not? The first two planes meet along line $\boldsymbol{L}$, but the third plane doesn't $\underline{ ? }$ with that line.

## Solution 6
The third plane doesn't **intersect** with $\boldsymbol{L}$. Since $y$ is always $1$ on $\boldsymbol{L}$, for the third plane to intersect, $2x + 2z = 6$. However, on $\boldsymbol{L}$ $x+z=1$ so $2x+2z=2$. Hence, there is no solution that satisfies all three equations.

## Problem 7

In Problem 5 the columns are $(1,1,2)$ and $(1,2,3)$ and $(1,1,2)$. This is a "singular case" because the third column is $\underline{ ? }$. Find two combinations of the columns that give $\boldsymbol{b} = (2,3,5)$. This is only possible for $\boldsymbol{b} = (4,6,c)$ if $c$ is $\underline{ ? }$.

## Solution 7
Column 3 is identical to column 1. $\boldsymbol{b} = (2,3,5)$ can be expressed as column 1 + column 2 or as column 3 + column 2. This is only possible for $\boldsymbol{b} = (4,6,c)$ if $c = 10$.

Using mathematical notation, calling the columns $x$, $y$, and $z$, two solutions for $\boldsymbol{b} = (2,3,5)$ include $(1,1,0)$ and $(0,1,1)$

```
New Definition: A matrix is **singular** if two or more columns are identical.
```

## Problem 8

Normally 4 "planes" in 4-dimensional space meet at a $\underline{ ? }$. Normally 4 column vectors in 4-dimensional space can combine to produce $\boldsymbol{b}$. What combination of $(1,0,0,0),(1,1,0,0),(1,1,1,0)$ and $(1,1,1,1)$ produces $\boldsymbol{b} = (3,3,3,2)$? What 4 equations for $x,y,z,t$ are you solving?

## Solution 8

Normally 4 hyperplanes in 4-dimensional space will meet at a **point**. To solve what combinations of these 4 vectors produce $(3,3,3,2)$ we must solve the following 4 equations: \(Note that since these are column vectors, they are written from top to bottom in the equations.

$
\begin{array}{rc}
    x + y + z + t &=3 \\
    y + z + t &=3 \\
    z+t&=3 \\
    t&=2
\end{array}{}
$

Solving bottom to top, we see that $t=2, z=1, y=0, x=0$.

