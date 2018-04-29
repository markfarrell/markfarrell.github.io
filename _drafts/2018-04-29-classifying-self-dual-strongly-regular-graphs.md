---
layout: post
title:  "Classifying Self-Dual Strongly Regular Graphs"
date:   2018-04-29
---

I would like to completely classify the self-dual strongly regular graphs: i.e. determine that a strongly regular graph
is self-dual if and only if it falls into one of finitely many families of strongly-regular graphs.

To this end, I would first like to derive some feasability conditions that the parameters of a self-dual strongly regular graph must satisfy,
using the characterization of self-dual strongly regular graphs that I established in my previous post based on their eigenvalues.

Suppose that $$G$$ is a self-dual strongly regular graph with adjacency matrix $$A$$.

Let $$\{k, \lambda, \mu \} \in \mathbb{R}$$ denote the set of distinct eigenvalues of $$G$$, with $$G$$ being self-dual with respect

to character table $$ P := \begin{pmatrix} 1 & 1 & 1 \\ k & \lambda & \mu \\ {n - 1 - k} & {-1 -\lambda} & {-1 - \mu } \end{pmatrix}$$.

Additionally, let $$\left \{ \frac{1}{n} J, E_{\lambda}, E_{\mu} \right \}$$ denote the set of primitive matrices in the adjacency algebra of $$G$$, with $$A = k \left ( \frac{1}{n} J \right ) + \lambda E_{\lambda} + \mu E_{mu}$$.

$$ \implies E_{\lambda} = \left ( \frac{1}{q(\lambda)} \right ) q(A) \text{ where } q(x) := (x - k) (x - \mu ) \in \mathbb{C}[x] $$

**[** from previous post, since $$A$$ is a real symmetric matrix and hence a normal matrix **]**.

$$ \implies E_{\lambda} = \left ( \frac{\beta}{(\lambda - k)(\lambda - \mu)} \right ) \overline{A} + \left ( \frac{\alpha - k - \mu}{(\lambda - k)(\lambda - \mu)} \right ) A + \left ( \frac{k(1 + \mu)}{(\lambda - k)(\lambda - \mu)}\right ) I $$

**[** with $$G$$ an $$\operatorname{SRG}(n, k, \alpha, \beta)$$ **]**

$$ = \left ( \frac{\mu}{n} \right ) \overline{A} + \left ( \frac{\lambda}{n} \right ) A + \left ( \frac{k}{n} \right ) I $$

**[** since $$G$$ is self-dual **]**.

$$ \implies (1 + \mu) = \frac{(\lambda -k)}{(\lambda - \mu)} $$

$$ \implies \beta = \mu (\mu + 1) $$

Now, in my previous post I established that conference graphs are self-dual strongly regular graphs.

Assume that $$G$$ is not a conference graph.

Recall the following fact about the spectrum of the self-dual strongly regular graph $$G$$: $$\lambda, \mu \in \left \{ \frac{(\alpha - \beta) \pm \sqrt{n}}{2} \right \}$$ with $$n = (\alpha - \beta)^{2} + 4(k - \beta)$$.

By properties of the dual character table of $$P$$ established in my previous post, it would be necessariy that $$k = \left ( \frac{n - 1}{2} \right ) $$ if $$(\alpha - \beta) = -1$$ and hence $$G$$ would be a conference graph.

Since $$G$$ is not a conference graph, it can then ultimately be deduced that $$\sqrt{n}$$ is rational and is hence moreover an integer, following from my previous point that $$\beta = \mu (\mu + 1)$$.

Observe that the multiplicities of $$\lambda$$ and $$\mu$$ are $$k$$ and $$n - 1 - k$$, since the dual character table of $$P$$ is $$P$$.

$$ \implies k \in \left \{ \left ( \frac{(n-1)}{2} \right ) \pm \left ( \frac{2k + (n - 1)(\alpha - \beta)}{\sqrt{n}} \right ) \right \}$$

**[** by properties of the multiplicities of eigenvalues of strongly regular graphs **]**.

Observe too that $$(-1 - \lambda) =  \left ( \frac{n - 1 - k}{k} \right ) \mu$$ from the character-and-dual-character table $$P$$ of $$G$$.

Recall the fact that $$(n - 1 - k)\beta = k(k - \alpha - 1)$$ since $$G$$ is strongly regular.

Let $$m := \sqrt{n} \in \mathbb{Z}$$.

Then either:

* $$\lambda = \left ( \frac{(\alpha - \beta) - m}{2} \right )$$ and $$\mu = \left ( \frac{(\alpha - \beta) + m}{2} \right )$$.
	
	$$ \implies \left ( \frac{m}{2} \right ) - \left ( \frac{(m+2)}{(m + 1)(m-1)} \right ) k $$

	$$ = (\alpha - \beta) $$

	$$ = \left ( \frac{2k}{m - 1} \right ) - m$$

	 **[** following from my previous two observations **]**.

	 Now, let $$\gamma := \left ( \frac{k}{m - 1} \right )$$.

	 $$ \implies \beta = \frac{1}{4} \left ( (\alpha - \beta)^{2} + 4k - m^{2} \right ) $$

	 $$ = \gamma \left ( \gamma - 1 \right ) $$

	 with $$ \gamma = \frac {3m(m+1)}{2(3m + 4)} \in \mathbb{N}$$.

	 And, $$(n - 1 - k)\beta = k(k - \alpha - 1)$$.

	 $$ \implies (m + 1 - \gamma)(\gamma - 1) = (m - 1)\gamma - \alpha - 1 $$

	 $$ \implies \alpha = \left ( \gamma - 1 \right ) \left ( \gamma - 2 \right ) + (m - 2) $$

* $$\lambda = \left ( \frac{(\alpha - \beta) + m}{2} \right )$$ and $$\mu = \left ( \frac{(\alpha - \beta) - m}{2} \right )$$.
	
	$$ \implies k \left ( \frac{(m - 2)}{(m + 1)( m - 1)} \right ) - \left ( \frac{m}{2} \right )$$

	$$ = (\alpha - \beta) $$

	$$ = m - \left ( \frac{2k}{(m-1)} \right )$$

	 **[** again, following from my previous two observations **]**.

	From the right-hand side of this equation, it is then possible to similarly derive that 

	$$\alpha = \left ( \gamma - 1 \right ) \left ( \gamma - 2 \right ) + (m - 2) $$ 
	and $$ \beta = \gamma(\gamma - 1) $$ with $$ \gamma = \frac {3m(m+1)}{2(2m + 3)} \in \mathbb{N}$$ as well.

It can then ultimately be concluded in general that a strongly regular graph is self-dual if and only if it is either a conference graph or an $$\operatorname{SRG} \left ( m^{2}, \ (m - 1) \gamma, \ \left ( \gamma - 1 \right ) \left ( \gamma - 2 \right ) + (m - 2) , \gamma (\gamma - 1) \right )$$ with $$\gamma \in \left \{  \left ( \frac {3m(m+1)}{2(3m + 4)} \right ), \left ( \frac {3m(m+1)}{2(2m + 3)} \right )\right  \}$$ for some $$m \in \mathbb{N}$$.

With that being said, it may still be possible to further classify the latter kind of self-dual strongly graph in terms of e.g. other 
familiar families of strongly regular graphs arising from various combinatorial constructions; I may return to this point in a future post.









