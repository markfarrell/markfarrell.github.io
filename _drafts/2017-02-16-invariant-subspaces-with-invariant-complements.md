---
layout: post
title:  "Invariant Subspaces With Invariant Complements"
date:   2017-02-16
--- 

Suppose that $$V$$ is a finite-dimensional vector space over a field $$\mathbb{F}$$.

Then, in this context, I would propose that:

1. For all linear operators $$L : V \to V$$, if the minimal polynomial of $$L$$ is irreducible over $$\mathbb{F}$$ then every $$L$$-invariant subpace of $$V$$ has an $$L$$-invariant complement.

2. For all linear operators $$L : V \to V$$, if the minimal polynomial of $$L$$ splits into distinct linear factors over $$\mathbb{F}$$ then every $$L$$-invariant subpace of $$V$$ has an $$L$$-invariant complement.

I would now like to verify that these propositions are indeed true in this context:

1. Suppose that $$L : V \to V$$ is an arbitrary linear operator whose minimal polynomial $$p(x)$$ is irreducible over $$\mathbb{F}$$, and $$\operatorname{deg}(p(x)) > 1$$.

	$$ \implies \mathbb{F}[x]/_{p(x)} = \{ [q(x)] : q(x) \in \mathbb{F}[x] \operatorname{and} \operatorname{deg}(q(x)) < \operatorname{deg}(p(x)) \} \text { is a field }$$

	**[** defining addition and multiplication in the usual way for polynomial quotient rings, since $$p(x)$$ is irreducible over $$\mathbb{F}$$**]**.

	Next, define:

	 $$ (\star) : \left ( \mathbb{F}[x]/_{p(x)} \right ) \times V \to V $$ 

	 $$ [q(x)] \star v := (q(L))(v) $$

	$$ \implies V \text{ is a vector space over } \mathbb{F}[x]/_{p(x)} $$

	**[** with scalar multiplication given by $$(\star)$$ and vector addition again given by $$(+)$$ **]**.

	Now, suppose that $$W$$ is an arbitrary $$L$$-invariant subspace of $$V$$ over $$\mathbb{F}$$.

	$$ \implies V = W \oplus W' $$ 

	**[** for some subspace $$W'$$ of $$V$$ **]**.

	$$ \implies W' \text { is a subspace of } V \text { over } \mathbb{F}[x]/_{p(x)} \text { as well } $$

	$$ \implies L(w') = [q(x)] \star w' \in W' \text { for all } w' \in W' $$

	**[** for some $$[q(x)] \in \mathbb{F}[x]/_{p(x)}$$, since $$\operatorname{deg}(p(x)) > 1$$ **]**.

	$$ \implies W' \text{ is } L\text{-invariant}$$

	$$ \implies W \text{ has an } L\text{-invariant} \text{ complement } $$

	The general result then follows since $$L$$ and $$W$$ are arbitrary - noting that it is also clear that every invariant subspace of a linear operator  acting on $$V$$ with a degree-one minimal polynomial has an invariant complement.

2. Suppose that $$L : V \to V$$ is an arbitrary linear operator whose minimal polynomial $$p(x)$$ splits into distinct linear factors as $$p(x) = \prod_\limits{\lambda\in \sigma(L)} (x - \lambda) $$ where $$\sigma(L)$$ denotes the set of eigenvalues of $$L$$, and suppose that $$W$$ is an arbitrary $$L$$-invariant subspace of $$V$$. Additionally, let $$\{ E_{\lambda} : \lambda \in \sigma(L) \}$$ denote the set of spectral idempotents of $$L$$ (where $$E_{\lambda} := \frac{1}{q_{\lambda}(\lambda)} q(L)$$ and $$q_{\lambda}(x) := \frac{p(x)}{(x - \lambda)}$$ for all $$\lambda \in \sigma(L)$$).

	$$ \implies V = W \oplus W' \text{ for some } W' \leq V $$

	Now, select an arbitrary $$\mu \in \sigma(L)$$ and an arbitrary $$w' \in \operatorname{image}(E_{\mu}) \cap W'$$.

	$$ \implies w' = E_{\mu}(v) \text { for some } v \in V $$

	**[** since $$W_{\mu}' \leq $$\operatorname{image}(E_{\mu})$$ **]**

	$$ \implies L(w') $$

	$$ = \left ( \sum\limits_{\lambda \in \sigma(L)} \lambda E_{\lambda} \right )(w') $$

	**[** assuming that $$L$$ has its spectral decomposition, from previous posts **]**

	$$ = \left ( \sum\limits_{\lambda \in \sigma(L)} \lambda E_{\lambda} \right )(E_{\mu}(v)) $$

	$$ = \left ( \sum\limits_{\lambda \in \sigma(L)} \lambda E_{\lambda} \right )(E_{\mu}(v)) $$

	$$ = \mu E_{\mu}(v) $$

	**[** since $$E_{\mu} E_{\lambda} = 0$$ for all $$ \lambda \in \sigma(L) \setminus \{\mu\} $$ and $$E_{\mu}^{2} = E_{\mu}$$ **]**

	$$ = \mu w' \in \operatorname{image}(E_{\mu}) \cap W' $$

	$$ \implies \operatorname{image}(E_{\mu}) \cap W' \text{ is } L\text{-invariant} $$

	**[** since $$w'$$ is arbitrary **]**

	$$ \implies \operatorname{image}(E_{\lambda}) \cap W' \text{ is } L\text{-invariant} \text{ for all } \lambda \in \sigma(L)$$

	**[** since $$\mu$$ is arbitrary as well **]**

	$$ \implies W' $$

	$$ = V \cap W' $$

	$$ = \left ( \bigoplus\limits_{\lambda \in \sigma(L)} \operatorname{image}(E_{\lambda}) \right ) \cap W' $$

	$$ = \bigoplus\limits_{\lambda \in \sigma(L)} \operatorname{image}(E_{\lambda}) \cap W' $$

	$$ \text {is } L\text{-invariant} $$

	**[** assuming the fact that the sum of finite number of $$L$$-invariant subspaces is $$L$$-invariant **]**

	$$ \implies W \text{ has an } L\text{-invariant complement}$$

	The general result then follows, since $$L$$ and $$W$$ in this context are arbitrary.






