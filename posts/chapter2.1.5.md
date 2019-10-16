---
layout: post
title: Problem Set 2.1 - Part 5
date: 2019-10-14
---
### Challenge Problems
## Problem 30
Continue Problem 29 from $\boldsymbol{u}_0 = (1,0)$ to $\boldsymbol{u}_7$,
and also from $\boldsymbol{v}_0 = (0,1)$ to $\boldsymbol{v}_7.$

(Recall that the"Markov matrix" $A = \bigl[\begin{smallmatrix}.8 & .3 \\ .2 & .7\end{smallmatrix}\bigr]$.)

What do you notice about $\boldsymbol{u}_7$ and $\boldsymbol{v}_7$?

Plot $\boldsymbol{u}_0$ to $\boldsymbol{u}_7$ and $\boldsymbol{v}_0$ to $\boldsymbol{v}_7$,

The $\boldsymbol{u}$'s and $\boldsymbol{v}$'s are approaching a steady state
vector $\boldsymbol{s}$. Guess that vector and check that $A\boldsymbol{s}=\boldsymbol{s}.$

## Solution 30
$
\boldsymbol{u}_1 =A\boldsymbol{u}_0=\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
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

$
\boldsymbol{u}_4 =A\boldsymbol{u}_3=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.65 \\ .35\end{bmatrix}=\begin{bmatrix}.625 \\ .375\end{bmatrix}
$

$
\boldsymbol{u}_5 =A\boldsymbol{u}_4=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.625 \\ .375\end{bmatrix}=\begin{bmatrix}.6125 \\ .3875\end{bmatrix}
$

$
\boldsymbol{u}_6 =A\boldsymbol{u}_5=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.6125 \\ .3875\end{bmatrix}=\begin{bmatrix}.60625 \\.39375 \end{bmatrix}
$

$
\boldsymbol{u}_7 =A\boldsymbol{u}_6=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.60625 \\ .39375\end{bmatrix}=\begin{bmatrix}.603125 \\ .396875\end{bmatrix}
$

$
\boldsymbol{v}_1 =A\boldsymbol{v}_0=\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}0 \\ 1\end{bmatrix}=\begin{bmatrix}.3 \\ .7\end{bmatrix}
$

$
\boldsymbol{v}_2 =A\boldsymbol{v}_1=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.3 \\ .7\end{bmatrix}=\begin{bmatrix}.45 \\ .55\end{bmatrix}
$

$
\boldsymbol{v}_3 =A\boldsymbol{v}_2=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.45 \\ .55\end{bmatrix}=\begin{bmatrix}.525 \\ .475\end{bmatrix}
$

$
\boldsymbol{v}_4 =A\boldsymbol{v}_3=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.525 \\ .475\end{bmatrix}=\begin{bmatrix}.5625 \\ .4375\end{bmatrix}
$

$
\boldsymbol{v}_5 =A\boldsymbol{v}_4=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.5625 \\ .4375\end{bmatrix}=\begin{bmatrix}.58125 \\ .41875\end{bmatrix}
$

$
\boldsymbol{v}_6 =A\boldsymbol{v}_5=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.58125 \\ .41875\end{bmatrix}=\begin{bmatrix}.590625 \\.409375 \end{bmatrix}
$

$
\boldsymbol{v}_7 =A\boldsymbol{v}_6=
\begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}.590625 \\ .409375\end{bmatrix}=\begin{bmatrix}.5953125 \\ .4046875\end{bmatrix}
$

It appears that we are approaching $\boldsymbol{s}=\begin{bmatrix}6\\4\end{bmatrix}$. Indeed:

$
A\boldsymbol{s} = \begin{bmatrix}.8 & .3 \\ .2 & .7\end{bmatrix}
\begin{bmatrix}6 \\ 4\end{bmatrix}=\begin{bmatrix}6 \\ 4\end{bmatrix}
$

## Problem 31
Invent a 3 by 3 **magic matrix** $M_3$ with entries $1,2,...9$. All rows,
columns, and diagonals add to 15. The first row could be $8, 3, 4$. What is
$M_3$ times $(1,1,1)$? What is $M_4$ times $(1,1,1,1)$ if a 4 by 4 magic matrix
has entries $1, ..., 16$?

## Solution 31
$M_3 = \begin{bmatrix}
m_{11}&m_{12}&m_{13}\\
m_{21}&m_{22}&m_{23}\\
m_{31}&m_{32}&m_{33}
\end{bmatrix}
\begin{bmatrix}1 \\ 1 \\ 1\end{bmatrix}=
\begin{bmatrix}
m_{11}+m_{12}+m_{13}\\
m_{21}+m_{22}+m_{23}\\
m_{31}+m_{32}+m_{33}
\end{bmatrix}=
\begin{bmatrix}
15 \\ 15 \\ 15
\end{bmatrix}$

because each row of $M_3$ sums to $15$.

Similarly, $M_4$ times $(1,1,1,1)$ = $(34,34,34,34)$

## Problem 32
Suppose $\boldsymbol{u}$ and $\boldsymbol{v}$ are the first two columns of a 3
by 3 matrix $A$. Which third columns $\boldsymbol{w}$ would make the matrix
singular? Describe a typical column picture of $A\boldsymbol{x}=\boldsymbol{b}$
in that singular case, and a typical row picture (for a random $\boldsymbol{b}$).

::: warning
I was not able to correctly describe the column and row pictures -- I needed to look at the solution guide.
:::

## Solution 32
$\boldsymbol{w}$ would be some linear combination
$c_1\boldsymbol{u}+c_2\boldsymbol{v}$.

The column picture in the singular case
would be three vectors that span a plane, with $\boldsymbol{b}$ outside that
plane. The row picture shows the intersection line of two planes parallel to a third
plane.

## Problem 33
**Multiplication by $A$ is a `linear transformation`.** This means:

::: note
If $\boldsymbol{w}$ is a combination of $\boldsymbol{u}$ and $\boldsymbol{v}$,
then $A\boldsymbol{w}$ is the same combination of $A\boldsymbol{u}$ and
$A\boldsymbol{v}$.
:::

It is this **linearity** $A\boldsymbol{w}=cA\boldsymbol{u} + dA\boldsymbol{v}$
that gives us the name "linear algebra".

If $\boldsymbol{u} = \begin{bmatrix}1\\0\end{bmatrix}$ and $\boldsymbol{v} = \begin{bmatrix}0\\1\end{bmatrix}$
then $A\boldsymbol{u}$ and $A\boldsymbol{v}$ are the columns of $A$.

Let $\boldsymbol{w} = c\boldsymbol{u} + d\boldsymbol{v}$. If $\boldsymbol{w} =
\begin{bmatrix}5 \\ 7\end{bmatrix}$ then how is $A\boldsymbol{w}$ connected to
$A\boldsymbol{u}$ and $A\boldsymbol{v}$?

## Solution 33
$A\boldsymbol{w} = cA\boldsymbol{u} +  dA\boldsymbol{v}$.
Thus, $c=5$ and $d=7$.

