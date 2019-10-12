---
layout: post
title: Problem Set 2.1 - Part 2
date: 2019-10-06
---

**Problems 9-14 are about multiplying matrices and vectors.**

## Problem 9

Compute each $A\boldsymbol{x}$ by dot products of the rows with the column vector:

a)$
\begin{bmatrix}
    1 & 2 & 4 \\
    -2 & 3 & 1 \\
    -4 & 1 & 2
\end{bmatrix}
\begin{bmatrix}
    2 \\ 2 \\ 3
\end{bmatrix}
$

b)$
\begin{bmatrix}
    2 & 1 & 0 & 0 \\
    1 & 2 & 1 & 0 \\
    0 & 1 & 2 & 1 \\
    0 & 0 & 1 & 2
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1 \\ 1 \\ 2
\end{bmatrix}
$

## Solution 9

a)
$
\begin{bmatrix}
    1 & 2 & 4 \\
    -2 & 3 & 1 \\
    -4 & 1 & 2
\end{bmatrix}
\begin{bmatrix}
    2 \\ 2 \\ 3
\end{bmatrix} =
\begin{bmatrix}
    18 \\ 5 \\ 0
\end{bmatrix}
$

b)
$
\begin{bmatrix}
    2 & 1 & 0 & 0 \\
    1 & 2 & 1 & 0 \\
    0 & 1 & 2 & 1 \\
    0 & 0 & 1 & 2
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1 \\ 1 \\ 2
\end{bmatrix} =
\begin{bmatrix}
    3 \\ 4 \\ 5 \\ 5
\end{bmatrix}
$

## Problem 10

Compute each $A\boldsymbol{x}$ in Problem 9 as a combination of the columns: 9\(a\) becomes $A\boldsymbol{x}= 2\begin{bmatrix}1 \\ -2 \\ 4\end{bmatrix} + 2\begin{bmatrix}2 \\ 3 \\ 1\end{bmatrix} + 3\begin{bmatrix}4 \\ 1 \\ 2\end{bmatrix} = \begin{bmatrix} ?\\ ? \\ ? \end{bmatrix}.$

How many separate multiplications for $A\boldsymbol{x}$ when the matrix is "3 by 3"?

## Solution 10

a\) $A\boldsymbol{x}= 2\begin{bmatrix}1 \\ -2 \\ 4\end{bmatrix} + 2\begin{bmatrix}2 \\ 3 \\ 1\end{bmatrix} + 3\begin{bmatrix}4 \\ 1 \\ 2\end{bmatrix} = \begin{bmatrix} 18 \\ 5 \\ 0 \end{bmatrix}.\quad$ 9 multiplications.

b\) $A\boldsymbol{x}= 1\begin{bmatrix}2 \\ 1 \\ 0 \\ 0\end{bmatrix} + 1\begin{bmatrix}1 \\ 2 \\ 1 \\ 0\end{bmatrix} + 1\begin{bmatrix}0 \\ 1 \\ 2 \\ 1\end{bmatrix} + 2\begin{bmatrix}0 \\ 0 \\ 1 \\ 2\end{bmatrix} = \begin{bmatrix} 3 \\ 4 \\ 5 \\ 5\end{bmatrix}.$ 16 multiplications.

## Problem 11

Find the two components of $A\boldsymbol{x}$ by rows or by columns:

$
\begin{bmatrix}2 & 3 \\ 5 & 1\end{bmatrix}\begin{bmatrix}4 \\ 2\end{bmatrix}
\text{and}
\begin{bmatrix}3 & 6 \\ 6 & 12\end{bmatrix}\begin{bmatrix}2 \\ -1\end{bmatrix}
\text{and}
\begin{bmatrix}1 & 2 & 4 \\ 2 & 0 & 1\end{bmatrix}\begin{bmatrix}3 \\ 1 \\ 1\end{bmatrix}.
$

## Solution 11

$$
\begin{bmatrix}2 & 3 \\ 5 & 1\end{bmatrix}\begin{bmatrix}4 \\ 2\end{bmatrix} =
\begin{bmatrix}14 \\ 22\end{bmatrix}
\qquad
\begin{bmatrix}3 & 6 \\ 6 & 12\end{bmatrix}\begin{bmatrix}2 \\ -1\end{bmatrix} =
\begin{bmatrix}0 \\ 0\end{bmatrix}
\qquad
\begin{bmatrix}1 & 2 & 4 \\ 2 & 0 & 1\end{bmatrix}\begin{bmatrix}3 \\ 1 \\ 1\end{bmatrix} =
\begin{bmatrix}9 \\ 7\end{bmatrix}
$$

## Problem 12

Multiply $A$ times $\boldsymbol{x}$ to find three components of $A\boldsymbol{x}$.

$
\begin{bmatrix}
    0 & 0 & 1 \\
    0 & 1 & 0 \\
    1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
    x \\ y \\ z
\end{bmatrix}
\text{and}
\begin{bmatrix}
    2 & 1 & 3 \\
    1 & 2 & 3 \\
    3 & 3 & 6 \\
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1 \\ -1
\end{bmatrix}
\text{and}
\begin{bmatrix}
    2 & 1 \\
    1 & 2 \\
    3 & 3 \\
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1
\end{bmatrix}
.
$

## Solution 12

10/6/2019

$
\begin{bmatrix}
    0 & 0 & 1 \\
    0 & 1 & 0 \\
    1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
    x \\ y \\ z
\end{bmatrix} =
\begin{bmatrix}
    z \\ y \\ x
\end{bmatrix}
$
```
This is cool -- an example of how we can rearrange the rows in a vector.
```
$
\begin{bmatrix}
    2 & 1 & 3 \\
    1 & 2 & 3 \\
    3 & 3 & 6
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1 \\ -1
\end{bmatrix} =
\begin{bmatrix}
    0 \\ 0 \\ 0
\end{bmatrix}
$

$
\begin{bmatrix}
    2 & 1 \\
    1 & 2 \\
    3 & 3
\end{bmatrix}
\begin{bmatrix}
    1 \\ 1
\end{bmatrix} =
\begin{bmatrix}
    3 \\ 3 \\ 6
\end{bmatrix}
$

## Problem 13

a\) A matrix with $m$ rows and $n$ columns multiplies a vector with $\underline{ ? }$ components to produce a vector $\underline{ ? }$ components.

b\) The planes from the $m$ equations $A\boldsymbol{x} = \boldsymbol{b}$ are in $\underline{ ? }$-dimensional space. The combination of the columns of $A$ is in $\underline{ ? }$-dimensional space.

## Solution 13

a\) A matrix with $m$ rows and $n$ columns multiplies a vector with  $\pmb{n}$ components to produce a vector with $\pmb{m}$ components.

b\) The planes from the $m$ equations $A\boldsymbol{x} = \boldsymbol{b}$ are in $\pmb{n}$-dimensional space. The combination of the columns of $A$ is in $\pmb{m}$-dimensional space.

## Problem 14

Write $2x + 3y + z + 5t = 8$ as a matrix $A$ \(how many rows?\) multiplying the column vector $\boldsymbol{x} = (x,y,z,t)$ to produce $\boldsymbol{b}$. The solutions $\boldsymbol{x}$ fill a plane or "hyperplane" in 4-dimensional space. _The plane is 3-dimensional with no 4D volume._

## Solution 14

The matrix contains one row:
$
\begin{bmatrix}
    2 & 3 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
    x \\ y \\ z \\ t
\end{bmatrix} =
8
$
