---
layout: post
title:  "More Self-Dual Coherent Algebras"
date:   2018-01-17
---

I would like to establish some more examples of families of self-dual coherent algebras, in addition to the 
prototypical example of a family of self-dual coherent algebras arising from finite abelian groups that I 
established in my last post.

Suppose that $$W$$ and $$X$$ are commutative coherent algebras of order $$n$$. 

A **duality mapping** from $$\mathcal{W}$$ to $$\mathcal{X}$$ is a linear isomorphism $$T : \mathcal{W} \to \mathcal{X}$$ such that:

1. $$T(M N) = T(M) \circ T(N)$$ for all $$M, N \in \mathcal{W}$$.

2. $$T(M \circ N) = \frac{1}{n} \ T(M) \ T(N)$$ for all $$M, N \in \mathcal{W}$$.

I would like to assume the fact that the tensor product of two commutative coherent algebras is self-dual if there is a duality mapping between them.

Then as a first additional example of a family of self-dual coherent algebras:

* Suppose that $$G$$ is a self-complementary strongly-regular graph of order $$n$$.

	Assume that $$G$$ is connected and $$k$$-regular.

	Then $$G$$ has three distinct eigenvalues $$\{k, \lambda, -1 - \lambda \}$$ for some $$\lambda \in \mathbb{R}$$, since it is strongly-regular and self-complementary.

	Moreover:

	$$\mathbb{C}[A] := \operatorname{span} \{ I, A, A^{2}, \cdots \} = \operatorname{span} \left \{ I, A, P A P^{T} \right \} = \operatorname{span} \left \{ \frac{1}{n} J, E, P E P^{T} \right \}$$

	for some permutation matrix $$P \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ and orthogonal projection $$E \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ such that $$A = k \left (\frac{1}{n} J \right ) + \lambda E + (-1 - \lambda) P E P^{T} $$, letting $$A \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ denote the adjacency matrix of $$G$$ and $$J$$ denote the all-ones matrix in $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$.

	Now, let $$T : \mathbb{C}[A] \to \mathbb{C}[A]$$ denote the linear automorphism on $$\mathbb{C}[A]$$ such that $$T(E) := A$$, $$T \left ( P E P^{T} \right ) := P A P^{T}$$, and $$T \left ( \frac{1}{n} J \right ) := I$$.

	$$\implies T \left ( A + P A P^{T} \right ) $$

	$$ = \left ( 2k \right ) \ T \left ( \frac{1}{n} J \right ) - T(E) - T \left (P E P^{T} \right ) $$

	$$ = (2k)I - A - P A P^{T} $$

	$$ = (n-1)I - A - P A P^{T} $$

	**[** again, since $$G$$ is self-complementary **]**

	$$ = nI - \left ( I + A + P A P^{T} \right ) $$

	$$ = nI - J $$ 

	$$ \implies T \left ( A + P A P^{T} \right ) = \frac{1}{n} \left ( T \left ( A + P A P^{T} \right ) \right )^{2} $$

	Observe now that $$\mathbb{C}[A]$$ is a commutative coherent algebra and that $$T \left ( P M P^{T} \right ) = P \ T(M) \ P^{T} $$ for all $$ M \in \mathbb{C}[A]$$.

	$$ \implies \frac{1}{n} T(A) \in \left \{ E, P E P^{T} \right  \} $$

	$$ \implies T \left ( M \circ N \right )  = \frac{1}{n} T(M) \ T(N) \text { for all } M, N \in \mathbb{C}[A] $$

	It can then be concluded that $$\mathcal{C}[A] \otimes \mathcal{C}[A]$$ is a self-dual coherent algebra, since $$T(M N) = T(M) \circ T(N) $$
	for all $$M,N \in \mathcal{C}[A]$$ by construction as well.









	

