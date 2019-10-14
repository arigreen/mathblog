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

## Solution 29
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

