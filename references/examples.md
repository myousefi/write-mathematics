# Before-and-After Examples

## Contents

1. Theorem statements
2. Proof architecture
3. Direct versus contradiction proofs
4. Notation
5. Quantifiers
6. Cross-references
7. Definitions
8. Abstracts and introductions
9. Related work and contributions
10. Technical prose and typography

## 1. Theorem statements

### Remove irrelevant assumptions

**Before**

> Let \(R\) be a commutative semisimple ring with unit and let \(x,y\in R\). Then \(x^2-y^2=(x-y)(x+y)\).

**After**

> Let \(R\) be a commutative ring and let \(x,y\in R\). Then \(x^2-y^2=(x-y)(x+y)\).

If commutativity is not required either, weaken further. The point is to prevent the reader from searching for a role played by assumptions that are actually irrelevant.

### Move definitions out of the theorem

**Before**

> **Theorem.** Let \(G=(V,E)\) be a finite directed graph whose edge costs \(c_e\) are nonnegative and whose node capacities satisfy Conditions 1–4 listed above. Then Algorithm 1 terminates in polynomial time and returns an optimal feasible path.

**After**

Define “admissible network” immediately before the theorem.

> **Theorem.** On every admissible network, Algorithm 1 terminates in polynomial time and returns an optimal feasible path.

### Do not mix consequences into the statement

**Before**

> **Theorem.** Every optimal extreme point is integral, and this means that the LP relaxation can be solved instead of the integer program, which is computationally useful.

**After**

> **Theorem.** Every optimal extreme point of the relaxation is integral.

Then discuss the computational consequence in prose after the proof or statement.

## 2. Proof architecture

### Announce strategy

**Before**

> Let \(x\in X\). By Lemma 2, ... Hence ... Applying Proposition 4 ... Therefore the policy is optimal.

**After**

> We prove optimality in two steps. First, we show that the candidate policy is feasible. Second, we construct a lower bound attained by that policy.
>
> **Feasibility.** Let \(x\in X\). ...
>
> **Optimality.** Proposition 4 gives ...
>
> Since the candidate policy attains the lower bound, it is optimal.

### Explain transformation purpose

**Before**

> \[
> J(x)=A(x)+B(x)=C(x)+B(x)=D(x).
> \]

**After**

> Substitute the balance equation into \(A(x)\) and collect the terms depending on \(x\):
> \[
> J(x)=C(x)+B(x).
> \]
> The complementarity condition eliminates \(B(x)\), so
> \[
> J(x)=D(x).
> \]

The second version tells the reader why the equalities are useful.

## 3. Direct versus contradiction proofs

### Prefer the direct structure when it is cleaner

**Before**

> Suppose, for contradiction, that \(b_j>b_i\) for some \(i<j\). Choose \(k\) sufficiently large. Then ... contradicts the assumption. Therefore \(b_i\ge b_j\).

**After**

> Fix \(i<j\). The defining inequality holds for every \(k\ge0\):
> \[
> c_i-c_j\ge k(b_j-b_i).
> \]
> Since the left-hand side is fixed while \(k\) can be arbitrarily large, we must have \(b_j-b_i\le0\). Hence \(b_i\ge b_j\).

The direct proof exposes the actual limiting argument without a temporary negation.

## 4. Notation

### Remove disposable symbols

**Before**

> Let \(X\) be a compact subset of a space \(Y\). If \(f:X\to\mathbb R\) is continuous, then \(f\) attains a minimum on \(X\).

**After**

> Every continuous real-valued function on a compact set attains a minimum.

Use the shorter version when \(X\), \(Y\), and \(f\) are not reused.

### Avoid premature indexing

**Before**

> Let \(X=\{x_1,\ldots,x_n\}\). Consider a subset \(Y=\{x_{i_1},\ldots,x_{i_m}\}\).

**After**

> Let \(X\) be a finite set and let \(Y\subseteq X\).

Introduce names for individual elements only when the proof actually needs them.

### Preserve type conventions

**Before**

> Let \(d_t\) denote random demand and \(D_t\) its observed value.

**After**

> Let \(D_t\) denote random demand and \(d_t\) a realized value.

This is not a universal law, but it matches a common and useful random-variable/realization convention.

## 5. Quantifiers

### Make scope explicit

**Before**

> For every \(n\), the error is bounded by some constant \(C\).

**Uniform bound**

> There exists a constant \(C\), independent of \(n\), such that \(e_n\le C\) for every \(n\).

**Nonuniform bound**

> For every \(n\), there exists a constant \(C_n\) such that \(e_n\le C_n\).

### Clarify asymptotic constant dependence

**Before**

> \(T(n,d)=O(n^d)\).

**After when \(d\) is fixed**

> For every fixed \(d\), there exists a constant \(C_d\) such that \(T(n,d)\le C_dn^d\) for all sufficiently large \(n\).

### Avoid unsupported uniqueness

**Before**

> Let \(x^\star\) be the optimal solution.

**After**

> Let \(x^\star\) be an optimal solution.

Use “the” only after uniqueness is known.

## 6. Cross-references

### Give references semantic content

**Before**

> By (14), (19), and Lemma 7, (24) follows.

**After**

> Substitute the demand recursion (14) into the cumulative balance equation (19). The error bound from Lemma 7 then yields (24).

### Repeat a simple expression instead of forcing lookup

**Before**

> Using (3.2), the bound follows.

**After**

> Recall that \(c_n=n/\log n\) from (3.2). Substituting this expression gives the bound.

## 7. Definitions

### Define both formally and informally when useful

**Before**

> Define \(L(C,P)=\{c+p_1+\cdots+p_m: c\in C,m\ge0,p_j\in P\}\).

**After**

> Define
> \[
> L(C,P)=\{c+p_1+\cdots+p_m: c\in C,m\ge0,p_j\in P\}.
> \]
> Thus, \(L(C,P)\) is the smallest set containing \(C\) that is closed under addition of elements of \(P\).

The second sentence provides a conceptual characterization of the formal definition.

### Do not dump definitions without purpose

**Before**

> Definition 1. ...
>
> Definition 2. ...
>
> Definition 3. ...
>
> Definition 4. ...

**After**

> The decomposition requires one additional concept: a protected echelon. We call echelon \(i\) protected if ...
>
> The next example shows why protection matters before we introduce the associated service-time parameter.

Stage definitions as the reader gains a reason to need them.

## 8. Abstracts and introductions

### Abstract

**Before**

> Supply chains are becoming increasingly complex, and inventory optimization has received significant attention in both academia and industry. In this paper we consider an important and novel problem related to inventory management.

**After**

> We study multi-echelon inventory optimization under correlated demand. We formulate dependence through a joint empirical demand distribution and show that the resulting echelon subproblems remain convex. This yields a decomposition that preserves the tractability of the classical independent-demand model while allowing cross-location dependence.

### Introduction opening

**Before**

> Inventory theory has a long and rich history dating back many decades. Many researchers have considered various inventory problems.

**After**

> We study how demand dependence changes safety-stock allocation in a multi-echelon network. Classical decompositions rely on independence across locations; with correlated demand, the same marginal forecasts can imply different joint service probabilities.

Reveal the problem before the history.

## 9. Related work and contributions

### Related work should express relationships

**Before**

> Smith [4] studied multi-echelon inventory. Jones [7] studied correlated demand. Wang [12] studied decomposition.

**After**

> Classical multi-echelon models exploit independent demand to decompose the network [4]. Jones [7] introduces parametric dependence but retains marginal safety-stock approximations, whereas Wang [12] models the joint distribution directly and loses decomposition. Our formulation retains a decomposable structure while allowing nonparametric joint forecasts.

### Contributions should be verifiable

**Before**

> Our method is novel, powerful, and computationally efficient.

**After**

> The paper makes three contributions. First, it models cross-location dependence through the empirical joint distribution rather than independent marginals. Second, it proves convexity of the resulting echelon subproblem. Third, it derives a decomposition whose number of subproblems grows linearly with the number of echelons for fixed support size.

## 10. Technical prose and typography

### Do not start with a symbol

**Before**

> \(x_n-a\) has \(n\) distinct zeros.

**After**

> The polynomial \(x_n-a\) has \(n\) distinct zeros.

### Put words between symbolic clauses

**Before**

> Consider \(S_q\), \(q<p\).

**After**

> Consider \(S_q\), where \(q<p\).

### Replace formal logic with prose

**Before**

> Therefore, \(\exists x\in S\) such that ...

**After**

> Therefore, there exists \(x\in S\) such that ...

### Add the missing reason

**Before**

> Clearly, \(f\) is convex.

**After**

> Since \(f\) is a nonnegative weighted sum of convex functions, \(f\) is convex.

### Linearize an overloaded sentence

**Before**

> Since demand is independent and the objective can therefore be decomposed, which follows from Proposition 2, we can optimize each echelon separately, provided that the service constraints are separable, as assumed in Section 2.

**After**

> By assumption, the service constraints are separable across echelons. Proposition 2 shows that demand independence also decomposes the objective. We can therefore optimize each echelon separately.

### Use parallel structure

**Before**

> If \(n\) is even, \(P_n\) holds. On the other hand, \(Q_n\) is true whenever \(n\) happens to be odd.

**After**

> If \(n\) is even, then \(P_n\) holds. If \(n\) is odd, then \(Q_n\) holds.
