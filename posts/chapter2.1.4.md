---
layout: post
title: Problem Set 2.1 - Part 4
date: 2019-10-13
---
## Problem 23
In `MATLAB` notation, write the commands that define this matrix $A$ and the
column vectors $\boldsymbol{x}$ and $\boldsymbol{b}$. What command would test
whether or not $A\boldsymbol{x}=\boldsymbol{b}$?

$
A = \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix}
\qquad\boldsymbol{x}=\begin{bmatrix}5 \\ -2\end{bmatrix}
\qquad\boldsymbol{b}=\begin{bmatrix}1 \\ 7\end{bmatrix}
$

## Solution 23
I will use python with numpy instead of `MATLAB`.
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
x = np.array([5, -2])
b = np.array([1, 7])
print(np.array_equal(np.dot(A, x), b))
```

## Problem 24
_Skipped, because the syntax is specific to MATLAB._

## Problem 25
If you multiply the 4 by 4 all-ones matrix $A$ and the all-ones vector
$\boldsymbol{v}$, what is $A\boldsymbol{v}$?
_The second part is skipped, as it uses MATLAB specific syntax which I am not
interested in deciphering._

## Solution 25
$A\boldsymbol{v} = \begin{bmatrix}4\\4\\4\\4\end{bmatrix}$.

**Questions 26-28 review the row and column picture in 2, 3, and 4 dimensions.**

## Problem 26
Draw the row and column pictures for the equations $x-2y=0$ and $x+y=6$.

## Solution 26
The row picture conists of 2 lines, intersecting at $x=4, y=2$.

The column picture has $4(1, 1) + 2(-2, 1) \longrightarrow (0, 6)$

## Problem 27
For two linear equations in three unknowns $x,y,z$ the row picture will show how
many lines or planes, in what-dimensional space? The column picture is in
what-dimensional space? The solutions normally lie on a `?`

## Solution 27
Each equation with three variables will result in a **plane** in 3-dimensional
space. Since there are 2 equations there will be **2** planes, typically
intersecting on a **line**.

Each column is in 2 dimensions so the column picture is in **2-dimensional** space

## Problem 28
For four linear equations in two unknowns $x$ and $y$, the row picture shows
four `?` The column picture is in `?`-dimensional space. The equations have no
solution unless the vector on the right side is a combination of `?`.

## Solution 28
The row picture shows four **lines**.

The column picture is in **4**-dimensional space.

There will only be a solution if the vector on the right side is a combination
of the **two vectors on the left side**.

## Problem 29
Start with the vector $\boldsymbol{u}_0 = (1,0)$. Multiply again and again by
the same "Markov matrix" $A = \bigl[\begin{smallmatrix}.8 & .3 \\ .2 &
.7\end{smallmatrix}\bigr]$. The next three vectors are
$\boldsymbol{u}_1, \boldsymbol{u}_2, \boldsymbol{u}_3$:

$
\boldsymbol{u}_1 =\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}1 \\ 0\end{bmatrix}=\begin{bmatrix}.8 \\ .2\end{bmatrix}
$

$
\boldsymbol{u}_2 =A\boldsymbol{u}_1=?
$

$
\boldsymbol{u}_3 =A\boldsymbol{u}_2=?
$

What property do you notice for all four vectors $\boldsymbol{u}_0,\boldsymbol{u}_1,\boldsymbol{u}_2,\boldsymbol{u}_3$?


## Solution 29
$
\boldsymbol{u}_1 =\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}1 \\ 0\end{bmatrix}=\begin{bmatrix}.8 \\ .2\end{bmatrix}
$

$
\boldsymbol{u}_2 =A\boldsymbol{u}_1=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.8 \\ .2\end{bmatrix}=\begin{bmatrix}.7 \\ .3\end{bmatrix}
$

$
\boldsymbol{u}_3 =A\boldsymbol{u}_2=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.7 \\ .3\end{bmatrix}=\begin{bmatrix}.65 \\ .35\end{bmatrix}
$

For all vectors $\boldsymbol{u}_i$, the sum of the components is $1$.

