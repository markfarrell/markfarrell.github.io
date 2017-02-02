---
layout: post
title:  "Grassman Graphs Are Distance-Regular"
date:   2017-01-20
---

In this post, my goal is to verify that every Grassman graph is distance-regular.

Suppose that we are given arbitrary natural number $$n$$, a natural number $$k \leq n$$, and a prime power $$q$$. Let $$S = \{ W : W \leq V \operatorname{and} \operatorname{dim}(W) = k \}$$ denote the set of $$k$$-dimensional subspaces of a vector space $$V$$ over the finite field $$F_{q}$$ of order $$q$$. Consider the simple graph $$G=(S,E)$$ formed with the set $$S$$ as vertices and the set $$E=\{\{W,Z\} : W,Z \in S \operatorname{and} \operatorname{dim}(W \cap Z)= k -1\} $$ as edges. Select an arbitrary pair of vertices $$X, Y \in S$$, and let $$j$$ denote the graph distance between them. Then:

1. Firstly, select an arbitrary $$W \in N_{j+1}(X) \cap N_1(Y)$$. 

	$$ \implies \operatorname{dim}(W \cap (X \cap Y)) \in \{ k - j - 1 , k - j \}$$ 

	**[** since $$\operatorname{dim}(W \cap Y) = k - 1$$ and $$\operatorname{dim}(X \cap Y) \leq Y$$ **]**

	$$ \implies \left (W \cap X \cap Y \right ) = \left ( W \cap X \right )$$

	**[**  since $$\left (W \cap X \cap Y \right )  \leq \left (W \cap X \right )$$ and $$\operatorname{dim}(W \cap X) = k - j - 1$$  **]**

	Secondly, let $$R = \{ Z : Z \leq V \operatorname{and} \operatorname{dim}(Z \cap (X + Y)) = 0 \}$$, $$S_1(R) = \{ L : L \in R \operatorname{and} \operatorname{dim}(L) = 1 \}$$, $$S_{k-j-1}(X \cap Y) = \{ Z : Z \leq (X \cap Y) \operatorname{and} \operatorname{dim}(Z) = k-j-1 \}$$, $$Q = \{ Z : Z \leq Y \operatorname{and} \operatorname{dim}(X \cap Z) = 0 \}$$, $$S_j(Q) = \{ Z : Z \in Q \operatorname{and} \operatorname{dim}(Z) = j \}$$, and $$T = \{ (L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$. 

	$$ \implies W \cap Y = (W \cap X \cap Y) \oplus Z $$

	**[** for some $$Z \in S_j(Q)$$, since $$\operatorname{dim}(W \cap Y) = k - 1 = (k - j - 1) + j$$ and $$\operatorname{dim}(W \cap X \cap Y) = k - j - 1$$ **]**

	$$ \implies W = L \oplus (W \cap Y) = L \oplus (W \cap X \cap Y) \oplus Z $$ 

	**[** for some $$L \in S_1(R)$$, since $$\operatorname{dim}(W) = k$$, and by similar reasoning as in the previous inference **]**

	$$ \implies W \in T $$

	$$ \implies N_{j+1}(X) \cap N_1(Y) \subseteq T $$

	**[** since W is arbitrary **]**

	$$ \implies N_{j+1}(X) \cap N_1(Y) = T $$

	**[** assuming $$T \subseteq N_{j+1}(X) \cap N_1(Y)$$ as well, which is straightforward to check **]**

	Thirdly, select arbitrary $$Z_1, Z_2 \in S_{j}(Q)$$. Then, independent of any choice of $$M \in S_{k-j-1}(X \cap Y)$$, it is possible to deduce that: 

	$$ \operatorname{dim}((M \oplus Z_1) \cap (M \oplus Z_2)) $$

	$$ = \operatorname{dim}(M \oplus (Z_1 \cap Z_2)) $$

	$$ = \operatorname{dim}(M) + \operatorname{dim}(Z_1 \cap Z_2) $$

	$$ = (k - j - 1) + \operatorname{dim}(Z_1 \cap Z_2) $$

	$$ \in \{ k - 2, k - 1 \} $$

	$$ \implies \operatorname{dim}(Z_1 \cap Z_2) \in \{ j - 1, j \} $$

	It follows that, in general, the dimension of the intersection of any pair of subspaces in $$S_{j}(Q)$$ is either $$j-1$$ or $$j$$.

	Now, select arbitrary $$M_1, M_2 \in S_{k-j-1}(X \cap Y)$$ such that $$M_1 \neq M_2$$, and select arbitrary $$Z_1, Z_2 \in S_j(Q)$$ Assume that $$\operatorname{dim}(Z_1 \cap Z_2) = j - 1 $$. Then:

	$$ \operatorname{dim}((M_1 \oplus Z_1) \cap (M_2 \oplus Z_2)) $$

	$$ = \operatorname{dim}((M_1 \cap M_2) \oplus (Z_1 \cap Z_2)) $$

	$$ = (k - j - 2) + (j - 1) $$

	$$ = k - 3 $$

	Yet, $$M_1 \oplus Z_1$$ and $$M_2 \oplus Z_2$$ are distinct $$k-1$$ dimensional subspaces of $$Y$$, which means that it must necessarily be the case that $$\operatorname{dim}((M_1 \oplus Z_1) \cap (M_2 \oplus Z_2)) = k - 2$$.

	$$ \implies \operatorname{dim}(Z_1 \cap Z_2) \neq j - 1 $$

	**[** i.e. the hypothesis in context is false, since a contradiction has been established **]**

	$$ \implies \operatorname{dim}(Z_1 \cap Z_2) = j $$ 

	**[** since, by the previous point, it is necessary that $$\operatorname{dim}(Z_1 \cap Z_2) \in \{ j - 1, j \}$$ nonetheless **]**

	$$ \implies Z_1 = Z_2 $$

	**[** since $$\left\vert Z_1 \right\vert = \lvert Z_1 \cap Z_2 \rvert = \lvert Z_2 \rvert = q^{j} $$ **]**

	$$ \implies \lvert S_j(Q) \rvert = 1 $$

	**[** since $$Z_1$$ and $$Z_2$$ are arbitrary, which means that the intersection of any pair of subspaces in $$S_j(Q)$$ must be equal **]**

	Lastly, partition $$T = \left ( \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M} \right )$$ into disjoint subsets, letting $$T_{M} = \{ (L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$ for each $$M \in S_{k-j-1}(X \cap Y)$$. Then:

	$$ \left\vert N_{j+1}(X) \cap N_1(Y) \right\vert $$ 

	$$ = \left\vert T \right\vert $$

	$$ = \left\vert \left ( \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M} \right ) \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left\vert T_M \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left\vert \{ (L \oplus M : L \in S_1(R), M \in S_{k-j-1}(X \cap Y) \} \right\vert $$

	**[** since, by the previous point, $$\lvert S_j(Q) \rvert = 1$$ **]**

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L_1 \in (V \setminus (X + Y)) } \left( \frac{\lvert \{ L_1 \oplus M \} \rvert }{\lvert \{ L_2 : L_2 \in (V \setminus (X + Y)) \operatorname{and} L_1 \oplus M = L_2 \oplus M \rvert} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L \in (V \setminus (X + Y)) } \left( \frac{1}{\lvert L \oplus M \rvert - \lvert M \rvert} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L \in (V \setminus (X + Y)) } \left( \frac{1}{q^{k-j} - q^{ k - j - 1}} \right) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( \frac{\lvert V \setminus (X + Y) \rvert }{q^{k-j} - q^{k-j-1}} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( \frac{q^{n} - q^{k+j}}{q^{k-j} - q^{k-j-1}} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = { k - j \brack 1 }_{q} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = q^{2j + 1}  { k - j \brack 1 }_{q} {n - k - j \brack 1 }_{q} $$


	which is independent of $$X$$ and $$Y$$.

2.








