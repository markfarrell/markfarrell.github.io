---
layout: post
title:  "Complete Graphs Are Characterized by Their Spectra"
date:   2016-09-23
categories: jekyll update
---

Having cospectral adjacency matrices is a necessary condition for simple graphs to be isomorphic. In general, however, it is not true that satisfying this condition alone is also sufficient for simple graphs to be isomorphic - but, for some families of simple graphs it is, and these families of simple graphs are particularly interesting to identify and study. In this particular post, my goal is to show that the complete graphs are an example of a family of simple graphs that are characterized by their spectra - which is to say that a simple graph $$G$$ on $$n$$ vertices is isomorphic to the complete graph $$K_n$$ on $$n$$ vertices if and only if they are cospectral relative to their adjacency matrices.

First and foremost, I would like to show how to deduce a general expression for the spectrum of a complete graph on any number vertices; so that we also know what the spectrum of another simple graph must be in order for it and a complete graph on the same number of vertices to be cospectral relative to their adjacency matrices. The adjacency matrix $$A$$ of the complete graph $$K_n$$ on $$n$$ vertices is given by $$A = J - I$$. From there, we can deduce that:
 
$$A^{2} $$

$$= (J - I)^{2} $$

$$= J^{2} - JI - IJ + I^{2} $$

$$= nJ - 2J + I $$

$$= (n - 2)J + I$$

$$= (n - 2)J - (n - 2)I + (n - 2)I + I $$

$$= (n - 2)(J - I) + (n - 1) I $$

$$= (n - 2)A + (n - 1)I$$

.

We can then see that the minimal polynomial of the complete graph $$K_n$$ on $$n$$ vertices is given by $$p(x) = (x - (n - 1))(x + 1)$$, since $$A^{2} - (n - 2)A - (n - 1)I = (A - (n - 1)I)(A + I) = 0$$. Additionally, we have that the spectral decomposition of $$A$$ is given by $$A = (n - 1)E_{n-1} - E_{-1}$$ where, in particular, $$E_{n - 1} = \frac{1}{(n - 1) + 1} (A + I) = \frac{1}{n} J$$; hence we can further deduce that $$n - 1$$ must have a multiplicity of one as an eigenvalue of $$A$$, and consequently that $$-1$$ must have a multiplicity of $$n - 1$$ as an eigenvalue of $$A$$, since their multiplicities must sum to $$n$$. Therefore, we can ultimately say that characteristic polynomial of the complete graph $$K_n$$ on $$n$$ vertices relative to its adjacency matrix is given by $$\phi(x) = (x - (n - 1))(x + 1)^{(n-1)}$$, and hence have deduced the spectrum of an arbitrary complete graph relative to its adjacency matrix as desired.

Now, I would like to use this general expression for the spectrum of a complete graph on any number of vertices to show that if a simple graph $$G$$ and the complete graph on the same number of vertices are cospectral relative to their adjacency matrices, then they must be isomorphic. Suppose that $$G$$ is an arbitrary simple graph on $$n$$ vertices whose characteristic polynomial is given by $$\phi(x) = (x - (n - 1))(x + 1)^{(n-1)}$$, relative to its adjacency matrix $$A$$. Then we know that the minimal polynomial of $$A$$ splits into distinct linear factors, and is given by $$p(x) = (x - (n - 1))(x + 1)$$; hence we can deduce that $$A$$ has the spectral decomposition $$A = (n - 1)E_{n - 1} - E_{-1}$$. Furthermore, we know that $$E_{n - 1} + E_{-1} = I$$ and hence $$E_{-1} = I - E_{n-1}$$; this tells us that $$A = nE_{n-1} - I$$. Additionally, we can see that $$\operatorname{rank}(E_{n - 1}) = 1$$, since from $$\phi(x)$$ we can see that $$n - 1$$ has a multiplicity of one as an eigenvalue of $$A$$. We also must have that $$A_{k,k} = (nE_{n-1} - I)_{k,k} = 0$$ and hence that $$(n E_{n - 1})_{k,k} = 1$$, for all $$1 \leq k \leq n$$; together with the fact that $$\operatorname{rank}(E_{n - 1}) = 1$$, we can ultimately conclude that $$nE_{n-1} = J$$ and hence that $$E_{n-1} = \frac{1}{n} J$$. Therefore, we have that $$A = (n - 1)E_{n-1} - E_{-1} = (n - 1)E_{n-1} - (I - E_{n-1}) = (n - 1)(\frac{1}{n} J) - (I - \frac{1}{n} J) = J - I$$, and hence that $$G$$ must ultimately be isomorphic to the complete graph $$K_n$$ on $$n$$ vertices as desired.

We know that it is always true that isomorphic simple graphs are cospectral relative to their adjacency matrices; we have shown that the converse is also true when restricted to simple graphs and complete graphs that are cospectral relative to their adjacency matrices. Hence we can ultimately conclude that a simple graph is isomorphic to a complete graph on the same number of vertices if and only if they are cospectral relative to their adjacency matrices, as desired.
