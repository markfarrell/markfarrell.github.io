---
layout: post
title:  "Spectral Decompositions of Continuous-Time Quantum Walks"
date:   2016-09-28 01:00
---

In my previous post, I assumed the fact that if the adjacency matrix $$A$$ of a simple graph $$G$$ has the spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_{\lambda}$$, then the continuous-time quantum walk $$U(t)$$ of $$G$$ relative to its adjacency matrix has the spectral decomposition $$U(t) = \sum\limits_{\lambda \in \sigma(A)} \operatorname{exp}(it(\lambda)) E_{\lambda}$$; here $$\sigma(A)$$ denotes the set of distinct eigenvalues of $$A$$. I would now like to verify that this fact is indeed true:


Suppose that $$G$$ is an arbitrary simple graph whose adjacency matrix $$A$$ has the spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_{\lambda}$$. Then, like in my previous blog posts, the continuous-time quantum walk of $$G$$ relative to is adjacency matrix is given by $$U(t) = \operatorname{exp}(itA) = \sum\limits_{n = 0}^{\infty} \frac{(itA)^{n}}{n!}$$. From there, we can deduce that:


$$U(t) $$

$$= \operatorname{exp}(itA) $$

$$= \operatorname{exp} \left ( it \left ( \sum\limits_{\lambda \in \sigma(A)} \lambda E_{\lambda} \right ) \right ) $$

$$= \prod\limits_{\lambda \in \sigma(A)} \operatorname{exp}(it(\lambda)E_{\lambda})$$

**[** by properties of matrix exponentials for matrices that commute **]**

$$= \sum\limits_{\lambda \in \sigma(A)} \operatorname{exp}(it(\lambda)E_{\lambda})$$

**[** since $$E_{\lambda}E_{\lambda'} = 0$$ unless $$\lambda = \lambda'$$ for all $$\lambda, \lambda' \in \sigma(A)$$ **]**

$$= \sum\limits_{\lambda \in \sigma(A)} \sum\limits_{n=0}^{\infty} \frac{(it(\lambda)E_{\lambda})^{n}}{n!} $$

$$= \sum\limits_{\lambda \in \sigma(A)} \sum\limits_{n=0}^{\infty} \frac{(it(\lambda))^{n}}{n!} E_{\lambda}^{n} $$

$$= \sum\limits_{\lambda \in \sigma(A)} \sum\limits_{n=0}^{\infty} \frac{(it(\lambda))^{n}}{n!} E_{\lambda}$$

**[** since each $$E_{\lambda}$$ is idempotent for all $$\lambda \in \sigma(A)$$ **]**

$$= \sum\limits_{\lambda \in \sigma(A)} \left ( \sum\limits_{n=0}^{\infty} \frac{(it(\lambda))^{n}}{n!} \right ) E_{\lambda} $$

$$= \sum\limits_{\lambda \in \sigma(A)} \operatorname{exp}(it(\lambda)) E_{\lambda}$$

.

Hence the continuous-time quantum walk $$U(t)$$ of $$G$$ has its spectral decomposition as desired; and therefore, the continuous-time quantum walk relative to the adjacency matrix of any simple graph has its spectral decomposition as desired, since $$G$$ is an arbitrary simple graph in this context.
