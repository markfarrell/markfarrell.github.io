---
layout: post
title:  "Counting Subspaces Over Finite Fields"
date:   2017-02-16
---

In this post, my goal is to verify some useful identities that hold about Gaussian binomial coefficients, which are namely used in the context of counting the number of subspaces of certain dimension of a finite-dimensional vector space over a finite field.

Fix a field $$\mathbb{F}$$ and an element $$q \in \mathbb{F} \setminus \{0,1\}$$. 

Define:

1. $${ \cdot \brack \cdot}_q : \mathbb{N} \times \mathbb{N} \to \mathbb{F} $$

	$$ {n \brack k }_q := \begin{cases} \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} & \text{ if } k \leq n \\ 0 & \text{ otherwise } \end{cases}$$

	*Note that in the case that $$\mathbb{F} = \mathbb{R}$$ and $$q$$ is a prime power, then $${n \brack k }_q$$ gives the number of $$k$$-dimensional subspaces of an $$n$$-dimensional vector space over a finite field of order $$q$$ for all $$n,k \in \mathbb{N}$$.*

2. $$ [\cdot]_q ! : \mathbb{N} \to \mathbb{F} $$ 

   $$[n]_q ! := \prod\limits_{j = 1}^{n} {n - (j - 1) \brack 1}_q $$

Then, in this context I would propose that:

1. $$  { n \brack k }_{q} = \frac{ [n]_q ! }{ {[k]_q !} {[n-k]_q !}} $$

	for all $$ n, k \in \mathbb{N} \text{ such that } k < n $$.

2. $$  { n \brack k }_{q} =  {n - 1 \brack k }_{q} + q^{n-k} { n - 1 \brack k - 1 }_{q}  = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q}$$

	for all $$ n, k \in \mathbb{N} \text{ such that } k \leq n $$.

3. For all algebras $$\mathcal{A}$$ over $$\mathbb{F}$$ and $$X, Y \in \mathcal{A}$$ such that $$YX = qXY$$,

	$$ (X + Y)^{n} = \sum\limits_{k = 0}^{n} {n \brack k}_q A^k B^{n-k}$$

	for all $$n \in \mathbb{N}$$.

4. $$ {n \brack k}_q = \sum\limits_{j=0}^{k} q^{(m - j)(k - j)} { n - m \brack k - j }_q { m \brack j }_q $$

	for all $$n, k, m \in \mathbb{N}$$ such that $$m \leq k \leq n$$.

I would now like to verify that these propositions are true in this context. Select an arbitrary $$n \in \mathbb{N}$$. Then:

1. Select arbitrary natural numbers $$n$$ and $$k$$ such that $$k \leq n$$.

	$$ \implies { n \brack k }_{q} $$

	$$ = \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} $$

	$$ = \left ( \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} \right ) \left ( \prod\limits_{j = k + 1}^{n} \frac{q^{n} - q^{j-1}}{q^{k} - q^{j - 1}} \right ) $$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  q^{n} - q^{j - 1} \right )}{\left ( \prod\limits_{j = 1}^{k} q^{k} - q^{j - 1} \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k} - q^{j - 1} \right ) }$$

	$$ = \frac{ \left ( \prod_\limits{j = 1}^{n} q^{j - 1} \right ) \left( \prod\limits_{j = 1}^{n}  q^{n - (j - 1)} - 1 \right )}{\left ( \left ( \prod_\limits{j = 1}^{k} q^{j - 1} \right ) \left ( \prod\limits_{j = 1}^{k} q^{k - (j - 1)} - 1 \right ) \right ) \left ( \left ( \prod_\limits{j = k + 1}^{n} q^{j - 1} \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k - (j - 1)} - 1 \right ) \right ) }$$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  q^{n - (j - 1)} - 1 \right )}{ \left ( \prod\limits_{j = 1}^{k} q^{k - (j - 1)} - 1 \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k - (j - 1)} - 1 \right ) }$$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  \frac{q^{n - (j - 1)} - 1}{q-1} \right )}{ \left ( \prod\limits_{j = 1}^{k} \frac{q^{k - (j - 1)} - 1}{q-1} \right ) \left ( \prod\limits_{j = k + 1}^{n} \frac{q^{k - (j - 1)} - 1}{q-1} \right ) }$$

	$$ = \frac{ [n]_q ! }{ {[k]_q !} {[n-k]_q !}}$$

	and the general result then follows.

2.  Select arbitrary natural numbers $$n$$ and $$k$$ such that $$k < n$$.

    $$ \implies { n \brack k }_{q} $$

	$$ = \left ( \frac{q^{n} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$

	$$ = \left ( \frac{q^{n} - q^{n-k} + q^{n-k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$ 

	$$ = \left ( \frac{q^{n-k}(q^{k} - 1) + (q^{n-k} - 1)}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$ 

	$$ = \left ( \frac{q^{n -k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} + q^{n-k} \left ( \frac{q^{k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q}  $$

	$$ = {n - 1 \brack k }_{q} + q^{n-k} { n - 1 \brack k - 1 }_{q} $$

	and 

	$$  { n \brack k }_{q} $$

	$$ = \left ( \frac{q^{n} - 1}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$

	$$ = \left ( \frac{q^{n} - q^{k} + q^{k} - 1}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$ 

	$$ = \left ( \frac{q^{k}(q^{n-k} - 1) + (q^{k} - 1)}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$

	$$ = q^{k} { n - 1 \brack k }_{q} + \left ( \frac{q^{k} - 1}{q^{n-k} - 1} \right) { n - 1 \brack k }_{q} $$

	$$ = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q} $$

	$$ \implies  { n \brack k }_{q} =  {n - 1 \brack k }_{q} + q^{n-k} { n - 1 \brack k - 1 }_{q}  = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q}$$

	and the general result then follows.

3. Suppose that $$\mathcal{A}$$ is an algebra over $$\mathbb{F}$$, $$X,Y \in \mathcal{A}$$, $$q \in \mathbb{F}$$, and $$YX = qXY$$.

	Assume that $$(X + Y)^k$$ for some $$k \in \mathbb{N} $$. 

	$$ \implies (X+Y)^{k+1} $$ 

	$$ = \left (\sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-j} \right ) (X + Y) $$

	$$ = \sum\limits_{j=0}^{k} \left ( q^{k-j} {k \brack j}_q \right ) X^{(j+1)} Y^{k-j} + \sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-(j-1)} $$

	$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=0}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} $$

	$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=1}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

	$$ = \sum\limits_{j=1}^{k} \left ({k \brack j} +  q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

	$$ = \sum\limits_{j=1}^{k} {k+1 \brack j}_q X^j Y^{k-(j-1)} + Y^{k+1} $$

	**[** by **2.** **]**

	$$ = \sum\limits_{j=0}^{k} {k+1 \brack j}_q X^j Y^{(k+1) - j}$$

	$$ \implies (A + B)^n = \sum\limits_{j = 0}^{n} {n \brack j}_q A^j B^{n-j} \text{ for all } n \in \mathbb{N} $$

	**[** since clearly $$A + B = {1 \brack 0 }_q A + {1 \brack 1}_q B = \sum\limits_{j = 0}^{1} {1 \brack j}_q A^j B^{1-j}$$ as well **]** .