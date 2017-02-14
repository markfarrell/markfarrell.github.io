---
layout: post
title:  "Counting Subspaces Over Finite Fields"
date:   2017-02-13
---

Suppose that $$q$$ is an arbitrary prime power, and that $$n, k$$ are arbitrary natural numbers where $$k \leq n$$. Then:

1. $$ { n \brack k }_{q} $$

	$$ = \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} $$

	$$ = \left ( \prod\limits_{j = 1}^{k} \frac{q^{n} - q^{j - 1}}{q^{k} - q^{j - 1}} \right ) \left ( \prod\limits_{j = k + 1}^{n} \frac{q^{n} - q^{j-1}}{q^{k} - q^{j - 1}} \right ) $$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  q^{n} - q^{j - 1} \right )}{\left ( \prod\limits_{j = 1}^{k} q^{k} - q^{j - 1} \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k} - q^{j - 1} \right ) }$$

	$$ = \frac{ \left ( \prod_\limits{j = 1}^{n} q^{j - 1} \right ) \left( \prod\limits_{j = 1}^{n}  q^{n - (j - 1)} - 1 \right )}{\left ( \left ( \prod_\limits{j = 1}^{k} q^{j - 1} \right ) \left ( \prod\limits_{j = 1}^{k} q^{k - (j - 1)} - 1 \right ) \right ) \left ( \left ( \prod_\limits{j = k + 1}^{n} q^{j - 1} \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k - (j - 1)} - 1 \right ) \right ) }$$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  q^{n - (j - 1)} - 1 \right )}{ \left ( \prod\limits_{j = 1}^{k} q^{k - (j - 1)} - 1 \right ) \left ( \prod\limits_{j = k + 1}^{n} q^{k - (j - 1)} - 1 \right ) }$$

	$$ = \frac{ \left( \prod\limits_{j = 1}^{n}  \frac{q^{n - (j - 1)} - 1}{q-1} \right )}{ \left ( \prod\limits_{j = 1}^{k} \frac{q^{k - (j - 1)} - 1}{q-1} \right ) \left ( \prod\limits_{j = k + 1}^{n} \frac{q^{k - (j - 1)} - 1}{q-1} \right ) }$$

	$$ = \frac{ [n]_q ! }{ {[k]_q !} {[n-k]_q !}}$$

2. Assume additionally that $$k < n$$.

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

	$$ \implies { n \brack k }_{q} = {n - 1 \brack k }_{q} + q^{n-k} { n - 1 \brack k - 1 }_{q} = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q}$$


Now, suppose that $$\mathcal{A}$$ is an algebra over a field $$\mathbb{F}$$, $$X,Y \in \mathcal{A}$$, $$q \in \mathbb{F}$$, $$q \neq 1$$, and $$YX = qXY$$.

Assume that $$(X + Y)^k$$ for some $$k \in \mathbb{N} $$. 

$$ \implies (X+Y)^{k+1} $$ 

$$ = \left (\sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-j} \right ) (X + Y) $$

$$ = \sum\limits_{j=0}^{k} \left ( q^{k-j} {k \brack j}_q \right ) X^{(j+1)} Y^{k-j} + \sum\limits_{j=0}^{k} {k \brack j}_q X^j Y^{k-(j-1)} $$

$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=0}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} $$

$$ = \sum\limits_{j=1}^{k} \left ( q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + \sum\limits_{j=1}^{k} \left ( {k \brack j}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

$$ = \sum\limits_{j=1}^{k} \left ({k \brack j} +  q^{k-(j-1)} {k \brack j-1}_q \right ) X^j Y^{k-(j-1)} + Y^{k+1} $$

$$ = \sum\limits_{j=1}^{k} {k+1 \brack j}_q X^j Y^{k-(j-1)} + Y^{k+1} $$

**[** by **2.** **]**

$$ = \sum\limits_{j=0}^{k} {k+1 \brack j}_q X^j Y^{k-(j-1)}$$

$$ \implies (A + B)^n = \sum\limits_{j = 0}^{n} {n \brack j}_q A^j B^{n-j} \text{ for all } n \in \mathbb{N} $$

**[** since clearly $$A + B = {1 \brack 0 }_q A + {1 \brack 1}_q B = \sum\limits_{j = 0}^{1} {1 \brack j}_q A^j B^{1-j}$$ as well **]** .