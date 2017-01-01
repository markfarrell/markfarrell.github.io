---
layout: post
title:  "Strongly Regular Grassman Graphs"
date:   2016-12-31
---

1. For all natural numbers $$n \geq 4$$ and prime powers $$q$$, 
$$\operatorname{Grassman}\left ( n, q, 2 \right)$$ is an $$\operatorname{SRG}\left ( {n \brack 2}_{q}, q^{2} {2 \brack 1}_{q}  {n - 2 \brack 1}_{q} , q^{2} {n - 2 \brack 1}_{q} + q^{2} - 1, \left ( {2 \brack 1}_{q} \right )^{2} \right)$$.

Suppose that we are given an arbitrary natural number $$n \geq 4$$ and prime power $$q$$. Let $$S = \{ W : W \leq V \operatorname{and} \operatorname{dim}{W} = 2  \}$$ denote the set of all subspaces of dimension $$2$$ of the vector space $$V = \mathbb{F}_{q}^{n}$$ over the finite field $$\mathbb{F}_{q}$$ of order $$q$$. Consider the simple graph $$G = (S, E)$$ formed with the set $$S$$ as vertices and the set $$E = \{ \{W, Z\} : W, Z \in S \operatorname{and} \operatorname{dim}(W \cap Z) = 1 \}$$ as edges. Then:

1. Select an arbitrary $$W \in S$$. Then there are $$\mid V \setminus W \mid$$ = $$\mid V\mid - \mid W \mid$$ = $$q^{n} - q^{2}$$ ways to select a vector in $$V$$ that is not also a vector in $$W$$, and for each $$v \in V \setminus W$$ there are $$q-1$$ other vectors in $$V \setminus W$$ that are non-zero scalar multiples of $$v$$. This means that there are $${2 \brack 1}_{q} \frac{\mid V \setminus W \mid}{q-1}$$ ways to select a one-dimensional subspace $$Y \leq W$$ of $$W$$ and then select another one-dimensional subspace $$Z \leq V$$ of $$V$$ where $$W \cap Z = \{ 0 \}$$ in order to construct a two-dimensional subspace $$Y \oplus Z \in S$$ of $$V$$ such that $$\operatorname{dim}(W \cap (Y \oplus Z)) = \operatorname{dim}(W \cap Y) = 1 $$. Hence $$W$$ is adjacent to $${2 \brack 1}_{q} \frac{\mid V \setminus W \mid}{q-1} = {2 \brack 1}_{q} \frac{q^{n} - q^{2}}{q-1} = {2 \brack 1}_{q} \frac{q^{2}\left(q^{n-2} - 1 \right)}{q-1} = q^{2} {2 \brack 1}_{q} {n-2 \brack 1}_{q}$$ vertices in $$S$$, which is independent of $$W$$ itself; therefore we ultimately have that $$G$$ is $$q^{2} {2 \brack 1}_{q} {n-2 \brack 1}_{q}$$-regular.

2.