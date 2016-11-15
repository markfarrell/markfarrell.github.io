---
layout: post
title:  "Perfect State Transfer and Uniform Mixing on Complete Graphs"
date:   2016-09-28
categories: jekyll update
---

I would like to continue to talk about my investigations into what simple graphs admit the properties known as perfect state transfer and uniform mixing relative to their adjacency matrices. In this particular post, my goals are to:

1. Verify that the only complete graph that admits the property known as perfect state transfer is $$K_2$$.

2. Verify that the only complete graphs that admit the property known as uniform mixing are $$K_2$$, $$K_3$$, and $$K_4$$.


In order to show that the only complete graph that admits perfect state transfer is $$K_2$$, I would like to first assume that if a simple graph admits perfect state transfer between a pair of distinct vertices at a particular time, then said pair of distinct vertices must also satisfy the property known as being strongly cospectral. A pair of distinct vertices on a simple graph are said to be strongly cospectral if they are both cospectral and parallel. I’ve previously discussed a few characterizations and sufficient conditions for a pair of distinct vertices to be considered cospectral on a simple graph: for an initial discussion on what it means for a pair of distinct vertices on a simple graph to be cospectral, please see my past blog post (https://m4farrel.quora.com/Closed-Walks-and-Cospectral-Vertices) on the matter. On the other hand, I’ve yet to define what it means for a pair of distinct vertices to be parallel on a simple graph: a pair of distinct vertices $$u$$ and $$v$$ on a simple graph $$G$$ are said to be parallel if $$E_{\lambda}e_u$$ and $$E_{\lambda}e_v$$ are linearly dependent for all $$\lambda \in \sigma(A)$$, where $$\sigma(A)$$ denotes the set of distinct eigenvalues of the adjacency matrix $$A$$ of $$G$$. With those definitions in mind, I would like to proceed to show that unless $$n = 2$$, the complete graph $$K_n$$ does not have any strongly cospectral vertices; and hence show that unless $$n = 2$$, the complete graph $$K_n$$ does not admit perfect state transfer, since strong cospectrality is necessary condition for a simple graph to admit perfect state transfer between a pair of distinct vertices.


We also saw in one of my [previous blog posts](https://m4farrel.quora.com/Complete-Graphs-Are-Characterized-by-Their-Spectra) that the adjacency matrix $$A$$ of a complete graph $$K_n$$ on $$n$$ vertices has the spectral decomposition $$A = (n - 1)E_{n-1} - E_{-1}$$, where $$E_{n-1} = \frac{1}{n} J$$ and $$E_{-1} = I - \frac{1}{n} J$$. Since $$E_{n-1}$$ is a rank-one matrix, it is apparent that $$E_{n-1}e_u$$ and $$E_{n-1}e_v$$ are linearly dependent for any pair of distinct vertices $$u$$ and $$v$$ on $$K_n$$; so to check that a pair of distinct vertices $$u$$ and $$v$$ on $$K_n$$ are parallel, it suffices to check that $$E_{-1}e_u$$ and $$E_{-1}e_v$$ are linearly dependent. Assuming that the Cauchy-Schwartz inequality holds for the standard inner product and norm on $$\mathbb{R}^{n}$$, we can check whether or not equality holds for $$\mid \langle E_{-1}e_u, E_{-1}e_v \rangle \mid \leq \lVert E_{-1} e_u \rVert \lVert E_{-1}e_u \rVert$$ in order to decide whether or not $$E_{-1}e_u$$ and $$E_{-1}e_v$$ are linearly dependent for a pair of distinct vertices $$u$$ and $$v$$ on $$K_n$$. By inspection, it is apparent that this equality does not hold for any pair of vertices $$u$$ and $$v$$ on $$K_n$$ unless $$n = 2$$, in which case it holds for the only pair of distinct vertices on $$K_2$$; hence we already know the only complete graph that could potentially admit perfect state transfer is $$K_2$$, since any other complete graph does not have any parallel vertices, and hence does not have any strongly cospectral vertices either.


I would now like to verify that $$K_2$$ indeed admits perfect state transfer between its only pair of distinct vertices. For $$K_2$$, we know that its only pair of vertices are strongly cospectral because they are parallel, and are also cospectral because there is an automorphism on $$K_2$$ that sends one vertex to the other; so we have reason to believe that $$K_2$$ could potentially admit perfect state transfer between its only pair of distinct vertices. We can in fact verify that $$K_2$$ indeed admits perfect state transfer between its only pair of distinct vertices now using a direct approach. For the purposes of this particular blog post, I would like to assume another fact that if the spectral decomposition of the adjacency matrix $$A$$ of a simple graph $$G$$ is given by $$A = \sum_{\lambda \in \sigma(A)} \lambda E_{\lambda}$$, then the spectral decomposition of its continuous-time quantum walk relative to its adjacency matrix is given by $$U(t) = \sum_{\lambda \in \sigma(A)} \operatorname{exp}(it(\lambda)) E_{\lambda}$$. Then, the continuous-time quantum walk of $$K_2$$ relative to its adjacency matrix is given by:

$$U(t)$$

$$= \operatorname{exp}(itA) $$

$$= \operatorname{exp}(it)E_{1} + \operatorname{exp}(-it)E_{-1} $$

$$= \operatorname{exp}(it)J + \operatorname{exp}(-it)(I - J) $$

$$= (\operatorname{exp}(it) - \operatorname{exp}(-it)) J + \operatorname{exp}(-it)I $$

$$= (\operatorname{exp}(it) - \operatorname{exp}(-it)) (J - I) + (\operatorname{exp}(-it) + (\operatorname{exp}(it) - \operatorname{exp}(-it))) I $$

$$= (\operatorname{exp}(it) - \operatorname{exp}(-it)) A + \operatorname{exp}(it)I $$

$$= i (2 sin(t)) A + \operatorname{exp}(it)I$$

.

We can further see that if $$U(t)e_1 = \operatorname{exp}(i \theta) e_2$$ at some time $$t \in \mathbb{R}$$ and for some angle $$\theta \in [0, 2 \pi]$$, i.e. $$K_2$$ admits perfect state transfer between its only pair of distinct vertices at time $$t$$, then $$sin(t) = 0$$ and $$t = \theta$$. Hence we can deduce that $$K_2$$ indeed admits perfect state transfer between its only pair of distinct vertices at time $$t = \frac{\pi}{2}$$; moreover, together with the fact from the previous paragraph the $$K_n$$ does not have any strongly cospectral vertices unless $$n = 2$$, we can conclude that $$K_2$$ is the only complete graph that admits perfect state transfer.


I would now like to move on to verify that $$K_2$$, $$K_3$$ and $$K_4$$ are the only complete graphs that admit uniform mixing. Recalling the definition of what it means for a simple graph to admit uniform mixing relative to its adjacency matrix from one of [my previous posts](https://m4farrel.quora.com/Perfect-State-Transfer-and-Uniform-Mixing-on-Cartesian-Products-of-Graphs), We can deduce a general expression for the mixing matrix of the complete graph $$K_n$$ on $$n$$ vertices as follows:

$$M(t) $$

$$= U(t) \circ U^{*}(t)$$

$$= \left ( \operatorname{exp}(it(n-1)) E_{n-1} + \operatorname{exp}(-it) E_{-1} \right ) \circ \left ( \operatorname{exp}(it(-(n - 1))) E_{n-1} + \operatorname{exp}(it) E_{-1} \right ) $$

$$= E_{n-1} \circ E_{n-1} + \left ( \operatorname{exp}(it(n)) + \operatorname{exp}(it(-n)) \right ) E_{n-1} \circ E_{-1} + E_{-1} \circ E_{-1} $$

$$= \left ( \frac{1}{n} J \right ) \circ \left ( \frac{1}{n} J \right ) + 2 cos(nt) \left ( \frac{1}{n} J \right ) \circ \left ( I - \frac{1}{n} J \right ) + (I - \frac{1}{n} J) \circ (I - \frac{1}{n} J ) $$

$$= \frac{1}{n^{2}} J + \frac{2 cos(nt)}{n} (I - \frac{1}{n} J ) + \left ( (1 - \frac{2}{n}) I + \frac{1}{n^{2}} J \right ) $$

$$= \frac{2 - 2 cos (nt)}{n^{2}} J + \frac{n^{2} - 2n + (2n)cos(nt)}{n^2} I $$

$$= \frac{2 - 2 cos (nt)}{n^{2}}(J - I) + \frac{n^{2} - 2n + 2 + 2(n-1)cos(nt)}{n^2} I $$

$$= \frac{2 - 2 cos (nt)}{n^{2}} A + \frac{n^{2} - 2n + 2 + 2(n-1)cos(nt)}{n^2} I$$

.

From there, we can deduce that if the complete graph $$K_n$$ on $$n$$ vertices admits uniform mixing at some specific time $$t \in \mathbb{R}$$, i.e. $$M(t) = \frac{1}{n} J$$, then we must have that $$\frac{2 - 2 cos (nt)}{n} = \frac{n^{2} - 2n + 2 + 2(n-1)cos(nt)}{n}$$. Then, we can ultimately infer from this that we must have that $$cos(nt) = 1 - \frac{1}{2} n$$, assuming that the complete graph $$K_n$$ admits uniform mixing at time $$t$$. It is then apparent that unless $$n \leq 3$$, our original assumption cannot be true, since we know that $$-1 \leq cos(nt) \leq 1$$. Therefore, we can conclude that the only complete graphs that admit uniform mixing are $$K_2$$, $$K_3$$ and $$K_4$$, as desired.
Hence we have ultimately verified in this post that:

1. The only complete graph that admits the property known as perfect state transfer is $$K_2$$.

2. The only complete graphs that admit the property known as uniform mixing are $$K_2$$, $$K_3$$, and $$K_4$$.
as desired.
