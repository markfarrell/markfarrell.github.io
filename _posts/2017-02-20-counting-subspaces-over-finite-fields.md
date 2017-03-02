---
layout: post
title:  "Counting Subspaces Over Finite Fields"
date:   2017-02-20
---

In this post, my goal is to verify some useful identities that hold about Gaussian binomial coefficients, which are namely used in the context of counting the number of subspaces of a certain dimension of a finite-dimensional vector space over a finite field.

Fix a prime power $$q$$.

Define:

1. $${ \cdot \brack \cdot}_q : \mathbb{N}_{0} \times \mathbb{N}_{0} \to \mathbb{R} $$

	$$ {n \brack k }_q := \begin{cases} \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} & \text{ if } 0 < k \leq n \\ 1 & \text { if } k = 0 \\ 0 & \text{ otherwise } \end{cases}$$

	*Note that $${n \brack k }_q$$ gives the number of $$k$$-dimensional subspaces of an $$n$$-dimensional vector space over a finite field of order $$q$$ for all $$n,k \in \mathbb{N}$$.*

2. $$ [\cdot]_q ! : \mathbb{N}_{0} \to \mathbb{R} $$ 

   $$[n]_q ! := \begin{cases} \prod\limits_{j = 1}^{n} {n - (j - 1) \brack 1}_q & \text{ if } n \in \mathbb{N} \\ 1 & \text{ if } n = 0 \end{cases} $$

Then, in this context I would propose that:

1. $$  { n \brack k }_{q} = \frac{ [n]_q ! }{ {[k]_q !} {[n-k]_q !}} $$

	for all $$ n, k \in \mathbb{N} \text{ such that } k \leq n $$.

2. $$  { n \brack k }_{q} =  {n - 1 \brack k }_{q} + q^{n-k} { n - 1 \brack k - 1 }_{q}  = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q}$$

	for all $$ n, k \in \mathbb{N} \text{ such that } k < n $$.

3. For all algebras $$\mathcal{A}$$ over $$\mathbb{R}$$ and $$X, Y \in \mathcal{A}$$ such that $$YX = qXY$$,

	$$ (X + Y)^{n} = \sum\limits_{k = 0}^{n} {n \brack k}_q X^k Y^{n-k}$$

	for all $$n \in \mathbb{N}$$.

4. $$ {n \brack k}_q = \sum\limits_{j=0}^{m} q^{(m - j)(k - j)} { m \brack j }_q  { n - m \brack k - j }_q $$

	for all $$n, k, m \in \mathbb{N}$$ such that $$m \leq k \leq n$$.

I would now like to verify that these propositions are true in this context. Then:

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

3. Suppose that $$\mathcal{A}$$ is an algebra over $$\mathbb{R}$$, $$X,Y \in \mathcal{A}$$, and $$YX = qXY$$.

	Assume that $$(X + Y)^k = \sum\limits_{j = 0}^{k} {k \brack j}_q X^j Y^{k-j}$$ for some $$k \in \mathbb{N} $$. 

	$$ \implies (X+Y)^{k+1} $$ 

	$$ = \left (\sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-j} \right ) (X + Y) $$

	$$ = \sum\limits_{j=0}^{k} \left ( q^{k-j} {k \brack j}_q \right ) X^{(j+1)} Y^{k-j} + \sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-(j-1)} $$

	$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=0}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} $$

	$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=1}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

	$$ = \sum\limits_{j=1}^{k} \left ({k \brack j} +  q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

	$$ = \sum\limits_{j=1}^{k} {k+1 \brack j}_q X^j Y^{k-(j-1)} + Y^{k+1} $$

	**[** by **2.** **]**

	$$ = \sum\limits_{j=0}^{k} {k+1 \brack j}_q X^j Y^{(k+1) - j}$$

	$$ \implies (X + Y)^n = \sum\limits_{j = 0}^{n} {n \brack j}_q X^j Y^{n-j} \text{ for all } n \in \mathbb{N} $$

	**[** since clearly $$X + Y = {1 \brack 0 }_q X + {1 \brack 1}_q Y = \sum\limits_{j = 0}^{1} {1 \brack j}_q X^j Y^{1-j}$$ as well **]** .

4. Select arbitrary $$n, k \in \mathbb{N}$$ such that $$k \leq n$$, and assume that $$ {n \brack k}_q = \sum\limits_{j=0}^{r} q^{(r - j)(k - j)} { r \brack j }_q  { n - r \brack k - j }_q $$ for some $$ r < k $$.

	$$ \implies {n \brack k}_q $$ 

	$$ = \sum\limits_{j=0}^{r} \left ( q^{(r - j)(k - j)} { r \brack j }_q \right ) { n - r \brack k - j }_q  $$

	$$ = \sum\limits_{j=0}^{r} \left ( q^{(r - j)(k - j)} { r \brack j }_q \right ) \left ( q^{(k - j)} { n - (r+1) \brack k - j }_q + { n - (r + 1) \brack k - (j+1) }_q \right ) $$

	**[** by **2.** **]**

	$$ = \sum\limits_{j=0}^{r} \left ( q^{((r+1) - j)(k - j)} { r \brack j }_q \right ) { n - (r+1) \brack k - j }_q + \sum\limits_{j=0}^{r} \left ( q^{(r - j)(k - j)} { r \brack j }_q \right ) { n - (r+1) \brack k - (j+1) }_q $$ 


	$$ = \sum\limits_{j=0}^{r} \left ( q^{((r+1) - j)(k - j)} { r \brack j }_q \right ) { n - (r+1) \brack k - j }_q + \sum\limits_{j=1}^{r+1} \left ( q^{(r - (j - 1))(k - (j-1))} { r \brack (j - 1) }_q \right ) { n - (r+1) \brack k - j }_q $$

	$$ = q^{(r+1)(k)} {n - (r+1) \brack k}_q + \sum\limits_{j=1}^{r} \left ( q^{((r+1) - j)(k - j)} { r \brack j }_q  + q^{(r - (j - 1))(k - (j-1))} { r \brack (j - 1) }_q\right ) { n - (r+1) \brack k - j }_q + { n - (r+1) \brack k - (r+1)}_q $$

	$$ = q^{(r+1)(k)} {n - (r+1) \brack k}_q + \sum\limits_{j=1}^{r} \left ( q^{((r+1) - j)(k - j)} \left ( { r \brack j }_q  + q^{(r + 1) - j} { r \brack (j - 1) }_q\right ) \right) { n - (r+1) \brack k - j }_q + { n - (r+1) \brack k - (r+1)}_q $$

	$$ = q^{(r+1)(k)} {n - (r+1) \brack k}_q + \sum\limits_{j=1}^{r} \left ( q^{((r+1) - j)(k - j)} { r + 1 \brack j }_q \right ) { n - (r+1) \brack k - j }_q + { n - (r+1) \brack k - (r+1)}_q $$

	**[** again by **2.** **]**

	$$ = \sum\limits_{j=0}^{r+1} q^{((r + 1) - j)(k - j)} { r + 1 \brack j }_q { n - (r + 1) \brack k - j }_q  $$

	as well.

	$$ \implies {n \brack k}_q = \sum\limits_{j=0}^{m} q^{(m - j)(k - j)} { m \brack j }_q  { n - m \brack k - j }_q \text { for all } m \leq k \leq n $$

	**[** since, by **2.**, it is also the case that $${n \brack k }_q = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q} = \sum\limits_{j=0}^{m} q^{(m - j)(k - j)} { m \brack j }_q  { n - m \brack k - j }_q$$ when $$m = 1$$ **]**.

	The general result then follows, since $$n$$ and $$k$$ are arbitrary.