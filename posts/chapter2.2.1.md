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
Subtracting **$l_{21}=5$** copies of equation 1 from equation 2 will eliminate $x$ from the
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

