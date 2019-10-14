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

