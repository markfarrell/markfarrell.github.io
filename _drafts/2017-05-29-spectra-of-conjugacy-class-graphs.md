---
layout: post
title:  "Spectra of Conjugacy Class Graphs"
date:   2017-05-29
---

Previously, I established that the set of conjugacy class diagraphs of a finite group gives rise to a (commutative) association scheme. It consequently follows that the adjacency matrix of a conjugacy class digraph of a finite group is normal and hence is diagonalizable. I would now like to verify how to derive a general expression for the spectrum of a conjugacy class digraph of a finite group.

Suppose that $$G$$ is a finite a group. Let $$e_{G}$$ denote the identity element of $$G$$, $$\operatorname{Cl}(G)$$ denote the set of conjugacy classes of $$G$$, $$\mathbb{C}[G]$$ denote the space of all total functions from $$G$$ to $$\mathbb{C}$$, $$X(G) \subset \mathbb{C}[G]$$ denote the set of irreducible characters of $$G$$ into $$\mathbb{C}$$, $$B := \{ \delta_{g} : g \in G \} $$ denote the standard basis for $$\mathbb{C}[G]$$, $$\operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote the space of $$\lvert G \rvert \times \lvert G \rvert$$ complex matrices whose rows and columns are indexed by the elements of $$G$$ relative to a certain ordering of them, and $$\mathcal{A} := \{ A_{C} : C \in \operatorname{Cl}(G) \} \subset \operatorname{Mat}_{G \times G}(\mathbb{C})$$ denote a set of adjacency matrices for the set of conjugacy class digraphs of $$G$$. Define:

* $$ \left ( M_{f} \right ) \in \operatorname{Mat}_{G \times G}(\mathbb{C})$$

  $$ \left ( M_{f} \right )_{x,y} := f(x^{-1} y) $$

  for all $$ f \in \operatorname{F}(G, \mathbb{C}) $$.

* $$ \left ( \star \right ) : \mathbb{C}[G] \times \mathbb{C}[G] \to \mathbb{C}[G] $$

  $$ \left ( f \star g \right )(x) := \sum\limits_{y \in G} f(y) g(y^{-1} x) $$

  turning $$ \mathbb{C}[G] $$ into the group ring of $$G$$ over $$\mathbb{C}$$.
   
Next, for all $$C \in \operatorname{Cl}(G)$$ and all irreducible representations $$F \in \operatorname{Hom} \left (G, \operatorname{Aut}(\mathbb{C}[G] ) \right )$$:

*  Interpret the group ring $$\mathbb{C}[G]$$ as a module $$\left ( \mathbb{C}[G], \cdot \right )$$ over itself, defining the scalar multiplication operation $$ (\cdot) : \mathbb{C}[G] \times \mathbb{C}[G] \to \mathbb{C}[G] $$ as $$ \left ( \delta_{g} \cdot f \right ) := F(g) \circ f $$ for all $$g \in G$$. 

   Assume the facts that:

     1. $$ \sum\limits_{c \in C} F(c)  \in \operatorname{End}\left ( \mathbb{C}[G], \cdot \right ) $$
     2. $$ \operatorname{End}\left ( \mathbb{C}[G], \cdot \right ) \subset \{ \lambda I : \lambda \in \mathbb{C} \} $$

        *which is to say that Schur's lemma is true in this context*.

It is now possible to deduce that for all $$C \in \operatorname{Cl}(G)$$ and all irreducible characters $$\chi \in X(G)$$

there is a $$\lambda_{\chi}(C) \in \mathbb{C}$$ such that for all $$x,y \in G$$:

 * $$ \left ( A_{C} \ M_{\chi} \right )_{x,y} $$

   $$ = \sum\limits_{z \in G, \ zx^{-1} \in C} \chi(z^{-1}y) $$

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

   $$ = \operatorname{tr} \left ( \left ( \overline { \lambda_{\chi} } I \right ) \ F \left ( y x^{-1} \right ) \right ) $$

   **[** by previous set of assumptions **]**

   $$ = \overline { \lambda_{\chi}(C) } \ \operatorname{tr} \left ( F \left ( y x^{-1} \right ) \right ) $$

   **[** again, by linearity of trace **]**

   $$ = \overline { \lambda_{\chi}(C) } \ \chi \left ( y x^{-1} \right ) $$

   $$ = \overline { \lambda_{\chi}(C)  \  \chi \left (  x^{-1} y \right ) } $$

   **[** assuming the fact that $$\chi \left ( g^{-1} \right ) = \overline { \chi \left ( g \right )} $$ for all $$ g \in G $$ **]**

   $$ = \overline{ \lambda_{\chi}(C) \  \left ( M_{\chi} \right)_{x,y} } $$

This then means that for all for all $$C \in \operatorname{Cl}(G)$$ and all irreducible characters $$\chi \in X(G)$$:

   * $$ \overline{ \lambda_{\chi}(C) \  \left ( M_{\chi} \right)_{e_{G},e_{G}} } = \left ( \sum\limits_{c \in C} \chi(c) \right ) \left ( \frac { \left ( M_{\chi} \right)_{e_{G},e_{G}} }{ \left ( M_{\chi} \right)_{e_{G},e_{G}} } \right ) $$

     $$ \implies \lambda_{\chi}(C) = \frac{1}{\chi(e_{G})} \overline { \left ( \sum\limits_{c \in C} \chi(c) \right ) } $$

     **[** assuming the fact that  $$\left ( M_{\chi} \right)_{e_{G},e_{G}} = \chi(e_{G}) \in \mathbb{R} $$ **]**.

