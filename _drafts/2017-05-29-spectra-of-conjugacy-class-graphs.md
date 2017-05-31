---
layout: post
title:  "Spectra of Conjugacy Class Graphs"
date:   2017-05-29
---

Previously, I established that the set of conjugacy class diagraphs of a finite group gives rise to a (commutative) association scheme. It consequently follows that the adjacency matrix of a conjugacy class digraph of a finite group is normal and hence is diagonalizable. I would now like to verify how to derive a general expression for the spectrum of a conjugacy class digraph of a finite group.

Suppose that $$G$$ is a finite a group. Let $$e_{G}$$ denote the identity element of $$G$$, $$\operatorname{Cl}(G)$$ denote the set of conjugacy classes of $$G$$, $$\mathbb{C}[G]$$ denote the space of all total functions from $$G$$ to $$\mathbb{C}$$, $$X(G) \subset \mathbb{C}[G]$$ denote the set of irreducible characters of $$G$$ into $$\mathbb{C}$$, $$\{ \delta_{g} : g \in G \} $$ denote the standard basis for $$\mathbb{C}[G]$$, $$\operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote the space of $$\lvert G \rvert \times \lvert G \rvert$$ complex matrices whose rows and columns are indexed by the elements of $$G$$ relative to a certain ordering of them, and $$\{ A_{C} : C \in \operatorname{Cl}(G) \} \subset \operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote a set of adjacency matrices for the set of conjugacy class digraphs of $$G$$. Define:

* $$ \left ( M_{f} \right ) \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$

  $$ \left ( M_{f} \right )_{x,y} := f(x^{-1} y) $$

  for all $$ f \in \mathbb{C}[G] $$.

* $$ \left ( \star \right ) : \mathbb{C}[G] \times \mathbb{C}[G] \to \mathbb{C}[G] $$

  $$ \left ( f \star g \right )(x) := \sum\limits_{y \in G} f(y) g(y^{-1} x) $$

  turning $$ \mathbb{C}[G] $$ into the group ring of $$G$$ over $$\mathbb{C}$$.
   
Next, for all $$C \in \operatorname{Cl}(G)$$ and all irreducible representations $$F \in \operatorname{Hom} \left (G, \operatorname{Aut}(\mathbb{C}[G] ) \right )$$:

* Interpret the group ring $$\mathbb{C}[G]$$ as a module over itself, defining the scalar multiplication operation $$ (\ast) : \mathbb{C}[G] \times \mathbb{C}[G] \to \mathbb{C}[G] $$ as $$ \left ( \delta_{g} \ast f \right ) := F(g) \circ f $$ for all $$g \in G$$.

  Assume the facts that:

    1. $$ \sum\limits_{c \in C} F(c)  \in \operatorname{End}_{\ast}( \mathbb{C}[G]) $$
       
       **[** letting $$\operatorname{End}_{\ast}( \mathbb{C}[G])$$ denote the space of module endomorphisms from $$\mathbb{C}[G]$$ to itself **]**.
    2. $$ \operatorname{End}_{\ast}( \mathbb{C}[G]) \subset \{ \lambda I : \lambda \in \mathbb{C} \} $$
       
       **[** which is to say that Schur's lemma is true in this context **]**.


It is then possible to deduce that for all $$C \in \operatorname{Cl}(G)$$ and all irreducible characters $$\chi \in X(G)$$

there is a $$\lambda_{\chi}(C) \in \mathbb{C}$$ such that for all $$x,y \in G$$:

  $$ \left ( A_{C} \ M_{\chi} \right )_{x,y} $$
  
  $$ = \sum\limits_{z \in G, \ xz^{-1} \in C} \chi(z^{-1}y) $$
  
  $$ = \sum\limits_{c \in C} \chi(x^{-1} c y) $$

  $$ = \sum\limits_{c \in C} \chi \left ( x (x^{-1} c y )x^{-1} \right ) $$

  $$ = \sum\limits_{c \in C} \chi \left ( c y x^{-1} \right ) $$

  $$ = \sum\limits_{c \in C} \chi \left ( c y x^{-1} \right ) $$

  $$ = \sum\limits_{c \in C} \operatorname{tr} \left ( F \left ( c y x^{-1} \right ) \right ) $$

  **[** for some irreducible representation $$F \in \operatorname{Hom} \left (G, \operatorname{Aut}(\mathbb{C}[G] ) \right )$$, assuming the fact that such an irreducible representation exists **]**

  $$ = \sum\limits_{c \in C} \operatorname{tr} \left ( F \left ( c \right ) F \left ( y x^{-1} \right ) \right ) $$

  **[** since $$F$$ is a group homomorphism **]**

  $$ = \sum\limits_{c \in C} \operatorname{tr} \left ( F \left ( c \right ) F \left ( y x^{-1} \right ) \right ) $$

  $$ = \operatorname{tr} \left ( \left ( \sum\limits_{c \in C}  F \left ( c \right ) \right ) F \left ( y x^{-1} \right ) \right ) $$

  **[** by linearity of trace **]**

  $$ = \operatorname{tr} \left ( \left ( \overline { \lambda_{\chi}(C) } I \right ) \ F \left ( y x^{-1} \right ) \right ) $$

  **[** by previous set of assumptions **]**

  $$ = \overline { \lambda_{\chi}(C) } \ \operatorname{tr} \left ( F \left ( y x^{-1} \right ) \right ) $$

  **[** again, by linearity of trace **]**

  $$ = \overline { \lambda_{\chi}(C) } \ \chi \left ( y x^{-1} \right ) $$

  $$ = \overline { \lambda_{\chi}(C)  \  \chi \left (  x^{-1} y \right ) } $$

  **[** assuming the fact that $$\chi \left ( g^{-1} \right ) = \overline { \chi \left ( g \right )} $$ for all $$ g \in G $$ **]**

  $$ = \overline{ \lambda_{\chi}(C) \  \left ( M_{\chi} \right)_{x,y} } $$

This then means that for all for all $$C \in \operatorname{Cl}(G)$$ and all irreducible characters $$\chi \in X(G)$$:

  $$ \overline{ \lambda_{\chi}(C) \  \left ( M_{\chi} \right)_{e_{G},e_{G}} } = \left ( \sum\limits_{c \in C} \chi(c) \right ) \left ( \frac { \left ( M_{\chi} \right)_{e_{G},e_{G}} }{ \left ( M_{\chi} \right)_{e_{G},e_{G}} } \right ) $$
  
  $$ \implies \lambda_{\chi}(C) = \frac{1}{\chi(e_{G})} \ \overline { \left ( \sum\limits_{c \in C} \chi(c) \right ) } $$
   
  **[** assuming the fact that  $$\left ( M_{\chi} \right)_{e_{G},e_{G}} = \chi(e_{G}) \in \mathbb{R} $$ **]**.

Now, observe that for all $$ f,g \in \mathbb{C}[G] $$:

  $$\left ( M_{f} \ M_{g} \right )_{x,y}$$
  
  $$ = \sum\limits_{z \in G} f(x^{-1} z) \ g(z^{-1} y) $$
  
  $$ = \sum\limits_{z \in G} f(x^{-1} z) \ g \left ( z^{-1} \left ( x \ x^{-1} \right ) y \right ) $$

  $$ = \sum\limits_{z \in G} f(x^{-1} z) \ g \left ( \left ( x^{-1} z \right )^{-1} \left ( x^{-1} y \right ) \right ) $$

  $$ = \sum\limits_{z \in G} f(z) \ g \left ( z^{-1} \left ( x^{-1} y \right ) \right ) $$

  $$ = \left ( f \star g \right ) \left ( x^{-1} y \right )$$

  $$ = \left ( M_{f \star g} \right )_{x,y}$$

  **[** by definition **]**.

It follows from this that $$ M_{f}^{2} = M_{f \star f} = \frac{ \lvert G \rvert }{ f(e_G) } \ M_{f} $$ for all $$f \in \mathbb{C}[G]$$.

Next, for all $$f \in \mathbb{C}[G]$$: define $$E_{f} := \frac{ f(e_G) }{ \lvert G \rvert }  M_{f} \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$.

Now, assume the facts that:

  * $$\sum\limits_{x \in G} \chi(x) \ \chi \left ( x^{-1} \right ) = 1 $$

    for all $$\chi \in X(G)$$.
  * $$\sum\limits_{\chi \in X(G)} \chi(x) \ \chi \left ( y^{-1} \right ) = 0$$

    for all $$x,y \in G$$ such that $$y \neq x^{-1}$$.

$$ \implies \sum\limits_{\chi \in X(G)} E_{\chi} = I$$

It is now follows for all $$C \in \operatorname{Cl}(G)$$: 

  $$A_{C} = \sum\limits_{\chi \in X(G)} \lambda_{\chi}(C) \ E_{\chi} $$

**[** since $$A_{C} E_{\chi} = \lambda_{\chi}(C) E_{\chi}$$ for all $$\chi \in X(G)$$, as a consequence of previous points **]**.

Lastly, observe that  for all $$\chi \in X(G)$$ and $$C \in \operatorname{Cl}(G)$$: $$E_{\chi}$$ is a projection onto the eigenspace of $$\lambda_{\chi}(C)$$ and moreover that $$\operatorname{dim} \left( \operatorname{null} \left ( A_{C} - \lambda_{\chi}(C) I \right ) \right )  = \operatorname{tr} \left ( E_{\chi} \right ) = \left (\chi (e_{G}) \right )^{2}$$.

Hence it is now possible to conclude that $$\phi_{C}(x) := \prod\limits_{\chi \in X(G)} \left ( x - \frac{1}{\chi(e_{G})} \ \overline { \left ( \sum\limits_{c \in C} \chi(c)  \right ) } \right )^{\left (\chi (e_{G}) \right )^{2}} \in \mathbb{C}[x] $$ is the characteristic polynomial of $$A_{C}$$ for all $$C \in \operatorname{Cl}(G)$$.

*A general expression for the spectrum of a conjugacy class digraph of a finite group is now immediate from the results verified in this post.*


