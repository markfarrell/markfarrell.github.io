---
layout: post
title:  "Characterizing Normal Matrices"
date:   2017-06-19
---

I would like to verify the core fact that a complex square matrix is normal if and only if it is unitarily diagonalizable; previously, I have assumed that normal matrices admit spectral decompositions and would now like to establish that this is indeed true in the process of achieving my primary goal for this post.

Suppose that $$n \in \mathbb{N}$$ and that $$A \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$. Let $$ \langle \cdot, \cdot \rangle $$ denote the trace inner product on $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$.

Assume that $$A$$ is normal.

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

 $$ \implies p(x) = \prod\limits_{\lambda \in S} (x - \lambda)^{m_{\lambda}} \text{ for some } S \subset \mathbb{C} \text { and some } \{ m_{\lambda} : \lambda \in S \} \subset \mathbb{N}$$ 

 **[** since $$\mathbb{C}$$ is algebraically closed **]**.

$$ \implies \sum\limits_{\lambda \in S } f_{\lambda}(A) q_{\lambda}(x) = 1 \text { for some } \{ f_{\lambda}(x) : \lambda \in S \} \subset \mathbb{C}[x] $$

**[** letting $$q_{\lambda} := \frac{p(x)}{(x - \lambda)^{m_{\lambda}}}$$ for all $$\lambda \in S$$, by similar reasoning as in a previous post **]**.

Next, let $$E_{\lambda} := f_{\lambda}(A) q_{\lambda}(A)$$ for all $$ \lambda \in S $$. 

Then for all $$\lambda \in S$$:

1. $$ \left ( A - \lambda I \right )^{m_{\lambda}} E_{\lambda} $$

	$$ = \left ( \left ( A - \lambda I \right ) E_{\lambda} \right )^{m_{\lambda}} $$

	$$ = 0$$

	**[** observing that $$E_{\lambda}^{2} = E_{\lambda}$$ and that $$E_{\lambda}$$ is a polynomial in $$A$$ **]**.

	$$ \implies \left ( A - \lambda I \right ) E_{\lambda} = 0 $$

	**[** ultimately following from previous point **]**

	$$ \implies A E_{\lambda} = \lambda \ E_{\lambda} $$

2. $$ \langle (A - \lambda I)^{*} E_{\lambda}, (A - \lambda I)^{*} E_{\lambda} \rangle $$

	$$ = \operatorname{tr} \left ( \left ( (A - \lambda I)^{*} E_{\lambda} \right )^{*} (A - \lambda I)^{*} E_{\lambda} \right ) $$

	$$ = \operatorname{tr} \left ( \left ( (A - \lambda I) E_{\lambda} \right ) \left ( (A - \lambda I) E_{\lambda} \right )^{*} \right ) $$

	$$ = \operatorname{tr} \left ( \left ( 0 \right )  \left ( 0 \right )^{*} \right ) $$

	**[** by **1.** **]**

	$$ = \operatorname{tr}(0) $$

	$$ = 0 $$

	$$ \implies (A - \lambda I)^{*} E_{\lambda} = 0 $$

	**[** by positive-definiteness of inner products **]**

	$$ \implies A^{*} E_{\lambda} = \overline{\lambda} \ E_{\lambda}$$


Since $$ \sum\limits_{\lambda \in S} E_{\lambda} = I$$, it then follows that 

$$A = \sum\limits_{\lambda \in S} \lambda \ E_{\lambda} \text{ and } A^{*} = \sum\limits_{\lambda \in S} \overline{\lambda} \ E_{\lambda} \text{ , } $$

which are said to be **spectral decompositions** for $$A$$ and $$A^{*}$$.

Now, observe that $$E_{\beta} E_{\gamma} = 0$$ for all $$\beta, \gamma \in S$$ such that $$\beta \neq \gamma$$. 

It is consequently possible to deduce that for all $$\alpha \in S$$:

1. $$ E_{\alpha}^{*} = g ( A ) \text { for some } g(x) \in \mathbb{C}[x] $$

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

From my previous two points, it is now apparent that with respect to the standard inner product on $$\mathbb{C}^{n}$$:

1. Any column of $$E_{\alpha}$$ is orthogonal to any column of $$E_{\beta}$$ for all $$\alpha, \beta \in S$$ such that $$\alpha \neq \beta$$.

2. It is possible to find an orthonormal basis $$B := \bigcup\limits_{\lambda \in S} B_{\lambda}$$ for $$\mathbb{C}^{n}$$ 
	
	where $$B_{\lambda}$$ is an orthonormal basis for $$\operatorname{col}(E_{\lambda}) = \operatorname{null}(A - \lambda I)$$ for all $$\lambda \in \mathbb{C}$$. 

	$$ \implies P^{*} A P \text{ is a diagonal matrix } $$

	**[** letting $$P \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ denote a change-of-basis matrix from the standard basis for $$\mathbb{C}^{n}$$ to $$B$$, since $$A = \sum\limits_{\lambda \in S} \lambda \ E_{\lambda}$$ **]**.

Hence it can be concluded that $$A$$ is unitarily diagonalizable.

Assume now instead that $$A$$ is unitarily diagonalizable, breaking out of the subcontext where it was assumed that $$A$$ is normal.

$$ \implies A = U D U^{*} $$ 

for some $$U, D \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ such that $$U$$ is unitary and $$D$$ is a diagonal matrix.

$$ \implies A^{*} = U D^{*} U^{*} $$

$$ \implies A A^{*} = U (D D^{*}) U^{*} = U (D^{*} D) U^{*} = A^{*} A $$

**[** observing the fact that diagonal matrices in $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$ commute **]**.

It can then be concluded that $$A$$ is normal in this context.

It now follows in general that a complex square matrix is normal if and only if it is unitarily diagonalizable, as desired.

Note too now that a normal matrix $$A$$ has a *unique* set $$\Sigma(A) := \{ E_{\lambda} : \lambda \in \sigma(A) \}$$ of orthogonal projections onto each of
its respective eigenspaces for its set $$\sigma(A)$$ of eigenvalues:

in fact $$ E_{\lambda} := \left ( \frac{1}{q_{\lambda}(\lambda)} \right ) q_{\lambda}(A) $$ with $$q_{\lambda}(x) := \prod\limits_{ \mu \in \sigma(A) \\ \mu \neq \lambda } \left ( (x - \mu) \right ) $$ for all $$\lambda \in \sigma(A)$$.

I will make use of these facts about normal matrices in future posts.



 
