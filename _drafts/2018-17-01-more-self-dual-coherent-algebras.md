---
layout: post
title:  "More Self-Dual Coherent Algebras"
date:   2018-01-17
---

I would like to establish some more examples of families of self-dual coherent algebras, in addition to the 
prototypical example of a family of self-dual coherent algebras arising from finite abelian groups that I 
established in my last post.

Suppose that $$\mathcal{W}$$ and $$\mathcal{X}$$ are commutative coherent algebras of order $$n$$. 

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

	Observe moreover that $$\Lambda_{M} : \mathcal{N}_{M} \to \mathcal{N}_{M_{T}}$$ is in fact a linear isomorphism (with inverse $$\left ( \Lambda_{M^{T}} \bullet \Lambda_{M} \right )^{2}$$): hence it is ultimately apparent too that $$\mathcal{N}_{M}$$ is closed under Schur-product (since $$\mathcal{N}_{M^{T}}$$ is closed under ordinary matrix multiplication).

	Since $$M$$ is Type-II, it immediately follows that the all-ones matrix $$J \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ is in $$\mathcal{N}_{M}$$ as well.

	Hence it can be established here that $$\mathcal{N}_{M}$$ is a coherent algebra; indeed, $$\mathcal{N}_{M}$$ is a commutative coherent algebra since 
	$$X Y = \Lambda_{M}^{-1} \left ( \Lambda_{M}(X) \circ \Lambda_{M}(Y) \right ) = \Lambda_{M}^{-1} \left ( \Lambda_{M}(Y) \circ \Lambda_{M}(X) \right ) = Y X$$ for all $$X, Y \in \mathcal{N}_{M}$$.

	It can then be similarly seen that $$\mathcal{N}_{M^{T}}$$ is a commutative coherent algebra as well. 

	It is then apparent that $$\Lambda_{M} : \mathcal{N}_{M} \to \mathcal{N}_{M^{T}}$$ is a duality mapping between commutative coherent algebras $$\mathcal{N}_{M}$$ and $$\mathcal{N}_{M^T}$$: since $$\frac{1}{n} \left ( \Lambda_{M^{T}} \bullet \Lambda_{M} \right )$$ maps Schur-primitive matrices in $$\mathcal{N}_{M}$$ to their Schur-primitive transpose in $$\mathcal{N}_{M}$$, it is necessary that $$\frac{1}{n} \Lambda_{M}$$ maps Schur-primitive matrices in $$\mathcal{N}_{M}$$ to primitive matrices in $$\mathcal{N}_{M^{T}}$$ and moreover that $$\Lambda_{M}(X \circ Y) = \frac{1}{n} \Lambda_{M}(X) \ \Lambda_{M}(Y)$$ for all $$X, Y \in \mathcal{N}_{M}$$.

	Finally, it can then be concluded here that the tensor product $$\mathcal{N}_{M} \otimes \mathcal{N}_{M^{T}}$$ of Nomura algebras $$\mathcal{N}_{M}$$ and $$\mathcal{N}_{M^{T}}$$ for the Type-II matrix $$M$$ is a self-dual coherent algebra.

So, self-dual coherent algebras can indeed be constructed from Type-II matrices: complex Hadamard matrices are a first example of a family of Type-II matrices that comes to mind, which moreover can e.g. be constructed from character tables of finite abelian groups and graphs that admit uniform mixing (with respect to their continuous-time quantum walks relative to their adjacency matrices).

I would now lastly like to establish that the adjacency algebras of Hamming graphs are self-dual coherent algebras:

* Suppose that $$G := H^{n}$$ is the $$n$$-th direct power of some finite cyclic group $$H$$ and $$n \in \mathbb{N}$$.

	Let $$\mathcal{W}_{G}$$ denote the coherent algebra arising from $$G$$ as in my previous posts: 
	i.e. $$\mathcal{W}_{G} := \operatorname{span} \{ A_{g} : g \in G \}$$ where $$A_{g} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ is a $$01$$-matrix relating pairs of elements of $$G$$ whose difference is $$g$$ for all $$g \in G$$.

	Additionally, let $$f_{G} : G \to \{ 0, \cdots, n \}$$ denote a Hamming weight function on $$G$$: i.e. a function mapping elements of $$G$$ to their
	number of non-zero coordinates.

	Partition the elements of $$G$$ according to their Hamming weight: define $$G_{j} := \{ g \in G : f_{G}(g) = j \}$$ for all $$0 \leq j \leq n$$.

	For all $$0 \leq j \leq n$$, let $$A_{j} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote the $$01$$-matrix in $$\in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ relating pairs of elements of $$G$$ whose difference has Hamming weight $$j$$:

	 i.e. $$\left ( A_{j} \right )_{x,y} := \begin{cases} 1 & \text{ if } f_{G}(xy^{-1}) = j \\ 0 & \text{ otherwise} \end{cases}$$ for all $$x, y \in G$$.

	Define $$\mathcal{X}_{G} := \operatorname{span} \{ A_{j} : 0 \leq j \leq n \} \subseteq \operatorname{Mat}_{G \times G}(\mathbb{C})$$.

	Note that $$\mathcal{X}_{G} \subseteq \mathcal{W}_{G}$$, since $$G$$ is abelian and hence $$f_{G}\left ( \left ( z x \right ) \left ( z y \right )^{-1} \right ) = f_{G} \left ( x y^{-1} \right )$$ for all $$x,y,z \in G$$ since $$G$$ is abelian.

	It is then apparent that $$\mathcal{X}_{G}$$ is a commutative coherent subalgebra of $$\mathcal{W}_{G}$$, observing that $$\mathcal{X}_{G}$$ can be identified
	with the adjacency algebra of a Hamming graph (which is a commutative coherent algebra, assuming the fact that Hamming graphs are distance-regular).

	Now, recall too from a previous post that the set $$\{ \chi_{g} : g \in G \}$$ of irreducible characters of $$G$$ can be indexed in such a way
	that $$\chi_{x}(y) = \chi_{y}(x)$$ for all $$x, y \in G$$ (and that $$\mathcal{W}_{G}$$ is self-dual under the character table of $$\mathcal{W}_{G}$$ relative to this way of indexing the irreducible characters of $$G$$).

	Observe too then that $$\sum\limits_{g \in G_{j}} \chi_{g}(h)$$ depends only on the Hamming weight of $$h$$ for all $$h \in G$$ and all $$0 \leq j \leq n$$,
	which essentially follows from the the fact that $$G$$ is a direct power of a finite cyclic group.

	Define the matrix $$P \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ as $$P_{j,k} :=  \frac{1}{\left\vert G_{k} \right\vert}  \left ( \sum\limits_{(g, h) \in G_{j} \times G_{k}} \overline{\chi_{g}(h)} \right )$$ for all $$0 \leq j, k \leq n$$.

	From previous posts, it then follows $$P$$ is character table for $$\mathcal{X}_{G}$$.

	Note too that $$P = \overline{P}$$, since $$\mathcal{X}_{G}$$ is the adjacency algebra of distance-regular graph and hence every Schur-primitive matrix in $$\mathcal{X}_{G}$$ is a Hermitian matrix (whose distinct eigenvalues are all real).

	Lastly, for all $$0 \leq j \leq n$$, define $$E_{j} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ as $$E_{j} := \frac{1}{\left\vert G \right\vert} \ F_{j}^{*} F_{j}$$ where $$F_{j} \in \operatorname{Mat}_{G_{j} \times G}(\mathbb{C})$$ is defined as $$\left ( F_{j} \right )_{x,y} := \overline{\chi_{x}(y)}$$ for all $$x \in G_{k}$$ and $$y \in G$$.

	It then be observed that $$A_{j} = \sum\limits_{k = 0}^{n} P_{j,k} E_{k}$$ and that $$E_{j} = \sum\limits_{k = n} P_{j,k} A_{k}$$ for all $$ 0 \leq j \leq n $$.

	Moreover, it follows from the fact the irreducible characters of $$G$$ form an orthonormal basis for the vector space $$L^{2}(G)$$ of complex-valued functions on $$G$$ that each $$E_{j}$$ is idempotent for all $$ 0 \leq j \leq n $$.

	Hence it can be concluded that $$\{ E_{j} : 0 \leq j \leq n \} \subseteq \mathcal{X}_{G}$$ is the set of primitive matrices in $$\mathcal{X}_{G}$$
	and that $$\mathcal{X}_{G}$$ is a self-dual coherent algebra.


It turns out that the adjacency algebra of every Hamming graph can be identified with an instance of this kind of coherent algebra arising
from a finite cyclic group as well; hence the adjacency algebras of Hamming graphs are indeed self-dual.


So, indeed there are some arguably interesting families of self-dual coherent algebras that can be constructed aside from the prototypical example
of a family of self-dual coherent algebras arising from finite abelian groups that I established in my previous post. I hope to continue to e.g. construct even more examples of self-dual coherent algebras in future posts towards e.g. completely classifying certain families of self-dual coherent algebras, such as certain families of distance-regular graphs whose adjacency algebras are self-dual.



















	

