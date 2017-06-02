---
layout: post
title:  "Grassmann Graphs Are Distance-Transitive"
date:   2017-02-14
---

I would like to verify that every Grassmann graph is distance-transitive.

Suppose that we are given arbitrary natural number $$n$$, a natural number $$k \leq n$$, and a prime power $$q$$. Let $$S = \{ W : W \leq V \text{ and }  \operatorname{dim}(W) = k \}$$ denote the set of $$k$$-dimensional subspaces of a vector space $$V$$ over the finite field $$\mathbb{F}_{q}$$ of order $$q$$. Consider the simple graph $$G=(S,E)$$ formed with the set $$S$$ as vertices and the set $$E=\{\{W,Z\} : W,Z \in S \operatorname{and} \operatorname{dim}(W \cap Z)= k - 1\} $$ as edges. Then:


1. Suppose that $$L : V \to V$$ is a linear isomorphism.

	Let $$F : S \to S$$ be a function on the vertices of $$G$$ where $$F(U) := \operatorname{image}(L\vert_U)$$ for all $$U \in S$$.

	Now, select an arbitrary pair of vertices $$X,Y \in S$$ such that $$X$$ is adjacent to $$Y$$ on $$G$$.

	$$ \implies \operatorname{dim}(F(X) \cap F(Y)) $$

	$$ = \operatorname{dim}(\operatorname{image}(L\vert_X) \cap \operatorname{image}(L \vert_Y))$$

	$$ = \operatorname{dim}(\{ v : v = L(x) = L(y) \text { for some } x \in X \text{ and } y  \in Y\}) $$

	$$ = \operatorname{dim}(\{ v : L^{-1}(v) = x = y \text { for some } x \in X \text{ and } y  \in Y\}) $$

	$$ = \operatorname{dim}(\{ v : L^{-1}(v) = z \text { for some } z \in X \cap Y \}) $$

	$$ = \operatorname{dim}(\{ v : v = L(z) \text { for some } z \in X \cap Y \}) $$

	$$ = \operatorname{dim}(\operatorname{image}(X \cap Y))$$

	$$ = k - 1 $$

	$$ \implies F(X) \text{ is adjacent to } F(Y) $$

	$$ \implies F \in \operatorname{Aut}(G) \text{ is an automorphism on } G$$

	**[** since $$X$$ and $$Y$$ are arbitrary, defining $$F^{-1} : S \to S$$ as $$F^{-1}(U) := \operatorname{image}(L^{-1}\vert_U)$$ for all $$U \in S$$**]**.


2. Suppose that $$W_1, W_2, X_1, X_2 \in S$$ such that $$d(W_1,W_2)=d(X_1,X_2)$$. Then:

	$$W_1 = (W_1 \cap W_2) \oplus Y_{W_2} $$ and $$ W_2 = (W_1 \cap W_2) \oplus Y_{W_1}$$

	**[** for some $$Y_{W_2} \leq W_1$$ where $$ Y_{W_2} \cap W_2 = \{0\} $$, and some $$Y_{W_1} \leq W_2$$ where $$ Y_{W_1} \cap W_1 = \{0\} $$ **]**

	$$\implies V = (W_1 + W_2) \oplus Z_{W_1 + W_2} = (W_1 \cap W_2) \oplus Y_{W_1} \oplus Y_{W_2} \oplus Z_{W_1 + W_2} $$

	**[** for some $$Z_{W_1 + W _2} \leq V$$ where $$Z_{W_1 + W_2} \cap (W_1 + W_2) = \{0\}$$ **]**

	Similarly, it must be the case that:

	$$X_1 = (X_1 \cap X_2) \oplus Y_{X_2} $$ and $$ X_2 = (X_1 \cap X_2) \oplus Y_{X_1}$$

	**[** for some $$Y_{X_2} \leq X_1$$ where $$ Y_{X_2} \cap X_2 = \{0\} $$, and some $$Y_{X_1} \leq X_2$$ where $$ Y_{X_1} \cap X_1 = \{0\} $$ **]**

	$$\implies V = (X_1 + X_2) \oplus Z_{X_1 + X_2} = (X_1 \cap X_2) \oplus Y_{X_1} \oplus Y_{X_2} \oplus Z_{X_1 + X_2} $$

	**[** for some $$Z_{X_1 + X _2} \leq V$$ where $$Z_{X_1 + X_2} \cap (X_1 + X_2) = \{0\}$$ **]**

	Now, note that $$\operatorname{dim}(W_1 \cap W_2) = \operatorname{dim}(X_1 \cap X_2)$$, $$\operatorname{dim}(Y_{W_1}) = \operatorname{dim}(Y_{W_2}) = \operatorname{dim}(Y_{X_1}) = \operatorname{dim}(Y_{X_1})$$, and $$\operatorname{dim}(Z_{W_1 + W_2}) = \operatorname{dim}(Z_{X_1 + X_2})$$ - since $$d(W_1,W_2)=d(X_1,X_2)$$ on $$G$$.

	This means here that it is possible to construct a linear isomorphism $$L : V \to V$$ such that $$\operatorname{image}(L\vert_{W_1 \cap W_2}) = X_1 \cap X_2$$,  $$\operatorname{image}(L\vert_{Y_{W_1}}) = Y_{X_1}$$, $$\operatorname{image}(L\vert_{Y_{W_2}}) = X_{X_2}$$, and $$ \operatorname{image}(L\vert_{Z_{W_1 + W_2}}) = Z_{X_1 + X_2}$$. 

	By **1.**, this implies that there is an automorphism $$F \in \operatorname{Aut}(G)$$ such that $$F(W_1) = X_1$$ and $$F(W_2) = X_2$$, where $$F(U) := \operatorname{image}(L\vert_{U})$$ for all $$U \in S$$.

	Hence $$G$$ is distance-transitive, since $$W_1, W_2, X_1$$ and $$X_2$$ are arbitrary.

By **1.** and **2.**, it follows that Grassmann graphs are distance-transitive in general.
