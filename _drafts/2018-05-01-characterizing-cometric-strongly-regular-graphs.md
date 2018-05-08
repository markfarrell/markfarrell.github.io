---
layout: post
title:  "Characterizing Cometric Strongly Regular Graphs"
date:   2018-05-01
---

I would like to characterize the cometric strongly graphs in terms of their eigenvalue multiplicities.

Suppose that $$G$$ is a (connected) $$k$$-valent strongly regular graph of order $$n$$ with character table $$ P := \begin{pmatrix} 1 & 1 & 1 \\ k & \lambda & \mu \\ {n - 1 - k} & {-1 -\lambda} & {-1 - \mu } \end{pmatrix}$$ for distinct eigenvalues $$\lambda, \mu \in \mathbb{R}$$ of $$G$$. 

Let $$\Lambda \left ( \mathcal{W} \right ) := \left \{ \frac{1}{n} J, E_{\lambda}, E_{\mu} \right \}$$ denote the set of primitive matrices in the adjacency algebra $$\mathcal{W}$$ of $$G$$ with adjacency matrix $$A = k \left ( \frac{1}{n} J \right ) + \lambda E_{\lambda} + \mu E_{\mu}$$.

Additionally, let $$ Q :=  \begin{pmatrix} 1 & 1 & 1 \\ j &  \lambda^{'} & \mu^{'} \\ {n - 1 - j} & {-1 - \lambda^{'}} & {-1 - \mu^{'}} \end{pmatrix}$$

denote the dual character table of $$G$$ relative to $$P$$

 with $$\lambda^{'} := \left ( \frac{j}{k} \right ) \lambda$$, 
  $$\mu^{'} := \left ( \frac{j}{n - 1 - k} \right ) \left ( -1 - \lambda \right )$$, 
  and $$j$$ the multiplicity of $$\lambda$$.

Since $$I = \frac{1}{n} J + E_{\lambda} + E_{\mu}$$, observe that $$G$$ is cometric relative to a primitive $$E \in \Lambda \left ( \mathcal{W} \right )$$ if and only if $$ I \in \operatorname{span} \{ J, E, E^{\circ 2} \}$$.

Now, recall from previous posts that:

$$ E_{\lambda} = \left ( \frac{1}{q_{\lambda}(\lambda)} \right ) q_{\lambda}(A) \text{ where } q_{\lambda}(x) := (x - k) (x - \mu ) \in \mathbb{C}[x] $$

$$ = \left ( \frac{\beta}{(\lambda - k)(\lambda - \mu)} \right ) \overline{A} + \left ( \frac{\alpha - k - \mu}{(\lambda - k)(\lambda - \mu)} \right ) A + \left ( \frac{k(1 + \mu)}{(\lambda - k)(\lambda - \mu)}\right ) I $$

$$ = \left ( \frac{\mu^{'}}{n} \right ) \overline{A} + \left ( \frac{\lambda^{'}}{n} \right ) A + \left ( \frac{j}{n} \right ) I $$

$$ \implies F_{\lambda} := E_{\lambda}^{\circ 2} - \left ( \frac{\lambda^{'} + \mu^{'}}{n} \right ) E_{\lambda} + \left ( \frac{ \lambda^{'} }{n} \right ) \left ( \frac{\mu^{'}}{n} \right ) J \in \operatorname{span} \{ I \}$$ 

And:

$$ E_{\mu} = \left ( \frac{-1 - \mu^{'}}{n} \right ) \overline{A} + \left ( \frac{-1 - \lambda^{'}}{n} \right ) A + \left ( \frac{n - 1 - j}{n} \right ) I $$

$$ \implies F_{\mu} := E_{\mu}^{\circ 2} - \left ( \frac{\left (-1 - \lambda^{'} \right ) + \left (- 1 - \mu^{'} \right )}{n} \right ) E_{\mu} + \left ( \frac{ \left ( -1 - \lambda^{'} \right )}{n} \right ) \left ( \frac{\left ( - 1 - \mu^{'} \right ) }{n} \right ) J \in \operatorname{span} \{ I \}$$ 

Observe that $$G$$ is cometric unless $$F_{\lambda} = 0 = F_{\mu}$$.

Assume then $$G$$ is not cometric.

$$ \implies \lambda^{'} \mu^{'} = j \left ( \lambda^{'} + \mu^{'} - j \right ) $$

$$ \text{ and } \left ( -1 - \lambda^{'} \right ) \left ( -1 - \mu^{'} \right ) = \left ( n - 1 - j \right ) \left ( \left ( -1 - \lambda^{'} \right ) + \left ( -1 - \mu^{'} \right ) - \left (n - 1 - j \right )  \right ) $$

$$ \implies \left ( 1 - j \right ) + \left ( 1 - \frac{1}{j} \right ) \lambda^{'} \mu^{'} = - (n - 1 - j) \left ( (n + 1) + \left ( \frac{1}{j} \right ) \lambda^{'} \mu^{'} \right ) $$

$$ \implies \lambda^{'} \mu^{'} = j \left ( \frac{ n(n - j) - 2}{n - 2} \right ) $$

It is then possible to express $$\lambda$$ and $$\mu$$ in terms of $$j$$ and the parameters of $$G$$:

*  $$ \lambda^{'} + \mu^{'} - j  = \left ( \frac{ n(n - j) - 2}{n - 2} \right ) $$
	
	$$ \implies \left ( \frac{1}{k} - \frac{1}{n - 1 - k} \right ) \lambda = \left ( \frac{ n(n - j) - 2}{j(n - 2) } \right ) + \left ( 1 + \frac{1}{n - 1 - k} \right ) $$

	$$ \implies \lambda = \left ( \frac{k}{n - 1 - 2k} \right ) \left ( \frac{(n - 1 - k)\left ( n^{2} - 2j - 2  \right )}{j(n-2)} + 1 \right ) $$

* $$ \lambda^{'} \mu^{'} = j \left ( \lambda^{'} + \mu^{'} - j \right ) $$ 

	$$ = j \left ( \frac{ n(n - j) - 2}{n - 2} \right ) $$

	$$ \implies \beta  \ \lambda^{'} = j \left ( \alpha + \beta - 2k - (k+1) \mu \right ) $$

	$$ = nk \left ( 1 + \mu \right ) \left ( \frac{ n(n - j) - 2}{n - 2} \right ) $$

	**[** from the expressions given for $$E_{\lambda}$$ **]**.

