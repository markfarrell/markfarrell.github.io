---
layout: post
title:  "Counting Subspaces Over Finite Fields"
date:   2017-02-01
---

Suppose that $$q$$ is an arbitrary prime power, and that $$n, k$$ are arbitrary natural numbers. Then:

1. 

2. $$ { n \brack k }_{q} $$

$$ = \left ( \frac{q^{n} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$

$$ = \left ( \frac{q^{n} - q^{n-k} + q^{n-k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$ 

$$ = \left ( \frac{q^{n} - q^{n-k} + q^{n-k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} $$ 

$$ = \left ( \frac{q^{n -k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q} + q^{n-k} \left ( \frac{q^{k} - 1}{q^{k} - 1} \right ) { n - 1 \brack k - 1 }_{q}  $$

$$ = {n - 1 \brack k } + q^{n-k} { n - 1 \brack k - 1 }_{q} $$

when $$k < n$$.

3. $$  { n \brack k }_{q} $$

$$ = \left ( \frac{q^{n} - 1}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$

$$ = \left ( \frac{q^{n} - q^{k} + q^{k} - 1}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$ 

$$ = \left ( \frac{q^{k}(q^{n-k} - 1) + (q^{k} - 1)}{q^{n-k} - 1} \right ) { n - 1 \brack k }_{q} $$

$$ = q^{k} { n - 1 \brack k }_{q} + \left ( \frac{q^{k} - 1}{q^{n-k} - 1} \right) { n - 1 \brack k }_{q} $$

$$ = q^{k} { n - 1 \brack k }_{q} + {n - 1 \brack k - 1}_{q} $$

when $$k < n$$.