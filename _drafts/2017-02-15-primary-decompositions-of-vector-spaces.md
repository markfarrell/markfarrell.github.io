---
layout: post
title:  "Primary Decompositions of Vector Spaces"
date:   2017-02-15
---

Suppose that $$L : V \to V$$ is a linear operator acting on a finite-dimensional vector space $$V$$ over a field $$\mathbb{F}$$. Additionally, suppose that the minimal polynomial of $$L$$ is given by $$p(x) = \left ( \prod\limits_{q \in S} q^{m_q} \right )(x)$$, where $$S$$ denotes the set of irreducible factors of $$p$$, and $$m_q$$ denotes the multiplicity of $$q$$ as a factor of $$p$$ for all $$q \in S$$.

Then it is apparent that the set of polynomials $$\left \{ \frac{p}{q^{m_q}} : q \in S \right \}$$ is coprime.

$$ \implies \sum\limits_{q(x) \in S} f_q(x) \left ( \frac{p}{q^{m_q}} \right )(x) = 1 $$ for some $$f_q(x) \in \mathbb{F}[x]$$ for each $$q \in S$$

**[** by the analogue of Bézout's identity for polynomials in $$\mathbb{F}[x]$$ **]**.

Now, let $$E_q = f_q(L) \left ( \frac{p}{q^{m_q}} \right )(L) $$ for each $$q \in S$$. Then:

1. $$ \sum\limits_{q \in S} E_q = I $$

2. For all $$q_1, q_2 \in S$$ such that $$q_1 \neq q_2$$, 

	$$ E_{q_1} E_{q_2} $$

	$$ = \left ( f_{q_1}(L) \left ( \frac{p}{q_{1}^{m_{q_1}}} \right )(L) \right ) \left ( f_{q_2}(L) \left ( \frac{p}{q_{2}^{m_{q_2}}} \right )(L) \right ) $$

	$$ = p(L) \left ( f_{q_1}(L) f_{q_2}(L) \left ( \frac{p}{q_{1}^{m_{q_1}} q_{2}^{m_{q_2}}} \right )(L) \right ) $$

	$$ = 0 $$

**[** since $$p$$ is the minimal polynomial of $$L$$ and hence $$p(L) = 0$$ by definition **]**.

3. For all $$q \in S$$: 

	$$\operatorname{image}(E_q) $$

	$$ = \{ u : u = E_q(v) \text{ for some } v \in V \} $$

	$$ = \{ u : q^{m_q}(L)(u) = (q^{m_q}(L) E_q)(v) = p(L)(v) = 0 \text{ for some } v \in V \} $$

	$$ = \operatorname{ker}(q^{m_q}(L))$$

$$ \implies V = \bigoplus\limits_{q \in S}  \operatorname{image}(E_q) = \bigoplus\limits_{q \in S} \operatorname{ker}(q^{m_q}(L)) $$

The direct sum decomposition $$V = \bigoplus\limits_{q \in S} \operatorname{ker}(q^{m_q}(L))$$ is said to be the **primary decomposition** of $$V$$ relative to $$L$$. *It is useful to note that it also follows from **1.**, **2.** and **3.** that for all $$q \in S$$, $$E_q$$ is a projection onto the component part $$\operatorname{ker}(q^{m_q}(L))$$ of the primary decomposition of $$V$$ relative to $$L$$*.

Since $$V$$ is arbitrary, it follows that finite-dimensional vector spaces have primary decompositions relative to linear operators acting on them in general, and moreover that projections onto component parts of primary decompositions of finite-dimensional vector spaces can also be found in general using the method discussed in this post.








