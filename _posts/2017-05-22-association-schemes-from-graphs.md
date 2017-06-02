---
layout: post
title:  "Association Schemes from Graphs"
date:   2017-05-22
---

I would like to establish some examples of families of (commutative) association schemes arising 
from distance-regular graphs and sets of conjugacy class digraphs of finite groups.

Firstly, suppose that $$G$$ is a distance-regular graph. Let $$\mathcal{V}_{G}$$ denote the vertex set of $$G$$, 
and $$\mathcal{A} := \{ A_{n} : 0 \leq n \leq \operatorname{diam}(G) \}$$ denote a set of distance matrices for $$G$$.
Additionally, define $$S_{i,j}(u,v) := \{ w : w \in \mathcal{V}_{G} \operatorname{and} (d(u, w), d(w, v)) = (i, j) \}$$ for all 
$$0 \leq i,j \leq \operatorname{diam}(G)$$ and all $$u,v \in \mathcal{V}_{G}$$. Now, select any particular $$0 \leq i,j \leq \operatorname{diam}(G)$$. Then for any $$w, x \in \mathcal{V}_{G}$$:

1. $$ \lvert S_{i,j}(w, x) \rvert = \lvert S_{j, i}(w, x) \rvert $$

	**[** since $$G$$ is a simple graph **]**.

2. $$ \lvert S_{i,j}(w,x) \rvert = \lvert S_{i,j}(y,z) \rvert \text{ for all } (y, z) \in \{ (u, v) : u, v \in \mathcal{V}_{G} \operatorname{and} d(u, v) = d(w,x) \}$$

	**[** since $$G$$ is distance-regular **]**.

3. $$ \left ( A_{i} A_{j} \right )_{w, x} $$

	$$ = \sum\limits_{\substack{u \in \mathcal{V}_{G} \\ d(u, w) = i}} \sum\limits_{\substack{v \in \mathcal{V}_{G} \\ d(x, v) = j}} \langle e_{u}, e_{v} \rangle $$

	$$ = \sum\limits_{\substack{v \in \mathcal{V}_{G} \\ d(v, w) = i \operatorname{and} d(x, v) = j}} 1 $$

	$$ = \lvert S_{i,j}(w,x) \rvert $$

    **[** letting $$\langle \cdot , \cdot\rangle$$ denote the standard inner product on $$\mathbb{R}^{\lvert \mathcal{V}_{G} \rvert}$$,

	and $$e_{v}$$ denote the representative vector of $$v$$ in $$\mathbb{R}^{\lvert \mathcal{V}_{G} \rvert}$$ for all $$v \in \mathcal{V}_{G}$$ **]**.


$$ \implies A_{i} A_{j} = A_{j} A_{i} = \sum\limits_{k = 0}^{\operatorname{diam}(G)} p_{i,j}(k) \ A_{k}  \text{ for some } \{ p_{i,j}(k) : 0 \leq k \leq \operatorname{diam}(G) \} \subset \mathbb{N} $$

$$ \implies \mathcal{A} \text{ is a commutative association scheme } $$

**[** since $$i$$ and $$j$$ are arbitrary, in addition to the facts that $$A_{0} = I \in \mathcal{A}$$, $$\sum\limits_{k = 0}^{\operatorname{diam}(G)} A_k = J$$, and $$A_{k}^{T} = A_{k}$$ for all $$0 \leq k \leq \operatorname{diam}(G)$$ by construction **]**.

It then follows in general that every distance-regular graph gives rise to a commutative association scheme in this way, since $$G$$ in this context is arbitrary.


Secondly, suppose now that $$G$$ is a finite group. Let $$e_{G}$$ denote the identity element of $$G$$, $$\operatorname{Cl}(G)$$ denote the set of conjugacy classes of $$G$$, 
 and $$ \mathcal{A} := \{ A_{k} : 1 \leq k \leq \lvert \operatorname{Cl}(G) \rvert \}$$ denote the of set adjacency matrices of
 the set of conjugacy class digraphs of $$G$$ relative a certain ordering of the elements of $$G$$ and $$\operatorname{Cl}(G)$$. Additionally, define $$S_{i,j}(u,v) := \{ w : w \in G, uw^{-1} \in \operatorname{Cl}_{i} \operatorname{and} wv^{-1} \in \operatorname{Cl}_{j} \} $$ for all $$1 \leq i, j \in \lvert \operatorname{Cl}(G) \rvert$$ and all $$u,v \in G$$, letting $$\operatorname{Cl}_{k}$$ denote the $$k$$-th conjugacy class of $$G$$ for all $$ 1 \leq k \leq \lvert \operatorname{Cl}(G) \rvert $$. Then for any particular $$ 1 \leq i, j \leq \lvert \operatorname{Cl}(G) \rvert $$:

 1. Select any $$g, h \in G$$.

    Define

    $$ L_{g} : S_{i,j}(h,e_{G}) \to S_{i,j}(gh,g) $$

    $$L_{g}(w) := gw $$
 
    and

    $$ R_{g^{-1}} : S_{i,j}(h,e_{G}) \to S_{i,j}(hg^{-1},g^{-1}) $$

    $$R_{g^{-1}}(w) := wg^{-1}$$

    . 

    It is apparent that $$L_{g}$$ and $$ L_{g} \circ R_{g^{-1}} $$ are bijections.

    $$ \implies \lvert S_{i,j}(gh,g) \rvert = \lvert S_{i,j}(h,e_{G}) \rvert = \lvert S_{i,j}(ghg^{-1}, e_{G}) \rvert $$

2. Select any  $$1 \leq k \leq \lvert \operatorname{Cl}(G) \rvert$$.

   Observe the fact that $$A_{k} = \sum\limits_{x \in \operatorname{Cl}_{k}} P_x$$ where $$P_{x}$$ denotes a permutation matrix representing the left-translation of the elements of $$G$$ by $$x$$ for all $$x \in \operatorname{Cl}_{k}$$.

   It then follows in general from **1.** that $$\lvert S_{i,j}(u,v) \rvert = \lvert S_{i,j}(w,x) \rvert$$ for all $$(u,v),(w,x) \in \{ (y, z) : y, z \in G \operatorname{and} yz^{-1} \in \operatorname{Cl}_{k} \}$$.

Now, for all $$1 \leq i,j,k \leq \lvert \operatorname{Cl}(G) \rvert$$ and all $$x \in G$$ define:

   * $$T_{i,j}(k) := \{ (g, h) : g \in \operatorname{Cl}_{i}, h \in \operatorname{Cl}_{j},  \operatorname{and} gh \in \operatorname{Cl}_{k} \} \text{ , }$$

     $$P_{i,j}(k) : T_{i,j}(k) \to T_{j,i}(k)$$

     $$ \left ( P_{i,j}(k) \right )(g,h) := (ghg^{-1}, g)$$

     and

     $$Q_{i,j}(x) : S_{i,j}(x, e_{G}) \to T_{i,j}(k) $$

     $$\left ( Q_{i,j}(x) \right )(g) := (xg^{-1}, g) $$

     .

Then for any particular $$1 \leq i,j,k \leq \lvert \operatorname{Cl}(G) \rvert$$:

  * Select any $$g \in \operatorname{Cl}_{k}$$.

    It is apparent that $$P_{i,j}(k)$$, $$Q_{i,j}(g)$$, and $$Q_{j,i}(g)$$ are bijections.

    $$ \implies Q_{j,i}^{-1}(g) \circ P_{i,j}(k) \circ Q_{i,j}(g) \text { is a bijection as well} $$

    $$ \implies \lvert S_{i,j}(g, e_{G}) \rvert = \lvert S_{j,i}(g, e_{G}) \rvert $$

    It then similarly follows from **1.** and **2.** that 

    $$ \lvert S_{i,j}(u, v) \rvert  = \lvert S_{i,j}(w,x) \rvert = \lvert S_{j,i}(w,x) \rvert =  \lvert S_{j, i}(u,v) \rvert $$

    and moreover that

    $$ \left ( A_{i} A_{j} \right )_{u,v} = \left ( A_{i}A_{j} \right )_{w,x} = \left ( A_{j}A_{i} \right )_{w,x} = \left ( A_{j}A_{i} \right )_{u,v} $$

    for all $$(u,v), (w, x) \in \{ (y, z) : y, z \in G \operatorname{and} yz^{-1} \in \operatorname{Cl}_{k} \}$$ .

Next, observe that: 

  * $$I \in \mathcal{A} \text{ , }$$

    since $$\{e_{G}\} \in \operatorname{Cl}(G)$$.
  * $$ \sum\limits_{i = 1}^{\lvert \operatorname{Cl}(G) \rvert} A_{i} = J \text{, }$$ 

    since every element of $$G$$ belongs to exactly one conjugacy class of $$G$$.
  * $$A_{i}^{T} \in \mathcal{A}$$ 

    for all $$ 1 \leq i \leq \lvert \operatorname{Cl}(G) \rvert \text{ , } $$

    since for all $$ 1 \leq i \leq \lvert \operatorname{Cl}(G) \rvert$$
    
    there is a $$ 1 \leq j \leq \lvert \operatorname{Cl}(G) \rvert$$ such that $$gh^{-1} \in C_{i}$$ if and only if $$hg^{-1} \in C_{j}$$

    for all $$g,h \in G$$.
  * $$A_{i}A_{j} = A_{j}A_{i} = \sum\limits_{k = 1}^{\lvert \operatorname{Cl}(G) \rvert} p_{i,j}(k) \ A_{k}$$ 

    for some $$\{ p_{i,j}(k) : 1 \leq k \leq \lvert \operatorname{Cl}(G) \rvert \} \subset \mathbb{N}$$ and all $$ 1 \leq i, j \leq \lvert \operatorname{Cl}(G) \rvert$$, 

    following from the previous point.

 $$ \implies \mathcal{A} \text{ is a commutative association scheme } $$

It then follows in general that the set of conjugacy classes of every finite group gives rise to a commutative association scheme in this way, since $$G$$ in this context is arbitrary.

*In conclusion, it is indeed the case that distance-regular graphs and sets of conjugacy classes of finite groups give rise to commutative association schemes in the ways presented in this post. It may be useful to note that it essentially follows that every distance-regular graph is walk-regular from the facts that the distance matrices of a distance-regular graph are simultaneously diagonalizable, the number of distinct eigenvalues of distance-regular graph is equal to one more than its diameter, in addition to the fact that distance-regular graphs give rise to commutative association schemes. Also, the fact that there are sets of projections onto the generalized eigenspaces of the adjacency matrices of the set of conjugacy class digraphs that form bases for the Bose-Mesner algebra of the conjugacy class scheme of a finite group is arguably useful for finding general expressions for the spectra of conjugacy class digraphs of finite groups; I hope to expand on this point in detail in a future post. Lastly, it may also be worth noting that there are arguably useful examples of families of association schemes arising from complex commutants of sets of permutation matrices as well as sets of orbits of certain actions of finite groups on certain sets of objects; however, these families of association schemes are not necessarily commutative and so my intent is to perhaps talk about them in a separate post in the future as well.*