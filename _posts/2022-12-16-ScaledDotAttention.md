---
layout: post
title:  Why the attention should be scaled by $\sqrt[]{d}$
date: 2022-12-16 13:15:00
description: Why the attention should be scaled by $\sqrt[]{d}$
tags: DL
categories: learn-ML
---


# Why the attention should be scaled by $\sqrt[]{d}$

The question is answered by [Shurang XIA's blog](https://blog.csdn.net/qq_37430422/article/details/105042303). In this blog, I just remake the proving process so that it seems to clearer for myself.



Question: Why large dot-product value will be generated when the $\sqrt{d_k}$ is large?

Prove: The mean value of $q^Tk=\sum_{i=1}^{d_k}q_ik_i$ is 0, the variance is $d_k$, where $d_k$ is the dimension of vectors $q$ and $k$.

==Assumption:== The elements in query and value are independent random variables that have mean as 0, and variance as 1.



According to the definitions, the two independent random variables have:

$E[X+Y]=E[X]+E[Y]$

$Var(X+Y)=Var(X)+Var(Y)+2Cov(X,Y)=Var(X)+Var(Y)$



According to the definitions, if two random variables $x$ and $y$ are independent, then the covariance should be zero:

$Cov(x,y)=E[(x-E[x])(y-E[y]]=E[xy]-E[x]E[y]=0$

Therefore,

$Cov(q_i,k_i)=0$, and $Cov(q_ik_i,q_jk_j)=0$

Note: If $q_i$ and $k_i$ is independent, then $q_ik_i$ and $q_jk_j$ is independent. This can be proved based on the necessary and sufficient condition of independency of random variables. [see the blog](https://blog.csdn.net/qq_31150463/article/details/85833571)



In addition, because $E[q_i]=0,E[k_i]=0$, we have $E[q_ik_i]=E[q_i]E[k_i]=0$



Now, we can have:

$Var(q_ik_i)=E[(q_ik_i)^2]-(E[q_ik_i])^2=E[q_i^2]E[k_i^2]-(E[q_i]E[k_i])^2=1$

Because:

$Var(q_i)=E[q_i^2]-(E[q_i])^2=E[q_i^2]=1$

$Var(k_i)=Ep[k_i^2]-(E[k_i])^2=E[k_i^2]=1$

$E[q_i]E[k_i]=0$

=> $Var(q_ik_i)=E[q_i^2]E[k_i^2]-(E[q_i]E[k_i])^2=1\times1-0=1$



According to the above process, we have:

$E[q^Tk]=\sum_{i=1}^{d_k}E[q_ik_i]=0$

$Var(q^Tk)=sum_{i=1}^{d_k}[Var(q_1k_1)]=d_k$