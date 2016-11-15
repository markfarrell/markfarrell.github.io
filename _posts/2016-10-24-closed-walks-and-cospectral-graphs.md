---
layout: post
title:  "Closed Walks and Cospectral Graphs"
date:   2016-10-24
categories: jekyll update
---

In this post, my goal is to verify that a pair of simple graphs are cospectral if and only if their respective generating series for all closed walks weighted by length are equal.


Suppose that $$G$$ is a simple graph with adjacency matrix $$A$$. Then, first and foremost, I would like to give a couple of definitions in this context:

1. The generating series closed walks on $$G$$ weighted by length is given by $$W_{G}(X) := \sum\limits_{n=0}^{\infty} \operatorname{tr}(A^{n}) X^{n}$$ - assuming, for the purposes of this post, the fact that $$\operatorname{tr}(A^{n})$$ gives the total number of closed walks of length $$n$$ on $$G$$ for all $$n \geq 0$$. 

*Note that here $$W_{G}(X) \in \mathbb{R}[[X]]$$, i.e. it is an element of the algebra of formal power series with real coefficients.*

2. Suppose that the characteristic polynomial of the adjacency matrix of $$G$$ is given by $$\phi_{G}(x)$$. Additionally, suppose that $$H$$ is another simple graph where the characteristic polynomial of the adjacency matrix of $$H$$ is given by $$\phi_{H}(x)$$. Then $$G$$ and $$H$$ are said to be cospectral if $$\phi_{G}(x) = \phi_{H}(x)$$.

Now, in order to achieve my original goal for this post of verifying that a pair of simple graphs are cospectral if and only if their respective generating series for all closed walks weighted by length are equal, I would first like to necessarily propose that the following facts hold in this context:

1. Suppose that minimal polynomial of the adjacency matrix $$A$$ of $$G$$ is given by $$p(x) = \prod\limits_{k = 1}^{n} \left (x - \lambda_k \right )$$. Additionally, suppose that $$A$$ has the spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_\lambda$$, where $$\sigma(A)$$ is the set whose elements consist of all of the roots of $$p(x)$$. Then the generating series $$W_{G}(X)$$ for all closed walks on $$G$$ weighted by length admits the partial fraction decomposition $$W_{G}(X) = \sum\limits_{\lambda \in \sigma(A)} \frac{\operatorname{tr}(E_{\lambda})}{1 - \lambda X}$$.

2. If the adjacency matrix $$A$$ of $$G$$ has the spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_\lambda$$, where $$\sigma(A)$$ is the set whose elements consist of the distinct eigenvalues of $$A$$, then $$\operatorname{tr}(E_\lambda) = m_{\lambda}$$ gives the multiplicity $$m_{\lambda}$$ of $$\lambda$$ as an eigenvalue of $$A$$ for all $$\lambda \in \sigma(A)$$.


Assuming that these facts hold in this context, then it is possible to then further deduce that the generating series $$W_{G}(X)$$ for all closed walks on $$G$$ weighted by length admits a closed form as a rational expression involving the characteristic polynomial of the adjacency matrix $$A$$ of $$G$$ and its formal derivative relative to a certain formal symbol in context, which will be useful for achieving my original goal of verifying that a pair of simple graphs are cospectral if and only if their respective generating series for all closed walks weighted by length are equal:


1. Suppose that the closed walk generating series $$W_G(X)$$ of all closed walks on $$G$$ weighted by length admits the partial fraction decomposition $$W_{G}(X) = \sum\limits_{\lambda \in \sigma(A)} \frac{m_{\lambda}}{1 - \lambda X}$$, where $$\sigma(A)$$ is the set whose elements consist of distinct eigenvalues of $$A$$ and each $$m_{\lambda}$$ denotes the multiplicity of $$\lambda$$ as an eigenvalue of $$A$$ for all $$\lambda \in \sigma(A)$$. Additionally, suppose that the characteristic polynomial $$\phi(x)$$ of $$A$$ is given by $$\phi(x) = \prod\limits_{\lambda \in \sigma(A)} \left ( x - \lambda \right )^{m_{\lambda}}$$. Then, we can further deduce from here that:

 $$W_{G}(X) $$

$$= \sum\limits_{\lambda \in \sigma(A)} \frac{m_{\lambda}}{1 - \lambda X} $$

$$= \sum\limits_{\lambda \in \sigma(A)} \left ( \frac{X^{-1}}{X^{-1}} \right ) \frac{m_{\lambda}}{1 - \lambda X} $$

$$= \sum\limits_{\lambda \in \sigma(A)} \frac{m_{\lambda} X^{-1}}{X^{-1} - \lambda} $$

$$= X^{-1} \sum\limits_{\lambda \in \sigma(A)} \frac{m_{\lambda}}{X^{-1} - \lambda}$$

$$= X^{-1} \sum\limits_{\lambda \in \sigma(A)}  \left ( \frac{ \left ( \frac{\phi(X^{-1})}{X^{-1} - \lambda} \right )}{ \left ( \frac{\phi(X^{-1})}{X^{-1} - \lambda} \right )} \right ) \frac{m_{\lambda}}{X^{-1} - \lambda}  $$

$$= X^{-1} \sum\limits_{\lambda \in \sigma(A)} \frac{m_{\lambda} \left ( \frac{\phi(X^{-1})}{X^{-1} - \lambda} \right )}{\phi(X^{-1})}  $$

$$= \frac{X^{-1} \left ( \sum\limits_{\lambda \in \sigma(A)} m_{\lambda} \left ( \frac{\phi(X^{-1})}{X^{-1} - \lambda} \right ) \right )}{\phi(X^{-1})} $$

$$= \frac{X^{-1} \phi^{'}(X^{-1})}{\phi(X^{-1})}$$

.

*Note that here $$X^{-1}$$ denotes another formal symbol that happens to have the relation $$X^{-1}X = 1$$ with the formal symbol $$X$$ and should not be interpreted as a “function of $$X$$” in the sense of calculus when e.g. considering the formal derivative $$\phi^{'}(X^{-1})$$ of $$\phi(X^{-1})$$ with respect to the formal symbol $$X^{-1}$$ in context.*

I would now like to show that the previous two facts that I assumed to be true indeed hold in this context:

1. Consider the left-shift operator $$T : \mathbb{R}[[X]] \to \mathbb{R}[[X]]$$ acting on the algebra $$\mathbb{R}[[X]]$$ of formal power series with real coefficients, defined as $$T \left ( \sum\limits_{n = 0}^{\infty} a_n X^{n} \right ) := \sum\limits_{n = 0}^{\infty} a_{n + 1} X^{n}$$ for all $$\sum\limits_{n = 0}^{\infty} a_n X^{n} \in \mathbb{R}[[X]]$$; I would like to assume, for the purposes of this post, that this operator is indeed linear and that $$\mathbb{R}[[X]]$$ can be interpreted as a vector space. Then, core linear algebra tells us that given the minimal polynomial $$p(x) = \prod\limits_{k = 1}^{j} \left (x - \lambda_k \right )$$ of the adjacency matrix $$A$$ of $$G$$, $$\operatorname{null}(p(T))$$ admits the direct sum decomposition $$\operatorname{null}(p(T)) = \oplus_{k = 1}^{j} \operatorname{null}(T - \lambda_{k} I) = \oplus_{k = 1}^{j} \operatorname{span} \left \{ \frac{1}{1 - \lambda_k X} \right \}$$; I would also ask, for the purposes of this blog post, that you believe me that this fact from linear algebra is indeed true - and also the fact that a formal power series $$A(X) \in \mathbb{R}[[X]]$$ is an eigenvector for an eigenvalue $$\lambda$$ of $$T$$ if and only if $$A(X)$$ is a (non-zero) scalar multiple of $$\frac{1}{1 - \lambda X}$$. Now, from linearity properties of the trace map $$\operatorname{tr} : \operatorname{Mat}_{d \times d}(\mathbb{R}) \to \mathbb{R}$$ where $$d$$ denotes the number of vertices on $$G$$ in this context, we can deduce that $$W_G(X) \in \operatorname{null}(p(T)) = \oplus_{k = 1}^{j} \operatorname{span} \left \{ \frac{1}{1 - \lambda_k X} \right \}$$; hence we can deduce that $$W_G(X) = \sum\limits_{k = 1}^{j} \frac{c_k}{1 - \lambda_k X}$$ for some unique scalars $$c_k \in \mathbb{R}$$ for all $$1 \leq k \leq j$$. However, if we know that the adjacency matrix $$A$$ of $$G$$ has the spectral decomposition $$A = \sum\limits_{\lambda \in \sigma(A)} \lambda E_{\lambda}$$ where $$\sigma(A)$$ denotes the set of distinct eigenvalues of $$A$$, then it turns out that $$A^{n}$$ has the spectral decomposition $$A^{n} = \sum\limits_{\lambda \in \sigma(A)} \lambda^{n} E_{\lambda}$$ for all $$n \geq 0$$; and hence it turns out that $$\operatorname{tr}(A^{n}) = \sum\limits_{\lambda \in \sigma(A)} \lambda^{n} \operatorname{tr}(E_{\lambda})$$ for all $$n \geq 0$$ by linearity properties of trace. If we consider the fact that the $$n$$-th coefficient of $$W_G(X)$$ is given by $$\operatorname{tr}(A^{n}) = \sum\limits_{\lambda \in \sigma(A)} \lambda^{n} \operatorname{tr}(E_{\lambda}) = \sum\limits_{k=1}^{j} \lambda_{k}^{n} \operatorname{tr}(E_{\lambda_k})$$ and is also given by the $$0$$-th coefficient of $$T^{n} \left ( \sum\limits_{k = 1}^{j} \frac{c_k}{1 - \lambda_k X} \right )$$ which is equal to $$\sum\limits_{k = 1}^{j} \lambda_{k}^{n} c_k$$ for all $$n \geq 0$$, then we see that each $$c_k = \operatorname{tr}(E_{\lambda_k})$$ for all $$1 \leq k \leq j$$ since each $$c_k$$ is unique. Hence we ultimately get that $$W_G(X)$$ admits the partial fraction decomposition $$W_{G}(X) = \sum\limits_{\lambda \in \sigma(A)} \frac{\operatorname{tr}(E_{\lambda})}{1 - \lambda X}$$ as desired.

2. Consider the spectral idempotent $$E_\lambda$$ for an arbitrary $$\lambda \in \sigma(A)$$ where $$\sigma(A)$$ denotes the set of distinct eigenvalues of the adjacency matrix $$A$$ of $$G$$. Then, since $$E_{\lambda}^{2} = E_{\lambda}$$ we can see that $$E_{\lambda}^{2} - E_{\lambda} = 0$$ and hence that the minimal polynomial of $$p(x)$$ of $$E_{\lambda}$$ is given by $$p(x) = x(x - 1)$$; since $$p(x)$$ splits into distinct linear factors, this means that $$E_{\lambda}$$ is diagonalizable with $$1$$s and $$0$$s lying along the diagonal matrix that it is similar to. Since the rank of the diagonal matrix that $$E_{\lambda}$$ is similar to is equal to the rank of $$E_{\lambda}$$, and since the only non-zero entries in the diagonal matrix that $$E_{\lambda}$$ is similar to will be $$1$$s lying along said matrix’s diagonal, we can deduce that $$\operatorname{rank}(E_{\lambda}) = \operatorname{tr}(E_{\lambda})$$. Lastly, since $$\operatorname{rank}(E_{\lambda}) = \operatorname{dim}(\operatorname{null}(A - \lambda I))$$, and since the multiplicity $$m_\lambda$$ of $$\lambda$$ as a eigenvalue of the adjacency matrix $$A$$ of $$G$$ is given by $$m_\lambda = \operatorname{dim}(\operatorname{null}(A - \lambda I))$$, we get that $$m_\lambda = \operatorname{tr}(E_{\lambda})$$. Therefore we get that $$m_{\lambda^{'}} = \operatorname{tr}(E_{\lambda_{'}})$$ for all $$\lambda^{'} \in \sigma(A)$$, since our choice of $$\lambda$$ in this context is arbitrary.


Now, I would like to break out of this context here and conclude that in general the closed walk generating series admits a closed form as a rational expression in the sense that I’ve shown is true in this context, since $$G$$ in this context is arbitrary.
I would next like to move onward to achieving my original goal of verifying that a pair of simple graphs are cospectral if and only if their respective generating series for all closed walks weighted by length are equal:

1. Suppose that $$G$$ and $$H$$ are a pair of cospectral simple graphs, where the respective characteristic polynomials of the adjacency matrices of $$G$$ and $$H$$ are denoted by $$\phi_{G}(x)$$ and $$\phi_{H}(x)$$. Then, assuming that my previous result is true, we can see that the respective generating series $$W_{G}(X)$$ and $$W_{H}(X)$$ for all closed walks on $$G$$ and $$H$$ weighted by length admit closed forms as rational expressions given by $$W_{G}(X) = \frac{X^{-1} \phi_{G}^{'}(X^{-1})}{\phi_{G}(X^{-1})}$$ and $$W_{H}(X) = \frac{X^{-1} \phi_{H}^{'}(X^{-1})}{\phi_{H}(X^{-1})}$$. However, since $$G$$ and $$H$$ are cospectral, we know that in particular $$\phi_{G}(X^{-1}) = \phi_{H}(X^{-1})$$ and can further deduce that $$\phi_{G}^{'}(X^{-1}) = \phi_{H}^{'}(X^{-1})$$ as well. Hence, it is quite clear that $$W_{G}(X) = W_{H}(X)$$ in this context; therefore, if any pair simple graphs of are cospectral, then their respective generating series for all closed walks weighted by length must be equal, since $$G$$ and $$H$$ in this context are arbitrary.

2. Now, suppose that $$G$$ and $$H$$ are a pair of simple graphs whose respective generating series for all closed walks weighted by length are equal, i.e $$W_G(X) = W_H(X)$$. Then, assuming my previous result, we know that $$\frac{X^{-1} \phi_{G}^{'}(X^{-1})}{\phi_{G}(X^{-1})} = \frac{X^{-1} \phi_{H}^{'}(X^{-1})}{\phi_{H}(X^{-1})}$$ where $$\phi_{G}(x)$$ and $$\phi_{H}(x)$$ denote the respective characteristic polynomials of the adjacency matrices of $$G$$ and $$H$$. From this, we can ultimately deduce that $$\phi_{G}^{'}(X^{-1}) \phi_{H}(X^{-1}) = \phi_{G}(X^{-1})\phi_{H}^{'}(X^{-1})$$ and furthermore that $$\left ( \frac{\phi_{G}(X^{-1})}{\phi_{H}(X^{-1})} \right )^{'} = 0$$. Lastly, since characteristic polynomials are monic, we can then deduce that $$\frac{\phi_{G}(X^{-1})}{\phi_{H}(X^{-1})} = 1$$ from the fact that $$\left ( \frac{\phi_{G}(X^{-1})}{\phi_{H}(X^{-1})} \right )^{'} = 0$$. Hence we get that $$\phi_{G}(X^{-1}) = \phi_{H}(X^{-1})$$ and can see that $$\phi_{G}(x) = \phi_{H}(x)$$. Therefore, we can conclude that $$G$$ and $$H$$ are cospectral because their respective characteristic polynomials are equal; we can also more generally conclude that if the respective generating series for closed walks weighted by length of a pair of simple graphs are equal, then they must be cospectral, since $$G$$ and $$H$$ in this context are arbitrary.


Therefore, we can ultimately conclude from this post that a pair of simple graphs are cospectral if and only if their respective generating series for all closed walks weighted by length are equal, as desired.
