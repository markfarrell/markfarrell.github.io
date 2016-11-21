---
layout: post
title:  "Perfect State Transfer and Uniform Mixing on Cartesian Products of Graphs"
date:   2016-09-18
---

In this post, my goals are to:
1. Verify that Cartesian products of simple graphs that admit the property known as perfect state transfer at the same time also admit perfect state transfer at the same time.
2. Verify that Cartesian products of simple graphs that admit the property known as uniform mixing at the same time also admit uniform mixing at the same time, assuming that the simple graphs in context have the same number of vertices.
First and foremost, I would like to define what it means for a simple graph to admit the properties known as perfect state transfer and uniform mixing. Suppose that $$G$$ is a simple graph on $$n$$ with adjacency matrix $$A$$.

Then, in this context:


1. The continuous-time quantum walk $$U : \mathbb{R} \to \operatorname{Mat}_{n \times n}(\mathbb{C})$$ of $$G$$ relative to its adjacency matrix is defined as $$U(t) := \operatorname{exp}(itA) = \sum\limits_{n = 0}^{\infty} \frac{ \left(itA \right)^{n}}{n!}$$.
2. Suppose $$u$$ and $$v$$ are a pair of distinct vertices on $$G$$. If $$U(t) e_u = \operatorname{exp}(i\theta) e_v$$ for some particular time $$t \in \mathbb{R}$$ and angle $$\theta \in [0, 2 \pi]$$, then $$G$$ is said to admit perfect state transfer (between $$u$$ and $$v$$, at time $$t$$).
3. The mixing matrix $$M : \mathbb{R} \to \operatorname{Mat}_{n \times n}(\mathbb{R})$$ of $$G$$ relative to its adjacency matrix is defined as $$M(t) := U(t) \circ U^{*}(t)$$, i.e. the entry-wise product of $$U(t)$$ and its conjugate transpose.
4. If $$M(t) = \frac{1}{n} J$$ at some particular time $$t \in \mathbb{R}$$, then $$G$$ is said to admit uniform mixing (at time $$t$$).

*Note that here $$J$$ denotes the $$n$$ x $$n$$ matrix consisting of all ones as entries.*

Secondly, I would like to verify that the following proposition is true:
1. For all simple graphs $$G$$ and $$H$$ whose continuous-time quantum walks are given by $$U_G (t)$$ and $$U_H (t)$$, the continuous-time quantum walk of their Cartesian product $$G \Box H$$ is given by $$U_{G \Box H} (t) = U_G (t) \bigotimes U_H (t)$$.
Assuming that this proposition is true, then:
2. Suppose that $$G$$ and $$H$$ are arbitrary simple graphs such that $$G$$ admits perfect state transfer between vertices $$u$$ and $$v$$ at time $$t$$, and $$H$$ admits perfect state transfer between vertices $$u'$$ and $$v'$$ at time $$t$$. By properties of the Kronecker product and the assumption that my previous proposition is true, we have that:


$$U_{G \Box H} \left ( e_{u} \bigotimes e_{u'} \right )   $$

$$= \left ( U_G (t) \bigotimes U_H (t) \right ) \left ( e_{u} \bigotimes e_{u'} \right )   $$

$$= \left ( U_{G}(t) e_{u} \right ) \bigotimes  \left ( U_H (t)  e_{u'} \right )   $$

$$= \left ( \operatorname{exp}(i \theta_{1}) e_{v} \right ) \bigotimes \left ( \operatorname{exp}(i \theta_{2}) e_{v'} \right )   $$

$$= \operatorname{exp}(i( \theta_{1} + \theta_{2})) e_{v} \bigotimes e_{v'}$$ 

for some angles $$\theta_{1}, \theta_{2} \in [0, 2 \pi ]$$.

Hence $$G \Box H$$ admits perfect state transfer at time $$t$$ as well; and therefore Cartesian products of simple graphs that admit perfect state transfer at the same time also admit perfect state transfer at the same time, since the choice of time and simple graphs in this context are arbitrary.
2. Similarly, suppose that $$G$$ and $$H$$ are arbitrary simple graphs on $$n$$ vertices that both admit uniform mixing at time $$t$$. By properties of the Kronecker product, its compatibility with the entry-wise product for matrices of the same dimensions, and the assumption that my previous proposition is true, we have that:

$$M_{G\Box H}(t)       $$

$$= U_{G \Box H}(t) \circ U_{G \Box H}^{*}(t)   $$

$$= \left ( U_G (t) \bigotimes U_H (t) \right ) \circ \left ( U_G (t) \bigotimes U_H (t) \right )^{*}   $$

$$= \left ( U_G (t) \bigotimes U_H (t) \right ) \circ \left ( U_{G}^{*}(t) \bigotimes U_{H}^{*}(t) \right )   $$

$$= \left ( U_G (t) \circ U_{G}^{*}(t) \right ) \bigotimes \left ( U_H (t) \circ U_{H}^{*}(t) \right )   $$

$$= M_{G}(t) \bigotimes M_{G}^{*}(t)   $$

$$= \left ( \frac{1}{n} J \right ) \bigotimes \left ( \frac{1}{n} J \right )   $$

$$= \frac{1}{n^{2}} J$$

. 

Hence $$G \Box H$$ admits uniform mixing at time $$t$$ as well; and therefore Cartesian products of simple graphs on the same number of vertices that admit uniform at the same time also admit uniform mixing at the same time, since the choice of time and simple graphs on the same number of vertices in this context are arbitrary.
I would now like to show that my previous proposition is indeed true.
1. Suppose that $$G$$ and $$H$$ are arbitrary simple graphs on $$m$$ and $$n$$ vertices. Then by properties of matrix exponentials, properties of the Kronecker product, and an assumed identity about the adjacency matrices of the Cartesian products of simple graphs, we have that:

$$U_{G \Box H}(t)      $$

$$= \operatorname{exp}(it A_{G \Box H})      $$

$$= \operatorname{exp} \left ( it \left(A_{G} \bigotimes I_n + I_m \bigotimes A_{H} \right ) \right )      $$

$$= \operatorname{exp} \left ( (it A_{G}) \bigotimes I_n + I_m \bigotimes (it A_{H}) \right )      $$

$$= \operatorname{exp} \left ( (it A_{G}) \bigotimes I_n \right ) \operatorname{exp} \left ( I_m \bigotimes (it A_{H}) \right )     $$

$$= \left ( \sum\limits_{n = 0}^{\infty} \frac{\left ( (it A_{G}) \bigotimes I_n \right )^{n}}{n!} \right ) \left ( \sum\limits_{n = 0}^{\infty} \frac{\left ( I_m \bigotimes (it A_{H}) \right )^{n}}{n!} \right )      $$

$$= \left ( \sum\limits_{n = 0}^{\infty} \frac{\left ( it A_{G} \right )^{n}}{n!} \bigotimes I_n \right ) \left ( \sum\limits_{n = 0}^{\infty} I_m \bigotimes \frac{\left ( it A_{H} \right )^{n}}{n!} \right )      $$

$$= \left ( \operatorname{exp}(it A_{G}) \bigotimes I_n \right ) \left ( I_m \bigotimes \operatorname{exp}(it A_{H}) \right )      $$

$$= \left ( \operatorname{exp}(it A_{G}) I_m \right ) \bigotimes  \left ( I_n \operatorname{exp}(it A_{H}) \right )      $$

$$= \operatorname{exp}(it A_{G}) \bigotimes \operatorname{exp}(it A_{H})      $$

$$= U_{G} (t) \bigotimes U_{H} (t)$$

as desired.

*Note that here $$A_{G \Box H}$$, $$A_G$$ and $$A_H$$ denote the respective adjacency matrices of $$G \Box H$$, $$G$$ and $$H$$; likewise $$U_{G \Box H}(t)$$, $$U_G (t)$$ and $$U_H (t)$$ denote their respective continuous-time quantum walks relative to their adjacency matrices.*

After showing that my previous proposition is true, we ultimately have that:
1. Cartesian products of simple graphs that admit the property known as perfect state transfer at the same time also admit perfect state transfer at the same time.
2. Cartesian products of simple graphs that admit uniform mixing at the same time also admit uniform mixing at the same time, assuming that the simple graphs in context have the same number of vertices.
as desired.
