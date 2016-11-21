---
layout: post
title:  "Strongly Regular Graphs Are Walk-Regular"
date:   2016-08-20
---

In this post, my goal is to show that strongly regular graphs are walk-regular.
I would like to start off by stating what it means for a simple graph to be walk-regular, as well as what it means for a simple graph to be strongly regular:
1. A simple graph is said to be *walk-regular* if all of its vertices are cospectral.
2. A simple graph is said to be *strongly regular* if it is: regular, every pair of adjacent vertices share the same number of neighbours in common, and every pair of non-adjacent vertices share the same number of neighbours in common - with the exception of the complete graphs, as well as the empty graph.

Suppose that $$G$$ is a strongly regular graph on $$n$$ vertices with adjacency matrix $$A$$.
Firstly, I would like to assume, for the purposes of this blog post, some standard facts about $$G$$ that must hold in this context:
1. The adjacency matrix $$A$$ of $$G$$ satisfies $$A^2 = \alpha I + \beta A + \gamma \overline{A}$$ for some non-negative integers $$\alpha,\beta,\gamma$$ (where $$\beta$$ and $$\gamma$$ are both not equal to $$0$$, and $$\alpha$$ is also non-zero).

*Note that here $$\overline{A}$$ denotes the adjacency matrix of the complement of $$G$$, which is explicitly defined as $$\overline{A} := J - I - A$$ (where $$J$$ denotes the matrix that consists entirely of $$1$$s as entries).*

2. The adjacency matrix $$A$$ of $$G$$ has three distinct eigenvalues, i.e. $$\mid\sigma(A)\mid = 3$$. In particular, $$E_\lambda = c_\lambda(A^2 - c_{\lambda}^{'}A - c_{\lambda}^{''}I)$$ for some $$c_{\lambda}, c_{\lambda}^{'}, c_{\lambda}^{''}$$ and all $$\lambda \in \sigma(A)$$; i.e. each $$E_\lambda$$ is some constant multiple of a monic polynomial of degree $$2$$ in $$A$$, for all $$\lambda \in \sigma(A)$$.

*Note that here, as in my previous blog post, each $$E_\lambda$$ denotes an orthogonal projection onto the eigenspace for eigenvalue $$\lambda$$ of $$A$$, for all eigenvalues $$\lambda \in \sigma(A)$$.
As in my previous blog post, I would also like to define an inner product on $$\mathbb{R}^{n}$$ as $$\langle x,y \rangle := x^T y$$ for all vectors $$x,y \in \mathbb{R}^{n}$$.*

Now, I would like to propose that $$G$$ is walk-regular, and would also like to show that this proposition holds in this context:
Consider any vertex $$u$$ on $$G$$ and any $$\lambda \in \sigma(A)$$. Then, from properties of inner products:

$$\langle E_\lambda e_u, e_u \rangle $$

$$= \langle c_\lambda (A^2 - c_{\lambda}^{'}A - c_{\lambda}^{''}I)e_u, e_u \rangle $$

$$= c_\lambda\langle (A^2 - c_{\lambda}^{'}A - c_{\lambda}^{''}I)e_u, e_u \rangle$$

.

From there, it is possible to further deduce that:

 $$\langle (A^2 - c_{\lambda}^{'}A - c_{\lambda}^{''}I)e_u, e_u \rangle $$

$$= \langle A^2 e_u, e_u \rangle - c_{\lambda}^{'} \langle Ae_u, e_u \rangle - c_{\lambda}^{''} \langle e_u, e_u \rangle $$

$$= \langle A^2 e_u, e_u \rangle - c_{\lambda}^{''} $$

$$= \langle (\alpha I + \beta A + \gamma \overline{A}) e_u, e_u \rangle - c_{\lambda}^{''} $$

$$= \alpha \langle e_u, e_u \rangle + \beta \langle Ae_u, e_u\rangle + \gamma \langle \overline{A}e_u, e_u \rangle - c_{\lambda}^{''} $$

$$= \alpha + \gamma \langle \overline{A}e_u, e_u \rangle - c_{\lambda}^{''} $$

$$= \alpha + \gamma \langle (J - I - A)e_u, e_u \rangle - c_{\lambda}^{''}$$

$$= \alpha + \gamma(\langle J e_u, e_u \rangle - \langle e_u, e_u \rangle - \langle A e_u, e_u \rangle) - c_{\lambda}^{''} $$

$$= \alpha - c_{\lambda}^{''}$$

. 

Therefore, $$\langle E_\lambda e_u, e_u \rangle = c_\lambda(\alpha - c_{\lambda}^{''})$$, which is independent of the choice of $$u$$ as a vertex. It ultimately follows that any pair of distinct vertices on $$G$$ are cospectral, and therefore $$G$$ is walk-regular.
Since $$G$$ is an arbitrary strongly regular graph, it is possible to conclude that every strongly regular graph is walk-regular. Hence, in this blog post, it is possible to conclude that every pair of distinct vertices on a strongly regular graph meet at least one of the necessary conditions for said vertices to admit the property known as perfect state transfer. However, it somewhat unfortunately turns out that it appears to be much rarer for strongly regular graphs to meet a stronger condition that a pair of distinct vertices must have to admit perfect state transfer, known as being strongly cospectral; I hope to examine the more specialized problem of systematically finding strongly regular graphs with strongly cospectral vertices in a future blog post.
