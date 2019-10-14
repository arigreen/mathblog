---
layout: post
title: Problem Set 2.1 - Part 3
date: 2019-10-10
---

**Problems 15-22 ask for matrices that act in special ways on vectors.**

## Problem 15

a\) What is the 2 by 2 identity matrix $I$ such that $I\begin{bmatrix}x \\ y\end{bmatrix} = \begin{bmatrix}x \\ y\end{bmatrix}$ ?

b\) What is the 2 by 2 exchange matrix $P$ such that $P\begin{bmatrix}x \\ y\end{bmatrix} = \begin{bmatrix}y \\ x\end{bmatrix}$?

```
This exercise reminds us what an Identity matrix is, and introduces us to an
exchange matrix.
```

### Solution 15

$\text{a)} I = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} \qquad \text{b)} P = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}$

## Problem 16
- a) What 2 by 2 matrix $R$ rotates every vector by $90^\circ$? $R$ times
$\bigl[\begin{smallmatrix}x \\ y\end{smallmatrix}\bigr]$ equals
$\bigl[\begin{smallmatrix}y \\ -x\end{smallmatrix}\bigr]$

- b) What 2 by 2 matrix $R^2$ rotates every vector by $180^\circ$?

## Solution 16
a) $\begin{bmatrix}0 & 1 \\ -1 & 0\end{bmatrix}\begin{bmatrix}x \\
    y\end{bmatrix} = \begin{bmatrix}y \\ -x\end{bmatrix}$

b) $\begin{bmatrix}-1 & 0 \\ 0 & -1\end{bmatrix}\begin{bmatrix}x \\
    y\end{bmatrix} = \begin{bmatrix}-x \\ -y\end{bmatrix}$

## Problem 17
a) Find the matrix $P$ that multiples $(x,y,z)$ to give $(y,z,x)$.

b) Find the matrix $Q$ that multiplies $(y,z,x)$ to bring back $(x,y,z)$.

## Solution 17
$
P =
\begin{bmatrix}
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    1 & 0 & 0
\end{bmatrix}
\longrightarrow
\begin{bmatrix}
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}x \\ y \\ z \end{bmatrix}=
\begin{bmatrix}y \\ z \\ x\end{bmatrix}$

$
Q =
\begin{bmatrix}
    0 & 0 & 1 \\
    1 & 0 & 0 \\
    0 & 1 & 0
\end{bmatrix}
\longrightarrow
\begin{bmatrix}
    0 & 0 & 1 \\
    1 & 0 & 0 \\
    0 & 1 & 0
\end{bmatrix}
\begin{bmatrix}y \\ z \\ x \end{bmatrix}=
\begin{bmatrix}x \\ y \\ z\end{bmatrix}$

## Problem 18
What 2 by 2 matrix $E$ subtracts the first component from the second component?

What 3 by 3 matrix does the same?

$
\qquad E\begin{bmatrix}3 \\ 5\end{bmatrix}=\begin{bmatrix}3 \\ 2\end{bmatrix}
\qquad E\begin{bmatrix}3 \\ 5 \\ 7\end{bmatrix}=\begin{bmatrix}3 \\ 2 \\ 7\end{bmatrix}
$

## Solution 18
$
E = \begin{bmatrix}
    1 & 0 \\
    -1 & 1
    \end{bmatrix}
\qquad
E = \begin{bmatrix}
    1 & 0 & 0\\
    -1 & 1 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
$

## Problem 19
What 3 by 3 matrix $E$ multiplies $(x, y, z)$ to give $(x, y, z+x)$?

What matrix $E^{-1}$ multiplies $(x, y, z)$ to give $(x,y,z-x)$?

If you multiply $(3,4,5)$ by $E$ and then multiply by $E^{-1}$, the two results are $?$ and $?$

## Solution 19
$
E = \begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0 \\
    1 & 0 & 1
    \end{bmatrix}
\qquad\qquad
E^{-1} =
\begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0 \\
    -1 & 0 & 1
\end{bmatrix}
$

$
\begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0 \\
    1 & 0 & 1
\end{bmatrix}
\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix}=
\begin{bmatrix}3 \\ 4 \\ 8\end{bmatrix}\qquad
\begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0 \\
    -1 & 0 & 1
\end{bmatrix}
\begin{bmatrix}3 \\ 4 \\ 8\end{bmatrix}=
\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix}
$

## Problem 20
What 2 by 2 matrix $P_1$ projects the vector $(x,y)$ onto the $x$ axis to
produce $(x,0)$?

What matrix $P_2$ projects onto the $y$ axis to produce $(0,y)$?

What do you get if you multiply $(5,7)$ by $P_1$ and then multiply by $P_2$?
## Solution 20
```
This exercise shows how we can combine projection matrices to modify a vector v.
```

$P_1 = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}$

$P_2 = \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix}$

$\begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}\begin{bmatrix}5 \\ 7\end{bmatrix}=\begin{bmatrix}5 \\ 0\end{bmatrix}$

$\begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix}\begin{bmatrix}5 \\ 0\end{bmatrix}=\begin{bmatrix}0 \\ 0\end{bmatrix}$

$P_2P_1\boldsymbol{v}=\begin{bmatrix}0 \\ 0\end{bmatrix}$


## Problem 21
What 2 by 2 matrix $R$ rotates every vector through 45$\degree$?
The vector $(1,0)$ goes to $(\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2})$.
The vector $(0,1)$ goes to $(\frac{-\sqrt{2}}{2},\frac{\sqrt{2}}{2})$.
Those determine the matrix. Draw these particular vectors in the $xy$ plane and
find $R$.

## Solution 21
$R = \begin{bmatrix}
    \frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\
    \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}
    \end{bmatrix}
$

## Problem 22
Write the dot product of $(1,4,5)$ and $(x,y,z)$ as a matrix multiplication
$A\boldsymbol{x}$. The matrix $A$ has one row. The solutions to $A\boldsymbol{x}
= \boldsymbol{0}$ lie on a `?` perpendicular to the vector `?`. The columns of
$A$ are only in `?`-dimensional space.

## Solution 22
$A\boldsymbol{x} = \begin{bmatrix}1 & 4 & 5\end{bmatrix}\begin{bmatrix}x \\ y
\\ z\end{bmatrix} = \boxed{1x + 4y + 5z}$.

The solutions to $1x + 4y + 5z = 0$ lie on a **plane**.
The three columns of $A$ are only in **1**-dimensional space.
$\textcolor{red}{\textnormal{I do not know what vector this plane is perpendicular to.}}$

