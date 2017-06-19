---
layout: post
title:  "Characterizing Normal Matrices"
date:   2017-06-19
---

I would like to verify the core fact that a complex square matrix is normal if and only if it is unitarily diagonalizable; previously, I have assumed that normal matrices admit their spectral decompositions and would now like to establish this is indeed true in the process of achieving my primary goal for this post.

Suppose that $$n \in \mathbb{N}$$ and that $$A \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ is normal. Let $$ \langle \cdot, \cdot \rangle $$ denote the trace inner product on $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$. 


Then for all $$f(x) \in \mathbb{C}[x]$$:

* Assume that $$ \left ( f (A) \right )^{k+1} = 0$$ for some $$k \in \mathbb{N}$$.

	Let $$ B := \left ( f(A) \right )^{k}$$.

	$$ \implies \langle B^{*} B, B^{*} B \rangle $$

	$$ = \operatorname{tr} \left ( \left ( B^{*} B \right )^{*} B^{*} B \right ) $$

	$$ = \operatorname{tr} \left ( B^{*} \left (B^{2} \right ) B^{*} \right ) $$

	$$ = \operatorname{tr} \left ( B^{*} \left ( \left (f(A) \right )^{2k} \right ) B^{*} \right ) $$

    $$ = \operatorname{tr} \left ( B^{*} \left ( \left (f(A) \right )^{k-1} \right ) \left ( \left (f(A) \right )^{k + 1} \right ) B^{*} \right ) $$

    $$ = \operatorname{tr} \left ( B^{*} \left ( \left (f(A) \right )^{k-1} \right ) \left ( 0 \right ) B^{*} \right ) $$

    $$ = \operatorname{tr}(0) $$

	$$ = 0 $$

	**[** assuming the fact that any polynomial in $$A$$ is normal as well **]**.

	By positive-definiteness of inner products, it follows that:

	$$ B^{*} B = 0 $$

	$$ \implies \langle B, B \rangle $$

	$$ = \operatorname{tr} \left ( B^{*} \ B \right ) $$

	$$ = 0 $$

	$$ \implies \left ( f(A) \right )^{k} = B = 0 $$

Now, let $$p(x) \in \mathbb{C}[x]$$ denote the minimal polynomial of $$A$$.

$$ \implies p(x) = \prod\limits_{\lambda \in S} (x - \lambda)^{m_{\lambda}} \text{ for some } S \subset \mathbb{C} \text { and some } \{ m_{\lambda} : \lambda \in S \} $$

**[** since $$\mathbb{C}$$ is algebraically closed **]**

$$ \implies \sum\limits_{\lambda in S } f_{\lambda}(A) q_{\lambda}(x) = 1 \text { for some } \{ f_{\lambda}(x) : \lambda \in S \} \subset \mathbb{C}[x] $$

**[** letting $$q_{\lambda} := \frac{p(x)}{(x - \lambda)^{m_{\lambda}}}$$ for all $$\lambda \in S$$. by similar reasoning as in a previous post **]**

Next, let $$E_{\lambda} := f_{\lambda}(A) q_{\lambda}(A)$$ for all $$ \lambda \in S $$. 

Then for all $$\lambda \in S$$:

1. $$ \left ( A - \lambda I \right )^{m_{\lambda}} E_{\lambda} $$

	$$ = \left ( \left ( A - \lambda I \right ) E_{\lambda} \right )^{m_{\lambda}} $$

	$$ = 0$$

	**[** observing that $$E_{\lambda}^{2} = E_{\lambda}$$ and that $$E_{\lambda}$$ is a polynomial in $$A$$ **]**.

	$$ \implies \left ( A - \lambda I \right ) E_{\lambda} = 0 $$

	**[** by previous point **]**

	$$ \implies A E_{\lambda} = \lambda \ E_{\lambda} $$

2. $$ \langle (A - \lambda I)^{*} E_{\lambda}, (A - \lambda I)^{*} E_{\lambda} \rangle $$

	$$ = \operatorname{tr} \left ( \left ( (A - \lambda I)^{*} E_{\lambda} \right )^{*} (A - \lambda I)^{*} E_{\lambda} \right ) $$

	$$ = \operatorname{tr} \left ( E_{\lambda}^{*} \left ( (A - \lambda I) E_{\lambda} \right ) (A - \lambda I)^{*} \right ) $$

	$$ = \operatorname{tr} \left ( E_{\lambda}^{*} \left ( 0 \right ) (A - \lambda I)^{*} \right ) $$

	**[** by **1.** **]**

	$$ = \operatorname{tr}(0) $$

	$$ = 0 $$

	$$ \implies (A - \lambda I)^{*} E_{\lambda} = 0 $$

	**[** by positive-definiteness of inner products **]**

	$$ \implies A^{*} E_{\lambda} = \overline{\lambda} \ E_{\lambda}$$


Since $$ \sum\limits_{\lambda \in S} E_{\lambda} = I$$, it then follows that 

$$A = \sum\limits_{\lambda \in S} \lambda \ E_{\lambda} $$ and $$A^{*} = \sum\limits_{\lambda \in S} \overline{\lambda} \ E_{\lambda}$$.

Now, observate that $$E_{\beta} E_{\gamma} = 0$$ for all $$\beta, \gamma \in S$$ such that $$\beta \neq \gamma$$. 

It is consequently possible to deduce that for all $$\alpha \in S$$:

1. $$ \implies E_{\alpha}^{*} = g ( A ) \text { for some } g(x) \in \mathbb{C}[x] $$

	**[** since $$A^{*}$$ is a polynomial in $$A$$ and $$E_{\alpha}^{*} $$ is a polynomial in $$A^{*}$$ **]**

	$$ \implies E_{\alpha}^{*} E_{\alpha} $$

	$$ = g(A) E_{\alpha} $$

	$$ = \left ( \sum\limits_{\beta \in S} g(\beta) E_{\beta} \right ) E_{\alpha} $$

	$$ = g(\alpha) E_{\alpha} $$

	$$ \implies E_{\alpha}^{*} E_{\alpha} $$

	$$ = \left ( E_{\alpha}^{*} E_{\alpha} \right )^{*} $$

	$$ = \overline{g(\alpha)} E_{\alpha}^{*} $$

	$$ \implies E_{\alpha}^{*} E_{\alpha} = E_{\alpha}^{*} E_{\alpha}^{2} = \overline{g(\alpha)} E_{\alpha}^{*} E_{\alpha} $$

	$$ \implies g(\alpha) = \overline{g(\alpha)} = 1 $$

	$$ \implies E_{\alpha}^{*} = E_{\alpha} $$




 
