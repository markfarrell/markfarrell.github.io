---
layout: post
title:  "Grassman Graphs Are Distance-Regular"
date:   2017-01-20
---

Suppose that we are given arbitrary natural number $$n$$, a natural number $$k \leq n$$, and a prime power $$q$$. Let $$S = \{ W : W \leq V \operatorname{and} \operatorname{dim}(W) = k \}$$ denote the set of $$k$$-dimensional subspaces of a vector space $$V$$ over the finite field $$F_{q}$$ of order $$q$$. Consider the simple graph $$G=(S,E)$$ formed with the set $$S$$ as vertices and the set $$E=\{\{W,Z\} : W,Z \in S \operatorname{and} \operatorname{dim}(W \cap Z)= k -1\} $$ as edges. Select an arbitrary pair of vertices $$X, Y \in S$$, and let $$j$$ denote the graph distance between them. Then:

1. Select an arbitrary $$W \in N_{j+1}(X) \cap N_1(Y)$$. 

	$$ \implies \operatorname{dim}(W \cap (X \cap Y)) \in \{ k - j - 1 , k - j \}$$ 

	**[** since $$\operatorname{dim}(W \cap Y) = k - 1$$ and $$\operatorname{dim}(X \cap Y) \leq Y$$ **]**

	$$ \implies \left (W \cap X \cap Y \right ) = \left ( W \cap X \right )$$

	**[**  since $$\left (W \cap X \cap Y \right )  \leq \left (W \cap X \right )$$ and $$\operatorname{dim}(W \cap X) = k - j - 1$$  **]**

	Now, let $$R = \{ Z : Z \leq V \operatorname{and} \operatorname{dim}(Z \cap (X + Y)) = 0 \}$$, $$S_1(R) = \{ L : L \in R \operatorname{and} \operatorname{dim}(L) = 1 \}$$, $$S_{k-j-1}(X \cap Y) = \{ Z : Z \leq (X \cap Y) \operatorname{and} \operatorname{dim}(Z) = k-j-1 \}$$, $$Q = \{ Z : Z \leq Y \operatorname{and} \operatorname{dim}(X \cap Z) = 0 \}$$, $$S_j(Q) = \{ Z : Z \in Q \operatorname{and} \operatorname{dim}(Z) = j \}$$, and $$T = \{ (L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$. 

	$$ \implies W \cap Y = (W \cap X \cap Y) \oplus Z $$

	**[** for some $$Z \in S_j(Q)$$, since $$\operatorname{dim}(W \cap Y) = k - 1 = (k - j - 1) + j$$ and $$\operatorname{dim}(W \cap X \cap Y) = k - j - 1$$ **]**

	$$ \implies W = L \oplus (W \cap Y) = L \oplus (W \cap X \cap Y) \oplus Z $$ 

	**[** for some $$L \in S_1(R)$$, since $$\operatorname{dim}(W) = k$$, and by similar reasoning as in previous inference **]**

	$$ \implies W \in T $$

	$$ \implies N_{j+1}(X) \cap N_1(Y) \subseteq T $$

	**[** since W is arbitrary **]**

	$$ \implies N_{j+1}(X) \cap N_1(Y) = T $$

	**[** assuming $$T \subseteq N_{j+1}(X) \cap N_1(Y)$$ as well, which is straightforward to check **]**

	Next, partition $$T = \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M}$$ into disjoint subsets, letting $$T_{M} = \{ (L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$ for each $$M \in S_{k-j-1}(X \cap Y)$$.

	$$ \implies \left\vert N_{j+1}(X) \cap N_1(Y) \right\vert $$ 

	$$ = \left\vert T \right\vert $$

	$$ = \left\vert \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M} \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left\vert T_M \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( \frac{q^{n} - q^{k+j}}{q^{k-j} - q^{k-j-1}} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = { k - j \brack 1 }_{q} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = q^{2j + 1}  { k - j \brack 1 }_{q} {n - k - j \brack 1 }_{q} $$







