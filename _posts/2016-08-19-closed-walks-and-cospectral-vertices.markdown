---
layout: post
title:  "Closed Walks and Cospectral Vertices"
date:   2016-08-19
categories: jekyll update
---

If a pair of distinct vertices on a simple graph admit perfect state transfer with respect to the continuous-time quantum walk of its adjacency matrix, then it is a necessary condition that said vertices have the property known as being cospectral. In this post, my goal is to provide some useful characterizations of cospectrality, and provide some useful sufficient conditions for a pair of distinct vertices to be cospectral on a simple graph.



Suppose that $$G$$ is a simple graph on $$n$$ vertices, with adjacency matrix $$A$$. Then, I would like to provide some definitions in this context:

1. An inner product can be defined on $$\mathbb{R}^{n}$$ as $$\langle x,y \rangle := x^T y$$ for all $$x,y \in \mathbb{R}^{n}$$.

2. Let $$\sigma(A)$$ denote the set of all distinct eigenvalues of $$A$$. If for any pair of distinct vertices $$u$$ and $$v$$ on $$G$$ we have that $$\langle E_\lambda e_u, e_u \rangle = \langle E_\lambda e_v, e_v \rangle$$ for all $$\lambda \in \sigma(A)$$, then $$u$$ and $$v$$ are said to be cospectral.

*Note that here each $$E_\lambda$$ denotes an orthogonal projection onto the eigenspace for eigenvalue $$\lambda$$* of *$$A$$, for all $$\lambda \in \sigma(A)$$.*

3. Suppose that $$u$$ is any vertex on $$G$$. Then closed walk generating series of $$u$$ is defined as: $$W_u(X) := \sum\limits_{k=0}^{\infty} \langle A^n e_u, e_u \rangle X^n$$.

*Note that $$W_u(X) \in \mathbb{R} \left[ \left[ X \right] \right]$$, i.e. it is an element of the algebra of formal power series with real coefficients.*

4. Suppose that $$G$$ has $$n$$ vertices, and $$u$$ is a vertex on $$G$$. Then the walk matrix $$B_u$$ relative to vertex $$u$$ is defined as $$B_u := \left( e_u \mid A e_u \mid \cdots \mid A^{n-1} e_u \right)$$.

5. If $$P$$ is an $$n$$ x $$n$$ permutation matrix that commutes with $$A$$, i.e. $$AP = PA$$, then $$P$$ is said to represent an automorphism on $$G$$.

And, I would like to state some propositions in this context:

1. Any pair of distinct vertices $$u$$ and $$v$$ on $$G$$ are cospectral if and only if their closed walk generating series are equal, i.e. $$W_u(X) = W_v(X).$$

2. Any pair of distinct $$u$$ and $$v $$on $$G$$ are cospectral if and only if $$(B_u)^T B_u = (B_v)^T B_v.$$

3. Suppose that a permutation matrix $$P$$ represents an automorphism on $$G$$. If for any pair of distinct vertices $$u$$ and $$v$$ on $$G$$, $$P e_u = e_v$$ and $$P e_v = e_u$$, then $$u$$ and $$v$$ are cospectral.

Finally, I would like to show that these propositions hold in this context:

1. Suppose that a pair of distinct vertices $$u$$ and $$v$$ on $$G$$ are cospectral, and that $$A$$ has spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_\lambda$$. Then for all non-negative integers $$k \geq 0,$$ $$A^k$$ has spectral decomposition $$A^k = \sum\limits_{\lambda \in \sigma(A)} \lambda^k E_\lambda$$. From properties of inner products, it follows that if for all $$\lambda \in \sigma(A)$$, $$\langle E_\lambda e_u, e_u \rangle = \langle E_\lambda e_v, e_v \rangle$$, then $$\langle A^k e_u, e_u \rangle = \langle A^k e_v, e_v \rangle$$ for all $$k \geq 0$$. Hence if $$u$$ and $$v$$ are cospectral, then their closed walk generating series are equal.

Conversely, suppose that a pair of distinct vertices $$u$$ and $$v$$ on $$G$$ have closed walk generating series, i.e. $$W_u(X) = W_v(X)$$. In particular, this means that for all non-negative integers $$k \geq 0$$, $$\langle A^k e_u, e_u \rangle = \langle A^k e_v, e_v \rangle$$. It follows from properties of inner products that for all polynomials $$f(A)$$ in $$A$$, i.e. $$f(x)$$ is a polynomial with real coefficients and $$f(A) \in Z(A) = \mathrm{span} \{ I, A, A^2, \cdots \}$$, $$\langle f(A) e_u, e_u \rangle = \langle f(A) e_v, e_v \rangle$$. It is also the case that each $$E_\lambda$$ is a polynomial in $$A$$ for all eigenvalues $$\lambda \in \sigma(A)$$, as can be seen in the proof of the establishment of the spectral decomposition of $$A$$. Hence it ultimately follows that if $$u$$ and $$v$$ have equal closed walk generating series, then $$u$$ and $$v$$ are cospectral.
2. Suppose that a pair of distinct vertices $$u$$ and $$v $$on $$G$$ are cospectral. By the previous proposition, this means that they also have equal closed walk generating series - which means that for all non-negative integers $$k \geq 0$$, $$\langle A^k e_u, e_u \rangle = \langle A^k e_v, e_v \rangle$$. Observe that any entry in $$(B_u)^T B_u$$ is of the form $$\langle A^j e_u, e_u \rangle$$ for some non-negative integer $$j$$. Hence it follows that $$(B_u)^T B_u = (B_v)^T B_v$$.

Conversely, suppose that $$(B_u)^T B_u = (B_v)^T B_v$$. Observe, by looking at the first columns of these matrices, that $$\langle A^j e_u, e_u \rangle = \langle A^j e_v, e_v \rangle$$ for all $$0 \leq j \leq n - 1$$. The degree of the minimal polynomial of $$A$$ must be less than or equal to $$n$$, since it wouldn’t make sense for $$A$$ to have more distinct eigenvalues than it has vertices. Hence for all $$k \geq n$$, $$A^k$$ can be expressed as a linear combination of $$I, A, \cdots$$, and $$A^{n-1}$$. It ultimately follows, from properties of inner products, that for all $$k \geq 0$$, $$\langle A^k e_u, e_u \rangle = \langle A^k e_v, e_v \rangle$$; which means that $$u$$ and $$v$$ have equal closed walk generating series, and hence they are cospectral.
3. Suppose that $$P$$ is a permutation matrix that represents an automorphism on $$G$$ that swaps distinct vertices $$u$$ and $$v$$ on $$G$$. Since $$P$$ represents an automorphism on $$G$$, this means that $$AP = PA$$. It follows that for all non-negative integers $$k \geq 0$$, $$A^k P = P A^k$$ as well. Furthermore, it follows that for all $$k \geq 0$$ and all vertices $$\alpha$$ on $$G$$,

$$ \langle A^k e_\alpha, e_\alpha \rangle $$


$$ = (e_\alpha)^T A^k e_\alpha $$

$$ = (e_\alpha)^T (P^T A^k P) e_\alpha $$

$$ = ((e_\alpha)^T P^T) A^k (P e_\alpha) $$

$$ = (P e_\alpha)^T (A^k (P e_\alpha)) $$

$$ = \langle A^k (Pe_\alpha), (Pe_\alpha) \rangle $$

.


Hence if $$P$$ sends $$u$$ to $$v$$ , i.e. $$Pe_u = e_v$$ and $$Pe_v = e_u$$, then in particular $$\langle A^k e_u, e_u \rangle = \langle A^k (Pe_u), (Pe_u) \rangle = \langle A^k e_v, e_v \rangle$$ for all $$k \geq 0$$; which means that the closed walk generating series of $$u$$ and $$v$$ are equal, and therefore they are cospectral.


These characterizations of cospectrality, and sufficient conditions for a pair of distinct vertices on a simple graph to be cospectral, can serve as a useful toolkit for finding cospectral vertices on particular simple graphs. For example, the automorphism group of any path graph is a cyclic group of order two, which is always generated by a single permutation that swaps its ends in particular; it follows, from the work above in this blog post, that the ends of any path are always cospectral. As an another example, the same work can be applied to determine that any pair of non-central vertices of any star graph are cospectral (for star graphs $$K(1,n)$$ for all $$n \geq 2$$). It is also possible to find closed forms for the closed walk generating series for non-central vertices of star graphs, and find that any pair of non-central vertices on a star graph are cospectral since they have equal closed walk generating series are hence cospectral; the same strategy can applied to again determine that the ends of any path are cospectral. However, cospectrality is only a neccessary (but not sufficient) condition for a pair of distinct vertices on a simple graph to admit the property known as perfect state transfer on a simple graph, which I was initially interested in investigating; I hope to discuss other necessary conditions, and ultimately all sufficient conditions, for perfect state transfer to occur between a pair of distinct vertices on a simple graph in future blogs, as I investigate and learn about them.
