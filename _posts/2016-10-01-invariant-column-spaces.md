---
layout: post
title:  "Invariant Column Spaces"
date:   2016-10-01
---

In this post, my goal is to show that for any $$n$$ x $$n$$ matrix $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$n$$ x $$m$$ matrix $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$ with entries in a field $$\mathbb{F}$$, the column space of $$X$$ is $$A$$-invariant if and only if $$AX = XY$$ for some $$m$$ x $$m$$ matrix $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$.


Firstly, suppose that we are given matrices $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$ where the column space of $$X$$ is $$A$$-invariant. Then, for all $$1 \leq j \leq n$$, we can construct a vector $$y_j \in \mathbb{F}^{m}$$ such that:

$$A (X e_j) $$

$$= \sum\limits_{k = 1}^{m} a_{k,j} (X e_k)$$

**[** for some $$a_{k, j} \in \mathbb{F}$$ for all $$1 \leq k \leq n$$, since the column space of $$X$$ is $$A$$-invariant **]**

$$= X \left ( \sum\limits_{k = 1}^{m} a_{k,j} e_k \right ) $$

$$= X y_j$$

**[** by letting $$y_j = \sum\limits_{k = 1}^{m} a_{k,j} e_k$$ **]**

. From there, we can construct a matrix $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$ such that:

$$AX $$

$$= \left [ A (X e_1) \mid \cdots \mid A (X e_m) \right ] $$

$$= \left [ X y_1 \mid \cdots \mid X y_m \right ]$$

$$= XY$$

**[** by letting $$Y = \left [ y_1 \mid \cdots \mid y_m \right ]$$ **]**. Therefore, since our particular choices of $$A$$ and $$X$$ in this context are arbitrary, we have that: for any matrices $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$, if the column space of $$X$$ is $$A$$-invariant, then there exists a matrix $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$ such that $$AX = XY$$ as desired.
Secondly, suppose that we are given matrices $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$ where $$AX = XY$$ for some $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$. Then, for all $$1 \leq j \leq m$$, we have that:

$$A(X e_j) $$

$$= X (Y e_j) $$

$$= X \left( \sum\limits_{k=1}^{m} Y_{k, j} e_k \right )$$

$$= \sum\limits_{k=1}^{m} Y_{k, j} (X e_k)$$

. This means, in particular, that $$A (X e_j) \in \operatorname{Col}(X)$$ for all $$1 \leq j \leq m$$. 

Now, select any vector $$u \in \operatorname{Col}(X)$$; then we know that $$u = X v = \sum\limits_{j=1}^{m} v_j (X e_j)$$ for some vector $$v \in \mathbb{F}^{m}$$. From there, we can deduce that:

$$A u $$

$$= A \left ( \sum\limits_{j=1}^{m} v_j (X e_j) \right ) $$

$$= \sum\limits_{j=1}^{m} v_j (A (X e_j) ) $$

$$= \sum\limits_{j=1}^{m} v_j \left ( \sum\limits_{k=1}^{m} Y_{k, j} (X e_k) \right ) $$

$$= \sum\limits_{j=1}^{m} \sum\limits_{k=1}^{m} v_j Y_{k, j} (X e_k)$$

$$= \sum\limits_{k=1}^{m} \left ( \sum\limits_{j=1}^{m} v_j Y_{k, j} \right ) (X e_k)$$

. This means that $$A u \in \operatorname{Col}(X)$$, and hence that $$\operatorname{Col}(X)$$ is $$A$$-invariant, since our choice of $$u$$ in this inner context is arbitrary. Therefore, since our contextual choices of $$A$$ and $$X$$ are likewise arbitrary, we have that: for any matrices $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$, if $$AX = XY$$ for some $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$, then the column of space of $$X$$ is $$A$$-invariant as desired.
Hence we can conclude that for any $$n x n$$ matrix $$A \in \operatorname{Mat}_{n \times n}(\mathbb{F})$$ and $$n$$ x $$m$$ matrix $$X \in \operatorname{Mat}_{n \times m}(\mathbb{F})$$ with entries in a field $$\mathbb{F}$$, the column space of $$X$$ is $$A$$-invariant if and only if $$AX = XY$$ for some $$m$$ x $$m$$ matrix $$Y \in \operatorname{Mat}_{m \times m}(\mathbb{F})$$, as desired.
