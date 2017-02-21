---
layout: post
title:  "Primary Decompositions of Vector Spaces"
date:   2017-02-21
---

Suppose that $$L : V \to V$$ is a linear operator acting on a finite-dimensional vector space $$V$$ over a field $$\mathbb{F}$$. Additionally, suppose that the minimal polynomial of $$L$$ is given by $$p(x) = \prod\limits_{q(x) \in S} \left ( q(x) \right )^{m_q} $$, where $$S$$ denotes the set of irreducible factors of $$p(x)$$, and $$m_q$$ denotes the multiplicity of $$q(x)$$ as a factor of $$p(x)$$ for all $$q(x) \in S$$.

Then it is apparent that the set of polynomials $$\left \{ \left ( \frac{p}{q^{m_q}} \right)(x) : q(x) \in S \right \}$$ is coprime.

$$ \implies \sum\limits_{q(x) \in S} f_q(x) \left ( \frac{p}{q^{m_q}} \right )(x) = 1 $$ for some $$f_q(x) \in \mathbb{F}[x]$$ for each $$q(x) \in S$$

**[** by the analogue of Bézout's identity for polynomials in $$\mathbb{F}[x]$$ **]**.

Now, let $$E_q = f_q(L) \left ( \left ( \frac{p}{q^{m_q}} \right)(x) \right )(L) $$ for each $$q(x) \in S$$. Then:

1. $$ \sum\limits_{q(x) \in S} E_q = I $$

2. For all $$q_1(x), q_2(x) \in S$$ such that $$q_1(x) \neq q_2(x)$$, 

	$$ E_{q_1} E_{q_2} $$

	$$ = \left ( f_{q_1}(L) \left ( \frac{p}{q_{1}^{m_{q_1}}} \right )(L) \right ) \left ( f_{q_2}(L) \left ( \frac{p}{q_{2}^{m_{q_2}}} \right )(L) \right ) $$

	$$ = p(L) \left ( f_{q_1}(L) f_{q_2}(L) \left ( \frac{p}{q_{1}^{m_{q_1}} q_{2}^{m_{q_2}}} \right )(L) \right ) $$

	$$ = 0 $$

**[** since $$p(x)$$ is the minimal polynomial of $$L$$ and hence $$p(L) = 0$$ by definition **]**.

3. For all $$q(x) \in S$$: 

	$$\operatorname{image}(E_q) $$

	$$ = \{ u : u = E_q(v) \text{ for some } v \in V \} $$

	$$ = \{ u : \left ( q(L) \right )^{m_q} (u) = (\left ( q(L) \right )^{m_q}  E_q)(v) = p(L)(v) = 0 \text{ for some } v \in V \} $$

	$$ = \operatorname{ker} \left ( q(L) \right )^{m_q} $$

$$ \implies V = \bigoplus\limits_{q(x) \in S}  \operatorname{image}(E_q) = \bigoplus\limits_{q(x) \in S} \operatorname{ker} \left ( q(L) \right )^{m_q}  $$

The direct sum decomposition $$V = \bigoplus\limits_{q(x) \in S} \operatorname{ker}\left ( q(L) \right )^{m_q} $$ is said to be the **primary decomposition** of $$V$$ relative to $$L$$. *It is useful to note that it also follows from **1.**, **2.** and **3.** that for all $$q(x) \in S$$, $$E_q$$ is a projection onto the component part $$\operatorname{ker} \left ( q(L) \right )^{m_q} $$ of the primary decomposition of $$V$$ relative to $$L$$*.

Since $$V$$ is arbitrary, it follows that finite-dimensional vector spaces have primary decompositions relative to linear operators acting on them in general, and moreover that projections onto component parts of primary decompositions of finite-dimensional vector spaces can also be found in general using the method discussed in this post.








