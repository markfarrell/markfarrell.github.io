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

So, self-dual coherent algebras can be constructed from e.g. self-complementary arc-transitive graphs in this way, for instance.

Now, a complex square matrix $$M$$ (of order $$n$$) is said to be **Schur-invertible** with **Schur-inverse** $$M^{(-)}$$ if $$M \circ M^{(-)} = J$$ for some (unique) matrix $$M^{(-)} \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ and all-ones matrix $$J \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$.

The **Nomura algebra** $$\mathcal{N}_{M}$$  (of order $$n$$) of a Schur-invertible matrix $$M \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ is defined as $$\mathcal{N}_{M} := \{ N \in \operatorname{Mat}_{n \times n}(\mathbb{C}) : N \left ( M e_{i} \circ M^{(-)} e_{j} \right ) \in \operatorname{span} \left \{ M e_{i} \circ M^{(-)} e_{j} \right \} \text{ for all } 1 \leq i,j \leq n \}$$; the Nomura algebra of Schur-invertible matrix is a subspace of complex square matrices that is closed under ordinary matrix multiplication with identity.

A Schur-invertible matrix $$M$$ of order $$n$$ is said to be **Type-II** if $$M M^{(-)} = n I$$.

I would like to construct a second example of a family of self-dual coherent algebras from Nomura algebras of Type-II matrices:

1. Let $$\Lambda_{M} : \mathcal{N}_{M} \to \operatorname{Mat}_{n \times n}(\mathbb{C})$$ denote the linear mapping such that $$N \left ( M e_{i} \ \circ \ M e_{j} \right ) = \left ( \Lambda_{M} (N) \right )_{i,j} \ \left ( M e_{i} \ \circ \ M e_{j} \right )$$ for all $$1 \leq i, j \leq n$$ and $$N \in \mathcal{N}_{M}$$, 
	for any Schur-invertible matrix $$M$$ (of order $$n$$).

2. Suppose that $$M$$ is a Type-II matrix of order $$n$$.

	Select any $$N \in \mathcal{N}_{M}$$.

	Then for all $$1 \leq i, j, k \leq n$$:

	$$ \implies e_{k}^{T} \left ( \Lambda_{M}(N) \left ( M^{T} e_{i} \circ M^{(-)T} e_{j} \right ) \right ) $$

	$$ = \sum\limits_{l = 1}^{n} \left ( \Lambda_{M}(N) \right )_{k, l} \ M_{i, l} \ M_{j,l}^{(-)} $$

	$$ = \sum\limits_{l = 1}^{n} \left ( \sum\limits_{m = 1}^{m} \left ( N_{j,m} M_{m,k} M_{m,l}^{(-)} \right ) \left ( M_{j,k}^{(-)} M_{j, l} \right ) \right ) M_{i,l} M_{j,l}^{(-)}$$

	$$ = M_{j,k}^{(-)} \left ( \sum\limits_{m = 1}^{n} \left ( N_{j,m} M_{m,k} \right )  \left ( \sum\limits_{l = 1}^{m} M_{i, l} M_{m, l}^{(-)} \right ) \right ) $$

	$$ = M_{j,k}^{(-)} \left ( N_{j, i} M_{i,k} \right ) \left ( n \right ) $$

	**[** since $$M$$ is Type-II **]**

	$$ = \left ( n N_{j, i} \right ) \left ( e_{k}^{T} \left ( M^{T} e_{i} \circ M^{(-){T}} e_{j} \right) \right ) $$

	.

	$$ \implies \Lambda_{M}(N) \in \mathcal{N}_{M^{T}} $$

	**[** noting that $$M^{T}$$ is also Type-II **]**.

	By similar reasoning, it follows that $$\Lambda_{M^{T}} \left ( \frac{1}{n} \ \Lambda_{M}(N) \right ) = N^{T} \in \mathcal{N}_{M}$$.

	It is then ultimately apparent that $$\mathcal{N}_{M}$$ is closed under transposition in general.

	Observe moreover that $$\Lambda_{M} : \mathcal{N}_{M} \to \mathcaL{N}_{M_{T}}$$ is in fact a linear isomorphism (with inverse $$\left \Lambda_{M^{T}} \circ \Lambda_{M} \right )^{2}$$): hence it is ultimately apparent too that $$\mathcal{N}_{M}$$ is closed under Schur-product (since $$\mathcal{M_{T}}$$ is closed under ordinary matrix multiplication).

	Lastly, since $$M$$ is Type-II, it immediately follows that the all-ones matrix $$J \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ is in $$\mathcal{N}_{M}$$ as well.

	Hence it can be concluded here that $$\mathcal{N}_{M}$$ is a coherent algebra.





















	

