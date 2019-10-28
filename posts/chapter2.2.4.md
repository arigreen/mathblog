---
layout: post
title: Problem Set 2.2 - Part 4
date: 2019-10-27
---
## Challenge Problems

Problem 29 is skipped as it involves MATLAB/

## Problem 30
If the last corner entry is $A(5,5) = 11$ and the last pivot of $A$ is
$U(5,5)=4$, what different entry $A(5,5)$ would have made $A$ singular?

## Solution 30
Let us construct an $A$ and a $U$ consistent with the requirements. The last
pivot of $U$ occurs in the bottom right corner, so $A$ is not singular. Suppose
$A$ contains $1$'s along the diagonal with the bottom right element set to $11$.
For this to have $4$ as the final pivot, we must need to subtract $7$
from $A_{55}$. Notice that if $A_{54} = 7$ then elimination will require that we
subtract 5 copies of row 4 from row 5 to compute $U$. If $A_{45}$ is 1, then
$U_{55}$ will be $11-7=4$. An example $A$ and its corresponding $U$ is:

$
A=
\begin{bmatrix}
1&0&0&0&0\\
0&1&0&0&0\\
0&0&1&0&0\\
0&0&0&1&1\\
0&0&0&7&11
\end{bmatrix}
\xrightarrow{R_5 = R_5 - 7R_4}
\begin{bmatrix}
1&0&0&0&0\\
0&1&0&0&0\\
0&0&1&0&0\\
0&0&0&1&1\\
0&0&0&0&4
\end{bmatrix}=U
$

We can see that if $A_{55}$ had been $7$, elimination would have produced 0 in the
bottom row so the matrix would have been singular.

## Problem 31
Suppose elimination takes $A$ to $U$ without row exchanges. Then row $j$ of $U$
is a combination of which rows of $A$? If $A\boldsymbol{x}=\boldsymbol{0}$, is
$U\boldsymbol{x}=\boldsymbol{0}$? If $A\boldsymbol{x}=\boldsymbol{b}$, is
$U\boldsymbol{x}=\boldsymbol{b}$? If $A$ starts out lower triangular, what is
the upper triangular $U$?

## Solution 31
Row 1 of $U$ is equivalent to row 1 of $A$.

Row 2 of $U$ is a linear combination of rows 1 and 2 of $A$.

Row 3 of $U$ is a linear combination of the first 3 rows of $A$.

In general, row $j$ of $U$ is a **combination of the first $j$ rows of $A$.**

If $A\boldsymbol{x}=\boldsymbol{0}$, then any linear combination of the rows
of the augmented matrix $A|\boldsymbol{b}$ will also have $\boldsymbol{b}=0$,
so $U\boldsymbol{x}=\boldsymbol{0}$. However, for a nonzero $\boldsymbol{b}$ in
general $U\boldsymbol{x}\not = \boldsymbol{b}$.

If $A$ starts out lower triangular, then $U$ will be the diagnoal matrix whose
diagonal entries are equivalent to $A's$.

