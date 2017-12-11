---
layout: post
title:  "Duality in Coherent Algebras"
date:   2017-12-11
---

I would like to introduce the character theory of (commutative) coherent algebras, with the goal of arriving at what it means for a coherent algebra to be self-dual, starting with the prototypical example of a family of self-dual coherent algebras arising from finite abelian groups.

Suppose that $$\mathcal{W}$$ is a commutative coherent algebra (of order $$n$$ and dimension $$d$$).

Let $$\Gamma(\mathcal{W})$$ and $$\Lambda(\mathcal{W})$$ denote the set of Schur-primitive and primitive matrices in $$W$$ respectively:

*Note that a non-zero $$01$$-matrix $$M \in \mathcal{W}$$ is said to be Schur-primitive if $$M \circ N \in \operatorname{span} \{ M \}$$ for all $$N \in \mathcal {W}$$, and likewise a non-zero idempotent matrix $$M \in \mathcal{W}$$ is said to be primitive if $$MN \in \operatorname{span} \{ M \}$$ for all $$N \in \mathcal {W}$$.*

I would propose that $$\mathcal{W} := \operatorname{span} \left ( \Gamma(\mathcal{W}) \right ) = \operatorname{span} \left ( \Lambda(\mathcal{W}) \right )$$ .

1. Let $$\widehat{\Gamma(\mathcal{W})} := \{ M \in \mathcal{W} : M \circ N = 0 \text{ for all } N \in \operatorname{span} \left ( \Gamma(\mathcal{W}) \right )\}$$.
	
	Observe that $$\widehat{\Gamma(\mathcal{W})}$$ is a Schur-closed subspace of $$\mathcal{W}$$.

	It follows that for all $$M \in \widehat{\Gamma(\mathcal{W})}$$ with a non-zero entry $$c \in \mathbb{C}$$, the matrix 
	$$ N \circ N - N \in \widehat{\Gamma(\mathcal{W})}$$ where $$N := \frac{1}{c} M$$ has fewer non-zero entries than $$M$$.


	This then means that the matrix in $$\widehat{\Gamma(\mathcal{W})}$$ with the least number of non-zero entries must be a $$01$$-matrix,
	and moreover must either be Schur-primitive or the zero matrix.

	But, there are no Schur-primitive matrices in $$\widehat{\Gamma(\mathcal{W})}$$.

	$$ \implies \widehat{\Gamma(\mathcal{W})}$$

	It is then ultimately apparent that $$\mathcal{W} = \operatorname{span} \left ( \Lambda(\mathcal{W}) \right ) $$.


2. Let $$\sigma(A)$$ denote the set of distinct eigenvalues of $$A$$ for all $$A \in \Gamma(\mathcal{W})$$.

	Observe that $$\Gamma(\mathcal{W})$$ is a set of commuting normal matrices.

	$$\implies $$ There is a unitary matrix $$U \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ that simultaneously diagonalizes $$\Gamma(\mathcal{W})$$.

	Let $$S := \{ P_{j} : 1 \leq j \leq n \}$$ where $$P_{j} := \left ( U e_{j} \right ) \left ( U e_{j} \right )^{T} \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ for all $$ 1 \leq j \leq n$$.

	Now, observe too that the elements of $$S$$ are orthogonal projections, and $$PQ = 0$$ for all $$P, Q \in S$$ such that $$P \neq Q$$.

	Let $$\Omega(A) := \left \{ \sum\limits_{P \in T_{\lambda}} P : \lambda \in \sigma(A) \right \} $$ where $$T_{\lambda} := \{ P \in S : AP = \lambda P \} $$ for all $$\lambda \in \sigma(A)$$ and all $$A \in \Gamma(\mathcal{W})$$.

	It then follows that $$\Omega(A)$$ is a set of orthogonal projections onto the eigenspaces of $$A$$ for all $$A \in \Gamma(\mathcal{W})$$.

	Let $$\Omega(\mathcal{W})$$ denote the set of non-zero matrices in $$\operatorname{Mat}_{n \times n}(\mathbb{C})$$ of the form 

	$$\prod\limits_{A \in \Gamma(\mathcal{W})} M_{A}$$ for some $$ \{ M_{A} : A \in \Gamma(\mathcal{W}), M_{A} \in \Omega(A) \} \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$. 

	$$ \implies \mathcal{W} = \operatorname{span} \left ( \bigcup_{A \in \Gamma(\mathcal{W})} \Omega(A) \right ) \subseteq \operatorname{span} \left ( \Omega(\mathcal{W}) \right ) $$

	Lastly, recall that every normal matrix $$M \in \operatorname{Mat}_{n \times n}(\mathbb{C})$$ has a *unique* set $$\Omega(M)$$ consisting of orthogonal projections onto each of its eigenspaces, and that $$\Omega(M) \subseteq \{ f(M) : f(x) \in \mathbb{C}[x] \}$$ as well.

	$$ \implies \operatorname{span} \left ( \Omega(\mathcal{W}) \right ) \subseteq \mathcal{W} $$.


	It can then ultimately be observed that $$\Omega(\mathcal{W}) = \Lambda(\mathcal{W})$$, and hence $$\mathcal{W} = \operatorname{span} \left ( \Lambda(\mathcal{W}) \right )$$.


So $$\mathcal{W}$$ is indeed spanned by its set of Schur-primitive matrices, and dually, its set of primitive matrices as well.

Now, suppose that orderings $$\Gamma(\mathcal{W}) = \{ A_{j} : 1 \leq j \leq d \}$$ and $$\Lambda(\mathcal{W}) = \{ E_{j} : 1 \leq j \leq d \}$$ are given on the sets of Schur-primitive and primitive matrices in $$\mathcal{W}$$ respectively.

Then, since $$\mathcal{W} := \operatorname{span} \left ( \Gamma(\mathcal{W}) \right ) = \operatorname{span} \left ( \Lambda(\mathcal{W}) \right )$$, there is a matrix $$P_{\mathcal{W}} \in \operatorname{Mat}_{d \times d}(\mathbb{C})$$ such that $$A_{i} = \sum\limits_{j = 1}^{d} P_{i,j} E_j$$ for all $$1 \leq i,j \leq d$$, known as the character table of $$\mathcal{W}$$ (relative to this ordering).

$$\mathcal{W}$$ is said to be self-dual if $$P \overline{P} = n I$$.





 















