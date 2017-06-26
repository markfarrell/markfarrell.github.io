---
layout: post
title:  "Strongly Cospectral Vertices on Cayley Graphs"
date:   2017-06-26
---

I would like to show that every pair of distinct vertices on a simple Cayley graph of a finite abelian group are strongly cospectral;
as discussed in previous posts strongly cospectrality is a necessary condition for a pair of distinct vertices on a simple graph to admit
perfect state transfer.

Suppose that $$G$$ is a finite abelian group. Let $$n := \lvert G \rvert $$, $$\operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote the space of
$$ n \times n $$ complex matrices whose rows and columns are indexed by the elements of $$G$$ 
relative to a certain ordering of them, and let $$\mathcal{A} := \{ A_{g} : g \in \mathbb{G} \} \subset $$ denote a set of adjacency matrices for 
the set of conjugacy class graphs of $$G$$ where $$\mathcal{A}_{g}$$ denotes an adjacency matrix for the conjugacy class graph of conjugacy class $$\{g \}$$ for all $$g \in G$$.

Now, consider any simple Cayley graph $$\Gamma$$ of $$G$$ with connection set $$C$$.

*I would firstly like to establish that $$\Gamma$$ has $$n$$ distinct eigenvalues in this context.*

Let $$A_{\Gamma}$$ denote the adjacency matrix of $$\Gamma$$, 
$$\sigma(\Gamma)$$ denote the set of distinct eigenvalues of $$\Gamma$$,
$$p(x) := \prod\limits_{\lambda \in \sigma(\Gamma)} (x - \lambda) \in \mathbb{C}[x]$$,
and let $$E_{\lambda} := \frac{1}{q_{\lambda}(\lambda)} q_{\lambda} \left ( A_{\Gamma}  \right ) $$ 
where $$ q_{\lambda}(x) := \frac{p(x)}{(x - \lambda)}$$ for all $$\lambda \in \sigma(\Gamma)$$.

Observe the facts that:
  * $$\{ E_{\lambda} : \lambda \in \sigma(\Gamma) \}$$ is linearly independent in $$\operatorname{Mat}_{G \times G}(\mathbb{C})$$. 
  * $$E_{\lambda}$$ is a projection onto $$\operatorname{null} \left ( A_{\Gamma} - \lambda I \right )$$  for all $$ \lambda \in \sigma(\Gamma) $$.
  * $$\sum\limits_{\lambda \in \sigma(\Gamma)} E_{\lambda} = I$$ 
    and moreover that $$A_{\Gamma} = \sum\limits_{\lambda \in \sigma(\Gamma)} \lambda \ E_{\lambda} $$.

Additionally, observe that $$A_{\Gamma} := \sum\limits_{c \in C} \left ( A_{c} + A_{c}^{T} \right )$$.

Next, select any particular $$c \in C$$. It follows from my previous points that:

$$ \operatorname{span} \mathcal{A} $$ 

$$ = \operatorname{span} \left ( A_{\Gamma} \sqcup \left ( \mathcal{A} \setminus \{ A_{c} \} \right ) \right ) $$

$$ = \operatorname{span} \left \{ E_{\lambda} : \lambda \in \sigma(\Gamma) \right \} $$

**[** since, by a previous post, $$\mathcal{A}$$ is a (commutative) association scheme
 and hence the elements of $$\operatorname{span} \mathcal{A}$$ are simultaneously diagonalizable **]**.

$$ \implies \lvert \mathcal{A} \rvert = \lvert \left \{ E_{\lambda} : \lambda \in \sigma(\Gamma) \right \} \rvert $$

$$ \implies \Gamma \text { has } n \text{ distinct eigenvalues, }$$

**[** since $$n = \lvert \mathcal{A} \rvert$$
and $$\lvert \sigma(\Gamma) \rvert =  \lvert \left \{ E_{\lambda} : \lambda \in \sigma(\Gamma) \right \} \rvert $$ **]**.

*Continuing on in the context, I would like to secondly establish that every pair of distinct vertices on $$\Gamma$$ are parallel*.

Let $$S$$ denote the set of irreducible characters of $$G$$ over $$\mathbb{C}$$, and let $$e$$ denote the identity element of $$G$$, 

Recalling the general expression for the characteristic polynomial of a conjugacy class graph of a finite group that I established
in a previous post, it is now apparent that:

$$ \phi_{\Gamma}(x) := \operatorname{det}(x \ I - A) = \prod\limits_{\chi \in S} \left ( x - \left ( \frac{1}{\chi(e)} \ \sum\limits_{c \in C} \overline{\chi(c)} \right ) \right )^{(\chi(e))^{2}} $$

is the characteristic polynomial of $$\Gamma$$

**[** since by previous points it is clear that $$\Gamma$$ is a union of conjugacy class graphs of $$G$$ **]**.

Then it is apparent that $$(\chi(e))^{2} = 1$$ and moreover that $$\chi(e) = 1$$ for all $$\chi \in S $$

**[** since $$\Gamma$$ has $$n$$ distinct eigenvalues, by previous point **]**.

$$ \implies \operatorname{dim} \left ( \operatorname{null} \left ( A_{\Gamma} - \lambda I \right ) \right ) = 1 \text{ for all } \lambda \in \sigma(\Gamma)$$

Next, define:

* $$\operatorname{M_{\chi}} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$

  $$M_{\chi}(x,y) := \chi(x^{-1} y)$$

for all $$\chi \in S$$.

Following from a previous a post, observe that:
* $$ \left ( M_{\chi} \right )^{2} = n \ M_{\chi}  $$
* $$\sum\limits_{\chi \in S} \frac{1}{n} \ M_{\chi} = I$$
	and moreover that 

	$$ A_{\Gamma} = \sum\limits_{\chi \in S } \left ( \sum\limits_{c \in C} \overline{\chi(c)} \right ) \left ( \frac{1}{n} \ M_{\chi} \right ) $$.

Additionally, by similar reasoning as before, observe that: 
  * $$ \operatorname{span} \left \{ E_{\mu} : \mu \in \sigma(\Gamma) \right \} $$
    $$ = \operatorname{span} \mathcal{A} $$ 
    $$ = \operatorname{span} \left \{ M_{\omega} : \omega \in S \right \} $$

Then, for any $$\chi \in S$$:

1. $$\operatorname{null} \left ( A_{\Gamma} - \left ( \sum\limits_{c \in C} \overline{\chi(c)} \right ) \ I \right) $$

	$$ = \operatorname{null} \left ( \sum\limits_{\psi \in S, \ \psi \neq \chi} \left ( \sum\limits_{c \in C} \overline{\psi(c) - \chi(c)} \right ) \left ( \frac{1}{n} \ M_{\psi} \right ) \right ) $$

	$$ = \operatorname{null} \left ( \sum\limits_{\psi \in S, \ \psi \neq \chi} M_{\psi} \right ) $$

	**[** observing that $$\{ M_{\psi} : \psi \in S \} \setminus \{ M_{\chi} \}$$ is linearly independent in $$\operatorname{Mat}_{G \times G}(\mathbb{C})$$ **]**

	$$ = \operatorname{null} \left ( \sum\limits_{\psi \in S, \ \psi \neq \chi} \left ( \frac{1}{n} \ M_{\psi} \right ) \right ) $$

	$$ = \operatorname{null} \left ( I - \left( \frac{1}{n} \  M_{\chi} \right ) \right ) $$

	**[** since $$\Gamma$$ has $$n$$ distinct eigenvalues and $$\lvert S \rvert = n$$ **]**

	$$ = \operatorname{col} \left ( \frac{1}{n} \ M_{\chi} \right ) $$

	**[** since $$\left ( \frac{1}{n} \ M_{\chi} \right )$$ is a projection **]**

	$$ = \operatorname{col} \left ( M_{\chi} \right ) $$

2. Select any $$\psi \in S$$ such that $$\chi \neq \psi$$.
	
	Let $$\lambda := \left ( \sum\limits_{c \in C} \overline{\psi(c)} \right )$$.

	Observe the facts that $$M_{\psi}$$ and $$E_{\lambda}$$ are Hermitian.

	$$ \implies M_{\chi} E_{\lambda} = E_{\lambda} M_{\chi} = 0$$

	**[** since $$ \operatorname{col} \left ( M_{\chi} \right ) = \operatorname{null} \left ( A_{\Gamma} - \left ( \sum\limits_{c \in C} \overline{\chi(c)} \right ) \ I \right)$$ by **1.**, 
  $$\operatorname{col} \left ( E_{\lambda} \right ) = \operatorname{null} \left ( A_{\Gamma} - \left ( \sum\limits_{c \in C} \overline{\psi(c)} \right ) \ I \right)$$, 
  and eigenvectors corresponding to distinct eigenvalues of $$A_{\Gamma}$$ are orthogonal with respect to the usual inner product on  $$\mathbb{C}^{n}$$ **]**.
3. Let $$\lambda := \left ( \sum\limits_{c \in C} \overline{\chi(c)} \right )$$.

	$$ \implies  \left ( \frac {1}{n} M_{\chi} \right ) E_{\lambda} = \left ( \frac {1}{n} M_{\chi} \right ) \text{ and } E_{\lambda} \left ( \frac {1}{n} M_{\chi} \right ) = E_{\lambda} $$

	**[** by **2.** and from previous points **]**.

	$$ \implies \left ( \frac {1}{n} M_{\chi} \right ), E_{\lambda} \in \operatorname{span} \mathcal{A} $$ 

	$$ \implies \left ( \frac {1}{n} M_{\chi} \right ) E_{\lambda} = E_{\lambda} \left ( \frac {1}{n} M_{\chi} \right ) $$

	$$ \implies \left ( \frac {1}{n} M_{\chi} \right ) = E_{\lambda} $$

4. $$ \left ( M_{\chi} \right )_{g,g} = \chi(e) = 1$$ for all $$g \in G $$.

   This implies that every of column of $$M_{\chi}$$ is non-zero.
  
From **1.**-**.4.**, together with the fact that $$\operatorname{dim} \left ( \operatorname{null} \left ( A_{\Gamma} - \lambda I \right ) \right ) = 1$$ for all $$\lambda \in \sigma(\Gamma)$$
, 
it follows that every pair of distinct columns of $$E_{\lambda}$$ are non-zero scalar multiples of each other for all $$\lambda \in \sigma(\Gamma)$$.

Hence every pair of distinct vertices on $$\Gamma$$ are parallel.

Lastly, since $$\Gamma$$ is a simple Cayley graph, it is vertex-transitive and therefore walk-regular - i.e. every pair of distinct
vertices on $$\Gamma$$ are cospectral as well.

It can therefore be concluded that every pair of distinct vertices on $$\Gamma$$ are strongly cospectral,

since a pair of distinct vertices on a simple graph are strongly cospectral if and only if they are both parallel and cospectral.


It also follows in general now that every pair of distinct vertices on a simple Cayley graph of a finite abeliean group are strongly cospectral, since $$\Gamma$$ is arbitrary.









