---
layout: post
title:  "Fourier Transforms on Coherent Algebras"
date:   2017-12-18
---

I would like to elaborate on how the theory of duality in coherent algebras generalizes the Fourier theory of finite abelian
groups in a way that could be useful towards e.g. the classification of distance-regular graphs, continuing from where I left
off in my previous post.

Suppose that $$\mathcal{W}$$ is a commutative coherent algebra (of order $$n$$ and dimension $$d$$).

Let $$\Gamma(\mathcal{W})$$ and $$\Lambda(\mathcal{W})$$ denote the sets of Schur-primitive and primitive matrices
in $$\mathcal{W}$$ respectively.

A **duality mapping** on $$\mathcal{W}$$ is a linear automorphism $$T : \mathcal{W} \to \mathcal{W}$$ such that:

1. $$T(MN) = T(M) \circ T(N) $$ for all $$M, N \in \mathcal{W}$$.

2. $$T(M \circ N) = \frac{1}{n} T(M) \ T(N) $$ for all  $$M, N \in \mathcal{W}$$.

I would propose that $$\mathcal{W}$$ is self-dual if and only if there is a duality mapping on $$\mathcal{W}$$.

1. Suppose that there is a duality mapping $$T : \mathcal{W} \to \mathcal{W}$$ on $${W}$$.
	
	$$\implies T \left ( \frac{1}{n}  A \right ) =  \frac{1}{n}  T \left ( A \circ A \right ) =  T \left ( \frac{1}{n}  A \right )^{2} \in \Lambda(\mathcal{W})$$ for all $$A \in \Gamma(\mathcal{W})$$.

	It follows that there are orderings $$\Gamma(\mathcal{W}) = \{ A_{j} : 1 \leq j \leq d \}$$ and $$\Lambda(\mathcal{W}) := \{ E_{j} : 1 \leq j \leq d \}$$ on the sets of Schur-primitive and primitive matrices in $$\mathcal{W}$$ such that $$T(A_j) = n \overline{E_j}$$ for all $$1 \leq j \leq d$$.

	Let $$P \in \operatorname{Mat}_{d \times d}(\mathbb{C})$$ denote the character table of $$W$$ relative to this ordering.

	$$ \implies T(E_j) = \sum\limits_{k = 1}^{d} \overline{ \left ( \frac{1}{n} P_{j,k} \right ) }\ T \left (A_k \right ) = \overline{ \left ( \sum\limits_{k = 1}^{d} P_{j,k} \ E_k \right ) } = \overline{A_{j}} = A_{j} \text { for all } 1 \leq j \leq d $$.

	Now, recall from my previous post that $$E_{j} = \sum\limits_{k = 1}^{d} P_{j,k}^{-1} \ A_{k}$$ for all $$1 \leq j \leq d$$.

	$$ \implies P \overline{P} = n I $$ and hence $$\mathcal{W}$$ is self-dual.

2. 	Conversely, suppose that $$\mathcal{W}$$ is self-dual.

	Then there are orderings $$\Gamma(\mathcal{W}) = \{ A_{j} : 1 \leq j \leq d \}$$ and $$\Lambda(\mathcal{W}) := \{ E_{j} : 1 \leq j \leq d \}$$ on the sets of Schur-primitive and primitive matrices in $$\mathcal{W}$$ such that $$ P \overline{P} = n I $$ for the character table $$P$$ of $$\mathcal{W}$$
	relative to this ordering.

	It is then apparent that the linear automorphism $$T : \mathcal{W} \to \mathcal{W}$$ defined as $$T(E_j) := A_j$$ for all $$ 1 \leq j \leq d $$
	is a duality mapping on $$\mathcal{W}$$.

So $$\mathcal{W}$$ is indeed self-dual if and only if there is a duality mapping on $$\mathcal{W}$$.

I would like to elaborate now on how the duality theory of commutative coherent algebras is related to the Fourier theory of finite abelian groups.

For every finite group $$G$$, define the coherent algebra $$\mathcal{W}_{G} := \operatorname{span} \{ P_{g} : g \in G \} \subseteq \operatorname{Mat}_{G \times G}(\mathbb{C})$$ where $$P_{g} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ is defined as $$ \left ( P_{g} \right )_{x,y} := \begin{cases} 1 & \text{if } xy^{-1} = g \\ 0 & \text{otherwise} \end{cases}$$ for all $$x, y \in G$$.

Observe, [from a previous post](/2017/05/31/spectra-of-conjugacy-class-graphs.html), that a character table $$P$$ of $$\mathcal{W}_{G}$$ for a finite abelian group $$G$$ can be identified as a [character table](https://en.wikipedia.org/wiki/Character_table) for $$G$$ in the usual sense of term and that $$PP^{*} = nI$$.

Next, for any finite cyclic group $$G$$ with generator $$g$$:

* Let $$\chi_{g^{j}} : G \to \mathbb{C}^{*}$$ denote the character of $$G$$ such that $$\chi_{g^{j}}(g) = \operatorname{exp} \left ( \frac{2 \pi i}{\vert G \vert} \right )^{j} $$ for all $$ 1 \leq j \leq \vert G \vert $$.
	
	$$ \implies \chi_{x}(y) = \chi_{y}(x) \text { for all } x, y \in G $$

	It can then be concluded that $$\mathcal{W}_{G}$$ is self-dual, define the character table $$P \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$ of $$G$$
	as $$P_{x, y} := \overline{\chi_{y}(x)}$$ for all $$x, y \in G$$.


Now, assume the fact that the tensor product $$\mathcal{X} \otimes \mathcal{Y} := \{ M \otimes N : M \in \mathcal{X}, N \in \mathcal{Y} \}$$ of coherent
algebras $$\mathcal{X}$$ and $$\mathcal{Y}$$ is a coherent algebra.

It follows that for any finite abelian group $$G$$, $$\mathcal{W}_{G}$$ can be identified with the tensor product 
$$\bigotimes\limits_{H \in S} \mathcal{W}_{H}$$ of coherent algebras $$ \{ \mathcal{W}_{H} \in \operatorname{Mat}_{H \times H}(\mathbb{C}) : H \in S \} $$ for a finite set $$S$$ of finite cyclic groups, essentially as a consequence of the [structure theorem](https://groupprops.subwiki.org/wiki/Structure_theorem_for_finitely_generated_abelian_groups) for finite abelian groups.

The tensor product of self-dual coherent algebras is self-dual, since $$P_{\mathcal{X}} \otimes P_{\mathcal{Y}}$$ is a character table 
for the tensor product $$\mathcal{X} \otimes \mathcal{Y}$$ of commutative coherent algebras $$\mathcal{X}$$ and $$\mathcal{Y}$$
with character tables $$P_{\mathcal{X}}$$ and $$P_{\mathcal{Y}}$$.

So, for any finite abelian group $$G$$, $$\mathcal{W}_{G}$$ is self-dual, and a duality mapping $$\mathcal{W}_{G}$$ can be identified with a Fourier transform on $$G$$.

Moreover, certain properties of a Fourier transform on a finite abelian group $$G$$ can be identified with properties of a duality mapping on $$\mathcal{W}_{G}$$:

* For example, suppose that $$T : \mathcal{W}_{G} \to \mathcal{W}_{G}$$ is a duality mapping on $$\mathcal{W}$$.

	Let $$L^{2}(G)$$ denote the space of complex-valued functions on $${G}$$.
	
	For all $$f \in L^{2}(G)$$, define $$M_{f} \in \mathcal{W}_{G}$$
	as $$\left ( M_{f} \right )_{x, y} := f(x^{-1}y)$$ for all $$x, y \in G$$.

	Then $$T(M_{f \star g}) = T(M_{f}M_{g}) = T(M_{f}) \circ T(M_{g})$$ for all $$f,g \in L^{2}(G)$$ on $$G$$

	with convolution $$f \star g$$, which is to ultimately say that a duality mapping on a product of elements of $$W_{G}$$ can be identified with a Fourier transform of a convolution of complex-valued functions on $$G$$.

Lastly, I would like to return to how the duality theory of commutative coherent algebras could be useful towards e.g. the classification of distance-regular graphs.

The commutative coherent algebra $$\mathcal{W}$$ is said to be **metric** (relative to $$A$$) if $$\mathcal{W} = \operatorname{span} \{ I, A, A^{2}, \cdots \}$$ for some $$A \in \Gamma(\mathcal{W})$$;
dually, $$\mathcal{W}$$ is said to be **cometric** (relative to $$E$$) if $$\mathcal{W} = \operatorname{span} \{ J, E, E^{\circ 2}, \cdots \}$$ for some $$E \in \Lambda(\mathcal{W})$$.

Suppose $$\mathcal{W}$$ is self-dual with duality mapping $$T : \mathcal{W} \to \mathcal{W}$$ on $${W}$$. 

By properties of $$T$$, observe that:

* If $$\mathcal{W}$$ is metric relative to $$A \in \Gamma(\mathcal{W})$$, then $$\mathcal{W} = \operatorname{span} \{ T(I), T(A), T(A^{2}), \cdots \} = \operatorname{span} \{J, E, E^{\circ 2}, \cdots \}$$ for some $$E \in \Lambda(\mathcal{W})$$.
* Dually, if $$\mathcal{W}$$ is cometric relative to $$E \in \Lambda(\mathcal{W})$$,
	then $$\mathcal{W} = \operatorname{span} \{ T(J), T(E), T(E^{\circ 2}), \cdots \} = \operatorname{span} \{I, A, A^{2}, \cdots \}$$ for some $$A \in \Gamma(\mathcal{W})$$.

So, a self-dual coherent algebra is metric if and only if it is cometric.

It turns out that coherent algebras that are both metric and symmetric can be identified with the adjacency algebras of distance-regular graphs.

Distance-regular graphs whose adjacency algebras are self-dual must then satisfy a number of additional properties and constraints that may be useful
towards e.g. classifying them. For example, it is ultimately apparent from my previous that the multiplicities of the eigenvalues of a self-dual distance-regular graph are the valencies of its distance-graphs. I will continue to elaborate on observations about self-dual distance-regular graphs that could be useful towards e.g. classifying them in future posts.

















	

