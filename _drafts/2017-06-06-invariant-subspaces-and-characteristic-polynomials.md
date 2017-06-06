---
layout: post
title:  "Invariant Subspaces and Characteristic Polynomials"
date:   2017-06-06
---

Finite-dimensional vector spaces admit cyclic decompositions, which are direct sum decompositions into invariant subspaces relative to linear operators acting on them. I would now like to use this fact to derive an expression for the characteristic polynomial of a linear operator acting on a finite-dimensional vector space from which it will be immediately apparent that it e.g. satisfies its own characteristic equation.

Suppose that $$T : V \to V$$ is a linear operator acting on a finite-dimensional vector space $$V$$ over a field $$\mathbb{F}$$.
Additionally, suppose that the minimal polynomial of $$T$$ is given by $$p(x) = \prod\limits_{q(x) \in S} \left ( q(x) \right )^{m_q}$$,

letting $$S$$ denote a set of irreducible polynomials in $$\mathbb{F}[x]$$ and $$m_q$$ denote the multiplicity of $$q(x)$$ as a factor of $$p(x)$$ for all $$q(x) \in S$$.

$$ \implies V = \bigoplus\limits_{q(x) \in S} \operatorname{ker} \left ( q(T) \right )^{m_q} = \bigoplus\limits_{q(x) \in S} \operatorname{ker} \left ( q(T) \right )^{\operatorname{dim}(V)}$$

**[** i.e. $$V$$ admits its primary decomposition relative to $$T$$, following from a previous post **]**.

$${\implies}$$ For all $$q(x) \in S$$:

$$\operatorname{ker} \left ( q(T) \right )^{\operatorname{dim}(V)} = \bigoplus_\limits{ v \in U_q } Z(T; v) \text { for some } U_q \subseteq V$$

**[** assuming the fact that finite-dimensional vector spaces admit cyclic decompositions **]**.

Now, let $$U = \bigcup\limits_{q(x) \in S} U_q$$.

$$\implies V = \bigoplus\limits_{v \in U} Z(T; v)$$

$$\implies B := \bigcup\limits_{v \in U} \{ v, Tv, \cdots, T^{\left ( \operatorname{dim}(Z(T;v)) - 1  \right) }v \}$$

is a basis for $$V$$.

$$\implies A := [T]_B = \bigoplus\limits_{v \in U} C_v $$

is a block-diagonal matrix, given here by a Kronecker sum of companion matrices, letting $$C_v := \left [ T \mid_{Z(T;v)} \right ]_B$$ for all $$v\in U$$.

$$\implies \phi(x) := \operatorname{det}(xI - A) $$

$$= \prod\limits_{v \in U } \operatorname{det}(xI - C_v) $$

$$= \prod\limits_{v \in U} p_v(x) $$

$$=  \prod\limits_{q(x) \in S} \left(q(x)\right)^{\operatorname{dim} \left ( \operatorname{ker} \left ( q(T) \right )^{\operatorname{dim}(V)}\right)}$$

is a expression for the characteristic polynomial of $$T$$ of the desired form, letting $$p_v(x)$$ denote the relative minimal polynomial of $$v$$ for all $$v \in U$$.

It is an immediate consequence of the result established in this post that e.g. the minimal polynomial of a linear operator acting on a finite-dimensional vector space divides its characteristic polynomial and hence that it satifies its characteristic equation.

*Note that this post is adapted from one of my selected answers on Quora.*

