---
layout: post
title:  "Distinct Eigenvalues and Walk-Regular Graphs"
date:   2016-12-27
---

In this post, my goals are to verify that:

1. Every regular graph with at most four distinct eigenvalues is walk-regular.
2. Every regular triangle-free graph with at most five distinct eigenvalues is walk-regular.
3. Every regular bipartite graph with at most six distinct eigenvalues is walk-regular.

Firstly, suppose that $$G$$ is an arbitrary $$k$$-regular graph on $$n$$ vertices with adjacency matrix $$A$$, and moreover suppose that $$A$$ has exactly four distinct eigenvalues. 
Let the set of distinct eigenvalues of $$A$$ be then denoted by $$\sigma(A) = \{ k, \alpha, \beta, \gamma \}$$, assuming for the purposes of this blog post the fact a $$k$$-regular graph always has $$k$$ as one of its distinct eigenvalues. It is then possible to deduce that:

$$ Z(A) $$ 

$$ = \operatorname{span} \{ I, A, A^{2}, \cdots \} $$

$$ = \operatorname{span} \{ I, A, A^{2}, A^{3} \} $$

**[** since $$A$$ has four distinct eigenvalues, which means here that the minimal polynomial of $$A$$ is a monic polynomial of degree 4 and hence $$A^j$$ can be expressed as linear combination of $$I, A, A^{2}$$ and $$A^{3}$$ for all $$ j \geq 4$$ **]**

$$ = \operatorname{span} \{ E_{k}, E_{\alpha}, E_{\beta}, E_{\gamma} \} $$

**[** letting $$E_{k}, E_{\alpha}, E_{\beta}$$, and $$E_{\gamma}$$ denote the spectral idempotents of $$A$$, and assuming the fact that the span of the set of all powers of the adjacency matrix of a simple graph is equal to the span of its set of spectral idempotents **]**

$$ = \operatorname{span} \{ J, E_{\alpha}, E_{\beta}, E_{\gamma} \} $$

**[** assuming the fact that a vector $$v \in \mathbb{R}^{n}$$ is an eigenvector for eigenvalue $$k$$ of a $$k$$-regular graph on $$n$$ vertices if and only if $$v_k = c$$ for all $$ 1 \leq k \leq n$$ and some constant $$c \in \mathbb{R}$$ **]**. This means, in particular, that:

$$ J = a_3 A^{3} + a_2 A^{2} + a_1 A + a_0 I$$ 

**[** for some $$a_3, a_2, a_1, a_0 \in \mathbb{R} $$ **]**

$$ \implies A^{3} = \frac{1}{a_3} \left ( J - a_2 A^{2} - a_1 A - a_0 I \right ) $$

. 

It ultimately follows from this that $$A^{3}$$ has a constant diagonal, i.e. $$(A^{3})_{k,k} = c$$, assuming that $$J, A^{2}, A$$, and $$I$$ all have constant diagonals as well; aside from the fact that $$J, A$$, and $$I$$ all have constant diagonals by construction here, $$A^{2}$$ has a constant diagonal because $$G$$ is $$k$$-regular and so each diagonal entry of $$A^{2}$$ counts the $$k$$ number of closed walks between each respective vertex of $$G$$. Since $$A^{j}$$ can be written as a linear combination of $$A^{3}, A^{2}, A$$ and $$I$$ for all $$j \geq 4$$, we have that $$A^{j}$$ has a constant diagonal for all $$j \geq 4$$ as well. This means here that all of the vertices of $$G$$ are cospectral, since it follows from this that the relative generating series for closed walks weighted by length for each of the respective vertices of $$G$$ are all equal to each other. Hence $$G$$ is then walk-regular since all of its vertices are cospectral, and therefore every regular with four distinct eigenvalues is walk-regular since $$G$$ in this context is arbitrary. Additionally, it follows that every regular graph with at most three distinct eigenvalues is walk-regular from the fact that $$I, A, $$ and $$A^2$$ all have constant diagonals for any regular graph whose adjacency matrix is denoted by $$A$$, and moreover from the fact that this ultimately means that the vertices of every regular graph with at most three distinct eigenvalues are all cospectral by similar reasoning as before. Therefore we finally have that every regular graph with at most four distinct eigenvalues is walk-regular as desired.

Secondly, suppose that $$G$$ is an arbitrary $$k$$-regular triangle-free graph with adjacency matrix $$A$$, and moreover suppose that $$A$$ has exactly five distinct eigenvalues. By using the same assumptions as in the last paragraph, letting $$\sigma(A) = \{ k, \alpha, \beta, \gamma, \delta \}$$ denote the set of distinct eigenvalues of $$A$$, and letting $$\{ E_{k}, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta} \}$$ denote the set of spectral idempotents of $$A$$, it is then possible to similarly deduce that:

$$ Z(A) $$

$$ = \operatorname{span} \{ I, A, A^{2}, \cdots \} $$

$$ = \operatorname{span} \{ I, A, A^{2}, A^{3}, A^{4} \} $$

$$ = \operatorname{span} \{ E_{k}, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta} \} $$

$$ = \operatorname{span} \{ J, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta} \} $$

$$ \implies J = a_4 A^{4} + a_3 A^{3} + a_2 A^{2} + a_1 A + a_0 I $$

**\[** for some $$a_4, a_3, a_2, a_1, a_0 \in \mathbb{R}$$ **\]**

$$ \implies A^{4} = \frac{1}{a_4} \left ( J - a_3 A^{3} - a_2 A^{2} - a_1 A - a_0 I \right ) $$ 

.

This means that $$A^{4}$$ here has a constant diagonal, assuming that $$J, A^{3}, A^{2}, A$$ and $$I$$ all have constant diagonals; in addition to the fact that $$J, A^{2}, A,$$ and $$I$$ all have constant diagonals for similar reasons as in the last paragraph, $$A^{3}$$ has constant diagonal here because $$G$$ is a triangle-free graph and hence has no closed walks of length three between any of its vertices and themselves. Since $$A^{j}$$ can be written as a linear combination of $$A^{4}, A^{3}, A^{2}, A$$ and $$I$$ for all $$j \geq 5$$, we have that $$A^{j}$$ has a constant diagonal for all $$j \geq 5$$ as well. This then ultimately means that $$G$$ is walk-regular, for similar reasons as in the last paragraph as well; hence every regular triangle-free graph with five distinct eigenvalues is walk-regular, since $$G$$ in this context is arbitrary. Therefore every regular triangle-free graph with at most five distinct eigenvalues is walk-regular, since a regular triangle-free graph with less than five distinct eigenvalues can be interpreted as a regular graph with at most four distinct eigenvalues and from the last paragraph every regular graph with at most four distinct eigenvalues is walk-regular.

Lastly, suppose that $$G$$ is an arbitrary $$k$$-regular bipartite graph with adjacency matrix $$A$$, and moreover suppose that $$A$$ has exactly six distinct eigenvalues. By using the same assumptions as the last two paragraphs, letting the set of distinct eigenvalues of $$A$$ be then denoted by $$\sigma(A) = \{ k, \alpha, \beta, \gamma, \delta, \epsilon \}$$ the set of distinct eigenvalues of $$A$$, and letting $$\{ E_{k}, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta}, E_{\epsilon} \}$$ denote the set of spectral idempotents of $$A$$, it is then possible to again similarly deduce that:

$$ Z(A) $$

$$ = \operatorname{span} \{ I, A, A^{2}, \cdots \} $$

$$ = \operatorname{span} \{ I, A, A^{2}, A^{3}, A^{4}, A^{5} \} $$

$$ = \operatorname{span} \{ E_{k}, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta}, E_{\epsilon} \} $$

$$ = \operatorname{span} \{ J, E_{\alpha}, E_{\beta}, E_{\gamma}, E_{\delta}, E_{\epsilon} \} $$

$$ \implies J = a_5 A^{5} + a_4 A^{4} + a_3 A^{3} + a_2 A^{2} + a_1 A + a_0 I $$

**\[** for some $$a_5, a_4, a_3, a_2, a_1, a_0 \in \mathbb{R}$$ **\]**

$$ \implies A^{4} = \frac{1}{a_4} \left ( J - a_5 A^{5} - a_3 A^{3} - a_2 A^{2} - a_1 A - a_0 I \right ) $$ 

.

This means that $$A^{4}$$ here has a constant diagonal, assuming that $$J, A^{5}, A^{3}, A^{2}, A$$ and $$I$$ all have constant diagonals; in addition to the fact that $$J, A^{2}, A,$$ and $$I$$ all have constant diagonals for similar reasons as in the last two paragraphs, $$A^{3}$$ and $$A^{5}$$ both have constant diagonals here because $$G$$ is a bipartite graph and hence has no closed walks of odd length between any of its vertices and themselves. $$A^{j}$$ can be written as a linear combination of $$A^{5}, A^{4}, A^{3}, A^{2}, A$$ and $$I$$ for all $$j \geq 6$$, we have that $$A^{j}$$ has a constant diagonal for all $$j \geq 6$$ as well. This then ultimately means that $$G$$ is walk-regular, for similar reasons as in the last two paragraphs; hence every regular bipartite graph with six distinct eigenvalues is walk-regular, since $$G$$ in this context is arbitrary. Therefore every regular bipartite graph with at most five distinct eigenvalues is walk-regular, since a regular bipartite graph with five distinct eigenvalues is just a regular triangle-free graph with five distinct eigenvalues and a regular bipartite graph with at most four distince distinct eigenvalues is just a regular graph with at most four distinct eigenvalues.

I have verified the desired results about families of walk-regular graphs that exist due to the number of distinct eigenvalues that they have and hence have achieved my goals for this post. In particular, I think it is worth mentioning that the results presented here in this post subsume a result that I originally verified in one my [previous blog posts]({% post_url 2016-08-20-strongly-regular-graphs-are-walk-regular %}) about the fact that strongly regular graphs, and more generally regular graphs with three distinct eigenvalues, are walk-regular. More generally, I think it would be interesting to decide whether more families of walk-regular graphs exist due to the number of distinct eigenvalues that they have exist, identify what these families of walk-regular graphs might be if more do exist, and find more general results that e.g. again similarly subsume the results in the current blog post presented here. As one last closing remark, it may be worth mentioning that the first example of a cubic walk-regular graph that is neither vertex-transitive nor distance-regular that I found is a bipartite graph with six distinct eigenvalues - could it be possible to e.g. identity other families of walk-regular graphs that e.g. cubic walk-regular graphs that are neither vertex-transitive nor distance-regular must necessarily otherwise belong to based on e.g. properties of their spectra, should more examples exist?