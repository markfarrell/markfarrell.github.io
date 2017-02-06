---
layout: post
title:  "Grassmann Graphs Are Distance-Regular"
date:   2017-02-05
---

In this post, my goal is to verify that every Grassmann graph is distance-regular.

Suppose that we are given arbitrary natural number $$n$$, a natural number $$k \leq n$$, and a prime power $$q$$. Let $$S = \{ W : W \leq V \operatorname{and} \operatorname{dim}(W) = k \}$$ denote the set of $$k$$-dimensional subspaces of a vector space $$V$$ over the finite field $$F_{q}$$ of order $$q$$. Consider the simple graph $$G=(S,E)$$ formed with the set $$S$$ as vertices and the set $$E=\{\{W,Z\} : W,Z \in S \operatorname{and} \operatorname{dim}(W \cap Z)= k - 1\} $$ as edges. Select an arbitrary pair of vertices $$X, Y \in S$$, and let $$j$$ denote the graph distance between them. Then:

1. Firstly, let $$N_{j+1}(X) = \{ Z : Z \in S \operatorname{and} d(X, Z) = j + 1 \}$$ and $$N_1(Y) = \{ Z : Z \in S \operatorname{and} d(Y,Z) = 1 \}$$.

	Now, select an arbitrary $$W \in N_{j+1}(X) \cap N_1(Y)$$.

	$$ \implies \operatorname{dim}(W \cap X \cap Y) \in \{ k - j - 1 , k - j \}$$ 

	**[** since $$\operatorname{dim}(W \cap Y) = k - 1$$, $$\operatorname{dim}(X \cap Y) = k - j$$, and $$X \cap Y \leq Y$$ **]**

	$$ \implies W \cap X \cap Y = W \cap X $$

	**[**  since $$W \cap X \cap Y  \leq W \cap X $$ and $$\operatorname{dim}(W \cap X) = k - j - 1$$  **]**

	Secondly, let $$R = \{ Z : Z \leq V \operatorname{and} \operatorname{dim}(Z \cap (X + Y)) = 0 \}$$, $$S_1(R) = \{ L : L \in R \operatorname{and} \operatorname{dim}(L) = 1 \}$$, $$S_{k-j-1}(X \cap Y) = \{ Z : Z \leq (X \cap Y) \operatorname{and} \operatorname{dim}(Z) = k-j-1 \}$$, $$Q = \{ Z : Z \leq Y \operatorname{and} \operatorname{dim}(X \cap Z) = 0 \}$$, $$S_j(Q) = \{ Z : Z \in Q \operatorname{and} \operatorname{dim}(Z) = j \}$$, and $$T = \{ L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$. 

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

	Yet, $$M_1 \oplus Z_1$$ and $$M_2 \oplus Z_2$$ are distinct $$k-1$$ dimensional subspaces of $$Y$$. 

	$$ \implies \operatorname{dim}((M_1 \oplus Z_1) \cap (M_2 \oplus Z_2)) = k - 2 \neq k - 3$$

	$$ \implies \operatorname{dim}(Z_1 \cap Z_2) \neq j - 1$$

	**[** i.e. the hypothesis in context is false, since a contradiction has been established **]**

	$$\implies \operatorname{dim}(Z_1^{'} \cap Z_2^{'}) = j \text { for all } Z_1^{'}, Z_2^{'} \in S_j(Q)$$

	$$\implies \lvert S_j(Q) \rvert = 1 $$

	Lastly, partition $$T = \left ( \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M} \right )$$ into disjoint subsets, letting $$T_{M} = \{ L \oplus M \oplus Z : L \in S_1(R), M \in S_{k-j-1}(X \cap Y), \operatorname{and} Z \in S_{j}(Q) \}$$ for each $$M \in S_{k-j-1}(X \cap Y)$$. Then:

	$$ \left\vert N_{j+1}(X) \cap N_1(Y) \right\vert $$ 

	$$ = \left\vert T \right\vert $$

	$$ = \left\vert \left ( \bigsqcup\limits_{M \in S_{k-j-1}(X \cap Y)} T_{M} \right ) \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left\vert T_M \right\vert $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left\vert \{ (L \oplus M : L \in S_1(R) \operatorname{and} M \in S_{k-j-1}(X \cap Y) \} \right\vert $$

	**[** since, by the previous point, $$\lvert S_j(Q) \rvert = 1$$ **]**

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L_1 \in (V \setminus (X + Y)) } \left( \frac{\lvert \{ L_1 \oplus M \} \rvert }{\lvert \{ L_2 : L_2 \in (V \setminus (X + Y)) \operatorname{and} L_1 \oplus M = L_2 \oplus M \rvert} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L \in (V \setminus (X + Y)) } \left( \frac{1}{\lvert L \oplus M \rvert - \lvert M \rvert} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \sum\limits_{L \in (V \setminus (X + Y)) } \left( \frac{1}{q^{k-j} - q^{ k - j - 1}} \right) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( \frac{\lvert V \setminus (X + Y) \rvert }{q^{k-j} - q^{k-j-1}} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( \frac{q^{n} - q^{k+j}}{q^{k-j} - q^{k-j-1}} \right ) $$

	$$ = \sum\limits_{M \in S_{k-j-1}(X \cap Y)} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = { k - j \brack 1 }_{q} \left ( q^{2j + 1} {n - k - j \brack 1 }_{q} \right ) $$

	$$ = q^{2j + 1}  { k - j \brack 1 }_{q} {n - k - j \brack 1 }_{q} $$

	which only depends on $$d(X,Y) = j$$.

2. Firstly, let $$ R = \{ Z : Z \leq X \operatorname{and} \operatorname{dim}(X \cap Z) = 0 \} $$, $$ Q = \{ Z : Z \leq Y \operatorname{and}  \operatorname{dim}(Y \cap Z) = 0 \}$$, $$S_1(R) = \{ L : L \in R \operatorname{and} \operatorname{dim}(L) = 1 \}$$, $$S_{j-1}(Q) = \{ Z : Z \in Q \operatorname{and} \operatorname{dim}(Z) = j - 1 \}$$, and $$ T = \{ (X \cap Y) \oplus L \oplus Z : L \in S_1(R) \operatorname{and} Z \in S_{j-1}(Q) \}$$.

	Secondly, let $$N_{j-1}(X) = \{ Z : Z \in S \operatorname{and} d(X, Z) = j - 1 \}$$ and $$N_1(Y) = \{ Z : Z \in S \operatorname{and} d(Y,Z) = 1 \}$$.

	Now, select an arbitrary $$ W \in N_{j-1}(X) \cap N_{1}(Y) $$.

	$$ \implies W \cap X = (X \cap Y) \oplus L $$ and $$ W \cap Y  = (X \cap Y) \oplus Z $$

	**[** for some $$ L \in S_1(R) $$ and some $$ Z \in S_{j-1}(Q) $$ **]**

	$$ \implies W = (W \cap X) + (W \cap Y) = (X \cap Y) \oplus L \oplus Z $$

	**[** since $$((W \cap X) + (W \cap Y)) \leq W$$, and $$\operatorname{dim}((W \cap X) + (W \cap Y)) = \operatorname{dim}((X \cap Y) \oplus L \oplus Z) = (k - j) + 1 + j -1 = k = \operatorname{dim}(W) $$ **]**

	$$ \implies W \in T $$

	$$ \implies N_{j-1}(X) \cap N_{1}(Y) \subseteq T $$

	**[** since $$W$$ is arbitrary **]**

	$$ \implies N_{j-1}(X) \cap N_{1}(Y) =  T $$

	**[** assuming that $$ T \subseteq N_{j-1}(X) \cap N_{1}(Y) $$ as well, which is straightforward to check **]**

	Thirdly, let $$S_j(R) = \{ Z : Z \in R \operatorname{and} \operatorname{dim}(Z) = j \}$$. 

	Now, assume that $$\operatorname{dim}(Z_1 \cap Z_2) < j $$ for some $$Z_1, Z_2 \in S_j(R)$$.

	$$ \implies \operatorname{dim}(((X \cap Y) \oplus Z_1) \cap ((X \cap Y) \oplus Z_2)) $$

	$$ = \operatorname{dim}((X \cap Y) \oplus (Z_1 \cap Z_2)) $$

	$$ = \operatorname{dim}(X \cap Y) + \operatorname{dim}(Z_1 \cap Z_2) $$

	$$ = (k - j) + \operatorname{dim}(Z_1 \cap Z_2) $$

	$$ < k $$

	Yet, $$\operatorname{dim}((X \cap Y) \oplus Z_1) \cap ((X \cap Y) \oplus Z_2)) = \operatorname{dim}(X \cap X) = \operatorname{dim}(X) = k$$.

	$$ \implies \operatorname{dim}(Z_1 \cap Z_2) \nless j $$


	$$ \implies \operatorname{dim}(Z_1^{'} \cap Z_2^{'}) = j \text{ for all } Z_1^{'}, Z_2^{'} \in S_j(R) $$

	$$ \implies \lvert S_j(R) \rvert = 1 $$

	By similar reasoning, $$\lvert S_j(Q) \rvert = 1$$, letting $$S_j(Q) = \{ Z : Z \in Q \operatorname{and} \operatorname{dim}(Z) = j \}$$.

	Since $$\operatorname{X \cap Y} = k - j$$, it is apparent now that $$S_1(R) = \{ L : L \leq X_0 \operatorname{and} \operatorname{dim}(L) = 1 \} $$, letting $$X_0$$ denote the only element of $$S_j(R)$$; likewise, it is apparent now that $$S_{j-1}(Q) = \{ Z : Z \leq Y_{0} \operatorname{and} \operatorname{dim}(Z) = j - 1 \}$$, letting $$Y_0$$ denote the only element of $$S_{j}(Q)$$.

	$$ \implies \lvert N_{j-1}(X) \cap N_{1}(Y) \rvert $$

	$$ = \lvert T \rvert $$

	$$ = \left\vert \left ( \bigsqcup\limits_{L \in S_1(R)} \{ (X \cap Y) \oplus L \oplus Z : Z \in S_{j-1}(Q) \} \right ) \right\vert $$

	$$ = \sum\limits_{L \in S_1(R)} \lvert \{ (X \cap Y) \oplus L \oplus Z : Z \in S_{j-1}(Q) \} \rvert $$

	$$ = \sum\limits_{L \in S_1(R)} \lvert S_{j-1}(Q) \rvert $$

	$$ = \sum\limits_{L \in S_1(R)} \lvert \{ Z : Z \leq Y_{0} \operatorname{and} \operatorname{dim}(Z) = j - 1 \} \rvert $$

	$$ = \sum\limits_{L \in S_1(R)} \left ( { j \brack j - 1 }_q \right ) $$

	$$ = \left ( \lvert  \{ L : L \leq X_0 \operatorname{and} \operatorname{dim}(L) = 1 \}  \rvert \right ) \left ( { j \brack j - 1 }_q \right ) $$

	$$ = {j \brack 1}_q {j \brack j - 1}_q $$

	$$ = {j \brack 1 }_q^2 $$

	which depends only on $$d(X, Y) = j$$.

It turns out that **1.** and **2.** are sufficient to establish that $$G$$ is distance-regular. 

Therefore every Grassmann graph is distance-regular, since $$G$$ is arbitrary.


