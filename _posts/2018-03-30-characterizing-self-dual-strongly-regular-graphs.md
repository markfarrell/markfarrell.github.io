---
layout: post
title:  "Characterizing Self-Dual Strongly Regular Graphs"
date:   2018-03-30
---

I would like to characterize the self-dual strongly regular graphs in terms of their eigenvalues.

The entries of the dual character table of a symmetric coherent algebra can be expressed in terms of the entries its character table:

* Suppose that $$W$$ is a symmetric coherent algebra of order $$n$$ and dimension $$d$$.

	Let $$P \in \operatorname{Mat}_{d \times d}(\mathbb{C})$$ denote the character table of $$W$$ with dual character table $$Q \in \operatorname{Mat}_{d \times d}(\mathbb{C})$$ relative to orderings $$\{ A_{j} : 1 \leq j \leq d \}$$ and $$\{ E_{j} : 1 \leq j \leq d \}$$ on its sets of Schur-primitive and primitive matrices respectively.

	Additionally, let $$v_{j}$$ denote the valency of $$A_{j}$$ and $$m_{j}$$ denote the rank of $$E_{j}$$ for all $$1 \leq j \leq d$$.

	Define the trace inner product $$\langle \cdot, \cdot \rangle : \operatorname{Mat}_{n \times n}(\mathbb{C}) \to \operatorname{Mat}_{n \times n}(\mathbb{C})$$ on $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$: 

	$$\langle A, B \rangle := \operatorname{tr}\left ( B^{*} A \right ) = \operatorname{sum} \left (\overline{B} \circ A \right )$$

	.

	$$ \implies v_{j} Q_{i, j} = \langle E_{i}, A_{j} \rangle = m_{i} P_{j, i} \text{ for all } 1 \leq i, j \leq d $$

	$$ \implies Q = R \circ P^{T}$$, defining $$R \in \operatorname{Mat}_{d \times d}(\mathbb{C})$$, $$R_{i,j} := \frac{m_{i}}{v_{j}}$$.


Now, suppose that $$G$$ is a (connected) strongly regular graph of order $$n \in \mathbb{N}$$ and valency $$k \in \mathbb{N}$$.

$$\implies$$ $$G$$ has three distinct eigenvalues $$\{ k, \lambda, \mu \} $$ for some $$\lambda, \mu \in \mathbb{R}$$.

Let $$j$$ denote the multiplicity of $$\lambda$$ as an eigenvalue of $$G$$.

Following my previous point, it is then possible to derive that

$$ P := \begin{pmatrix} 1 & 1 & 1 \\ k & \lambda & \mu \\ {n - 1 - k} & {-1 -\lambda} & {-1 - \mu } \end{pmatrix}$$

is a character table for the adjacency algebra of $$G$$

with dual character table $$Q :=  \begin{pmatrix} 1 & 1 & 1 \\ 
	j &  \lambda^{'} & \mu^{'} \\
	{n - 1 - j} & {-1 - \lambda^{'}} & {-1 - \mu^{'}} \end{pmatrix}$$.

letting $$\lambda^{'} := \left ( \frac{j}{k} \right ) \lambda$$ and $$\mu^{'} := \left ( \frac{j}{n - 1 - k} \right ) \left ( -1 - \lambda \right )$$.

Recall that $$PQ = nI$$.

$$ \implies \begin{cases}
	k + \left ( \lambda^{'} \right ) \lambda + \left ( -1 - \lambda^{'} \right ) \mu = n \\
	k + \left ( \mu^{'} \right ) \lambda + \left ( -1 - \mu^{'} \right ) \mu = 0
	\end{cases} $$

$$ \implies \left ( \lambda - \mu \right ) \left ( \lambda^{'} - \mu^{'} \right ) = n $$

We also have from this that: $$ k + (j) \lambda + (n - 1 - j) \mu = 0 = j + (k) \lambda^{'} + (n - 1 - k) \mu^{'}$$.

I would then propose that $$G$$ is self-dual if and only if $$ \left ( \lambda - \mu \right )^{2} = n $$:

* Assume that  $$\left ( \lambda - \mu \right )^{2} = n$$ 

	$$ \implies \left ( \lambda - \mu \right )^{2}  = \left ( \lambda - \mu \right ) \left ( \lambda^{'} - \mu^{'} \right ) $$

	$$ \left ( \lambda - \mu \right ) = \left ( \lambda^{'} - \mu^{'} \right ) $$

	**[** since $$\lambda$$ and $$\mu$$ are distinct **]**

	$$ k + (j) \lambda + (n - 1 - j) \mu = 0 = j + (k) \lambda + (n - 1 - k) \mu $$ 

	**[** following my previous point **]**

	$$ \implies (j - k)\left ( 1 - \lambda + \mu \right ) = 0 $$

	$$ \implies j = k $$

	**[** since $$n > 1$$ and $$n = 1$$ otherwise **]**

	$$ \implies Q = \begin{pmatrix} 1 & 1 & 1 \\ 
	k &  \lambda & \left ( \frac{k}{n - 1 - k} \right ) \left ( -1 - \lambda \right ) \\
	{n - 1 - k} & \left ( \frac{n - 1 - k}{k} \right ) \mu  & {-1 - \mu} \end{pmatrix}$$

	$$ \implies \left ( e_{1}^{T} P \right ) \left ( Q e_{2} \right ) = 1 + \lambda + \left ( \frac{n - 1 - k}{k} \right ) \mu  = 0 $$

	$$ \implies P = Q $$

	and hence $$G$$ is self-dual.

It is conversely clear that $$\left ( \lambda - \mu \right )^{2} = n$$ if $$G$$ is self-dual (and hence $$P = Q$$).

So, $$G$$ is indeed self-dual if and only if $$\left ( \lambda - \mu \right )^{2} = n$$.

A first example of a family of self-dual strongly regular graphs is then the [conference graphs](https://en.wikipedia.org/wiki/Conference_graph); I will return to work towards completely classifying the self-dual strongly regular graphs in a future post.


	
