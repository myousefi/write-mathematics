# Core Principles of Mathematical Writing

## Contents

1. Reader model and mathematical payload
2. Global architecture
3. Theorems and proofs
4. Examples and counterexamples
5. Notation and terminology
6. Mathematical prose
7. Quantifiers and epistemic status
8. Cross-references and repetition
9. Abstracts, introductions, conclusions, and appendices
10. Figures and visual structure
11. Revision strategy
12. Priority rules for conflicts

## 1. Reader model and mathematical payload

### Write for a definite reader

Choose a concrete target reader before deciding how much detail to include. Record what the reader knows, what terminology is standard, what can be cited, and what will probably cause difficulty.

Do not aim vaguely at “mathematicians” or “scientists” when the actual audience is, for example, first-year graduate students in optimization or specialists in stochastic networks.

The audience determines:

- prerequisite detail;
- acceptable shorthand;
- proof granularity;
- expected notation;
- appropriate examples;
- the amount of motivation required.

### Have something definite to say

A mathematical document should have a recognizable intellectual center. Identify the main question and the main result before organizing sections.

A list of topics is not a thesis. “Inventory, optimization, forecasting, stochasticity, and supply chains” is not a paper's point. “We show that correlated empirical demand can be incorporated into a multi-echelon inventory model while preserving convex subproblems” is.

### Separate mathematical payload from presentation

Before polishing prose, inventory the mathematical objects that the reader must ultimately understand:

- definitions;
- assumptions;
- results;
- proof dependencies;
- examples;
- limitations;
- algorithms;
- figures.

This inventory prevents the prose from determining the mathematics accidentally.

## 2. Global architecture

### Organize before arranging

Distinguish conceptual organization from linear order.

Organization asks:

- What are the main conceptual units?
- Which results depend on which definitions and lemmas?
- Which examples belong to which idea?
- Which facts are reusable?

Arrangement asks:

- In what sequence should the reader encounter those units?

The dependency structure is usually a graph; the document must be a line. Good mathematical writing chooses a linearization that minimizes reader backtracking and memory burden.

### Present reader order, not discovery order

Research may proceed through failed attempts, special cases, backward reasoning, numerical experiments, or accidental discoveries. The final document should normally present the clean conceptual order unless the history itself provides useful motivation.

Use discovery history only when it explains why a definition, assumption, or new idea is natural.

### Keep prerequisites close to use

Definitions, lemmas, and notation should appear near the place where the reader needs them, subject to logical dependencies.

Long-distance dependencies are expensive. If a term defined many pages earlier reappears unexpectedly, remind the reader of its meaning.

### Segment the exposition

Treat a mathematical document as a sequence of coherent reader-sized segments rather than as an undifferentiated stream.

A segment typically contains one of:

- a theorem and proof;
- a definition with examples;
- a modeling choice and its implications;
- a related cluster of results;
- an algorithmic idea;
- a substantive example.

A useful segment structure is:

1. orientation;
2. local question or motivation;
3. necessary definitions;
4. main argument or result;
5. interpretation;
6. transition.

### Use hierarchy only when it pays

Extract common material into lemmas or special background sections when several later arguments reuse it. Do not create hierarchy merely because a proof is long.

Every new lemma, subsection, or definition creates indirection. Its value must exceed that cost.

## 3. Theorems and proofs

### State the result before proving it

Do not make the reader infer the theorem from a chain of calculations. Give motivation if useful, then the formal statement, then the proof.

The reader can follow a proof more intelligently when the target is visible.

### Keep theorem statements clean

Move these outside the formal theorem statement when possible:

- proof commentary;
- historical discussion;
- “without loss of generality” reasoning;
- informal consequences;
- citations that belong in surrounding prose;
- temporary proof notation.

Define reusable concepts before the theorem if doing so substantially shortens the statement.

### Audit every hypothesis

For each theorem assumption, identify its role in the proof or result.

If an assumption is unused:

- remove it;
- weaken it;
- explain that it is retained as a standing assumption for uniformity;
- or investigate whether the proof is incomplete.

Irrelevant assumptions mislead readers because they invite a search for a nonexistent role.

### Expose proof architecture

For a nontrivial proof, reveal the strategy before the dense details.

Useful forms include:

- “The proof has two steps.”
- “We first establish feasibility and then prove optimality.”
- “The only nontrivial case is the boundary case.”
- “The argument reduces the problem to total unimodularity.”

The reader should continually know:

- what is already established;
- the current subgoal;
- why the current step matters;
- what remains.

### Prefer forward proofs

Authors often discover proofs backward: to prove A, try to prove B; to prove B, seek C. Readers should usually receive the proof forward: establish C, infer B, conclude A.

Backward scaffolding can be useful as a brief strategy statement, but the formal execution should normally proceed from established facts to consequences.

### Avoid unnecessary contradiction

Proof by contradiction increases the reader's logical state: original assumptions, a temporary negation, a contradiction, and a final reversal.

Use contradiction when it exposes the structure. Prefer a direct proof when the same reasoning can be stated forward more cleanly.

### Distinguish rigor from exhaustive algebra

A proof is rigorous when every nontrivial logical step is justified. Rigor does not require narrating every algebraic operation.

Classify omitted steps mentally:

- immediate algebra;
- standard fact known to the audience;
- standard fact requiring citation;
- routine but nontrivial step worth a hint;
- new or essential reasoning that must be shown.

Do not hide the last category behind “clearly.”

### Explain transformations, not only formulas

A chain

\[
A=B=C=D
\]

may be verifiable but still poor exposition if the reader must reverse-engineer why each transformation was chosen.

Explain the strategy:

> Substitute the balance equation into the objective and collect the terms involving \(x_t\). Complementarity eliminates the third term, leaving the desired bound.

### Distinguish explanation from proof

Label heuristics and intuition as such. If a paragraph is motivational and not part of the proof, say so when confusion is plausible.

A reader must never be forced to decide whether a statement is rigorous, suggestive, empirical, or conjectural.

### Omit proofs honestly

If a proof is standard, routine, or outside scope, omit it honestly and provide enough information for the reader to locate or reconstruct it.

Prefer:

> The result follows from the contraction-mapping theorem; see [X, Theorem Y].

or:

> A routine compactness argument gives the claim; we omit the details.

Do not provide a vague half-proof that appears rigorous but is not.

## 4. Examples and counterexamples

### Make examples do work

A good example should perform at least one function:

- instantiate a definition;
- motivate a definition;
- reveal the mechanism of a result;
- illustrate a proof idea;
- show a boundary of applicability;
- demonstrate why an assumption matters.

Avoid examples that merely substitute arbitrary numbers into a formula without adding insight.

### Use counterexamples to expose logical boundaries

When a converse fails or an assumption is essential, a counterexample is often the clearest explanation.

For example, after stating that strict convexity implies uniqueness, show that convexity alone does not:

\[
f(x)=0\quad\text{on }[0,1]
\]

is convex and has infinitely many minimizers.

### Explain nonimplications

Do not write “A does not imply B” and continue without support when the nonimplication matters.

Use one of:

- a counterexample;
- a promised later counterexample;
- a reference;
- an explicit statement that the question is open.

## 5. Notation and terminology

### Design notation before drafting

Maintain a notation ledger for substantial work. Record symbol, object, semantic type, and indexing convention.

Good notation should be:

- consistent;
- simple;
- mnemonic when possible;
- visually distinguishable;
- stable across sections.

### Treat notation as a semantic system

Use consistent families where appropriate:

- capital letters for sets or random variables;
- lowercase for realizations or scalars;
- \(i,j,k\) for indices;
- \(t,s\) for time;
- calligraphic letters for families or feasible regions;
- Greek letters for parameters.

These are conventions, not universal laws. Internal consistency matters more than any one alphabet policy.

### Minimize notation

Every symbol creates memory cost. Do not name an object used once unless naming it materially clarifies the expression.

Prefer:

> Every continuous real-valued function on a compact set attains a minimum.

when the symbols \(X\) and \(f\) would never be reused.

### Avoid index explosions

Do not begin with \(X=\{x_1,\ldots,x_n\}\) if the elements do not need names. Premature indexing often creates later expressions such as subscripted subscripts.

When a symbol becomes visually overloaded, consider:

- changing representation;
- moving one dimension into function arguments;
- relying on local context;
- introducing a meaningful named object.

### Define symbols near first serious use

A symbol introduced long before its first real use is easily forgotten. Delay the definition or remind the reader when it returns.

### Use canonical terminology

Choose among synonyms once unless a genuine distinction is intended. Do not alternate “edge,” “arc,” and “link” for the same object simply for stylistic variety.

### Use technical terms precisely

Do not weaken mathematical terminology casually:

- independent ≠ uncorrelated;
- random variable ≠ random value;
- optimal ≠ locally optimal;
- unique ≠ selected;
- function ≠ function value.

Precision should be unobtrusive, not pedantic.

## 6. Mathematical prose

### Keep mathematics grammatical

Treat formulas as constituents of sentences. Punctuate displayed equations according to the grammar of the surrounding sentence.

Example:

> Since
> \[
> x+y=z,
> \]
> the conservation constraint is satisfied.

The comma belongs after the display because the mathematical clause is part of the sentence.

### Do not begin a normal sentence with a bare symbol

Prefer:

> The variable \(x\) is positive.

or:

> It follows that \(x\) is positive.

instead of:

> \(x\) is positive.

### Put words between adjacent symbolic clauses

Avoid:

> Consider \(S_q\), \(q<p\).

Prefer:

> Consider \(S_q\), where \(q<p\).

### Prefer words to formal logic symbols in prose

In ordinary exposition, write:

> For every \(x\in S\), there exists \(y\in T\) such that ...

rather than:

> \(\forall x\in S\,\exists y\in T\) ...

Formal logic notation is appropriate when formal logic itself is the subject or when a display genuinely benefits from it.

### Write sentences in dependency order

Avoid sentences that require the reader to revise their interpretation as later clauses arrive.

Bad:

> It follows that, since \(x>0\), we have \(f(x,y)>0\), because \(y>0\), and therefore, using Theorem 3, since \(f\) is irreducible, it is primitive.

Better:

> The function \(f\) is irreducible. Theorem 3 therefore implies that \(f\) is primitive. Since \(x>0\) and \(y>0\), we also have \(f(x,y)>0\).

### Preserve helpful small words

Do not remove “that” or “then” merely for brevity if they make parsing easier.

Prefer:

> If \(n\) is odd, then \(n\neq0\).

> Assume that \(A\) is invertible.

when those forms read more smoothly.

### Use active direct prose

Prefer:

> We now prove the bound.

or simply:

> The next lemma proves the bound.

instead of:

> It will now be shown that the bound holds.

Use “we” naturally as author and reader proceeding through the argument, not as a mechanical substitute for every subject.

### Avoid inflated language

Keep the prose intellectually serious but linguistically plain.

Prefer:

> This formulation yields a simpler feasible set.

instead of:

> The aforementioned formulation facilitates the attainment of a more advantageous characterization of the feasible region.

### Use parallel language for parallel mathematics

When two statements differ in one mathematical feature, preserve the grammatical structure so the mathematical contrast is visible.

> If \(n\) is even, then \(P_n\) holds.
>
> If \(n\) is odd, then \(Q_n\) holds.

Do not rewrite the second sentence merely to avoid repetition.

### Make pronouns unambiguous

Replace vague pointers when multiple technical objects are nearby.

Bad:

> Substituting this into the bound proves it.

Better:

> Substituting the capacity bound into (14) proves the desired inequality.

## 7. Quantifiers and epistemic status

### Audit quantifier order

Natural-language quantifiers can hide radically different statements.

The sentence

> For every \(n\), we have \(n<c\) for some \(c\).

can mean either \(\forall n\exists c\) or \(\exists c\forall n\).

Rewrite until the scope is explicit.

### Make hidden constant dependence explicit

Asymptotic notation often conceals quantifiers.

If the intended statement is “for every fixed \(d\), there exists \(C_d\),” say so. Do not allow readers to infer a uniform constant accidentally.

### Use articles mathematically

“The optimal solution” implies uniqueness. If uniqueness has not been proved, write “an optimal solution.”

Apply the same discipline to minimizers, stationary distributions, fixed points, and other objects that may be nonunique.

### Avoid evaluative shortcuts

Treat “obvious,” “trivial,” “easy,” and “clearly” as warning signs. Replace them with the reason whenever practical.

Instead of:

> Clearly, \(f\) is convex.

write:

> Since \(f\) is a nonnegative weighted sum of convex functions, \(f\) is convex.

### Declare epistemic status

Signal whether a statement is:

- proved here;
- assumed;
- standard;
- cited;
- conjectured;
- observed numerically;
- empirical;
- deferred;
- heuristic.

Example:

> Numerical experiments suggest monotonicity under correlated demand; we have not proved this property.

This is substantially better than “The policy appears monotone.”

## 8. Cross-references and repetition

### Prefer semantic references

Avoid forcing readers to decode naked numbers.

Weak:

> By (14), (19), and Lemma 7, (24) follows.

Better:

> Substitute the demand recursion (14) into the cumulative balance equation (19). The error bound from Lemma 7 then gives (24).

Numbers tell the reader where; descriptive phrases tell the reader what.

### Repeat simple expressions when cheaper than lookup

A short expression may be easier to repeat than to reference remotely. Avoid unnecessary page flipping and memory retrieval.

### Number only useful displays

Number equations that will be referenced, serve as landmarks, or represent important named relations. Do not label disposable algebraic intermediates merely because they are displayed.

### Repeat parallel wording deliberately

Word-for-word repetition can be good when it highlights a precise mathematical difference.

### Avoid repeated substantial proofs

If two proofs share the same real argument, extract the common reasoning into a meaningful lemma or reusable statement.

## 9. Abstracts, introductions, conclusions, and appendices

### Abstract

Make the abstract informational rather than ceremonial.

Usually answer:

1. What problem is studied?
2. What framework or setting is used?
3. What is the main result?
4. What is technically distinctive?
5. Why does the result matter, if this can be stated concretely?

Use minimal notation. Avoid generic background, marketing adjectives, and a literature history.

### Introduction

Reveal the paper's problem early. Do not make the reader traverse a historical essay before learning what the paper does.

A useful order is:

1. frame the problem;
2. motivate it;
3. place it in the literature;
4. preview the main results and contributions;
5. give the paper roadmap if useful.

### Related work

Describe relationships among papers, not just a sequence of citations.

Explain whether prior work:

- assumes more or less;
- solves a special or general case;
- uses a different method;
- loses or gains tractability;
- proves a stronger or weaker result.

### Contributions

State contributions as verifiable claims rather than praise.

Avoid self-evaluative language such as “groundbreaking,” “powerful,” or “highly significant.” Let the result demonstrate its importance.

### Conclusions

Do not merely rewrite the abstract in past tense. Use the conclusion to surface conceptual lessons, limitations, open questions, conjectures, or nontrivial extensions.

### Appendices

Move long or specialized material to an appendix when doing so preserves the main narrative. Keep the main text conceptually self-contained: state any result needed by the main argument in the main text even if its proof is deferred.

## 10. Figures and visual structure

### Use figures to communicate structure

A figure should do something prose or equations do less efficiently, such as show:

- a dependency graph;
- a network;
- geometric intuition;
- an algorithm state;
- a feasible region;
- a proof mechanism;
- convergence behavior.

### Keep figures simple

Do not use decorative complexity. Remove visual elements that do not support the mathematical point.

### Write substantial captions

A caption should help a skimming reader understand what the figure demonstrates. It should augment the body text rather than merely repeat the title.

### Balance prose and symbols visually

Dense uninterrupted prose is difficult to scan. Pages filled almost entirely with formulas become code-like. Use displays, paragraphs, and prose so the eye can recover the structure of the argument.

## 11. Revision strategy

### Rewrite, do not merely edit

When the logical order is wrong, changing punctuation and vocabulary will not repair the exposition. Reconstruct the paragraph or section from the dependency order.

### Use separate revision passes

Do not rely on one generic proofread.

Recommended passes:

1. correctness;
2. architecture;
3. proof and dependency flow;
4. reader orientation;
5. notation and terminology;
6. prose and grammar;
7. references and examples;
8. typography;
9. cold-reader review.

Different passes reveal different defects.

### Use the formula deletion test

Mentally replace substantial formulas with “[EQUATION]” and read the prose. The reader should still understand the narrative purpose of the mathematics.

If the remaining prose says only “therefore [EQUATION], hence [EQUATION],” add semantic explanation.

### Use the symbol substitution test

Read sentences aloud with symbols replaced by their spoken grammatical meaning. If the sentence becomes ungrammatical or awkward, rewrite it.

### Use the left-to-right test

At each point in a sentence, ask whether a reader can correctly interpret what has appeared so far without waiting for a later clause to repair the parse.

### Use the distance-to-definition test

The farther an unusual term or symbol is from its definition, the more likely a reminder is worthwhile.

### Use the assumption-removal test

For every assumption, ask what breaks if it is removed. This can reveal unnecessary hypotheses, missing counterexamples, or opportunities for generalization.

### Use a notation budget

Treat reader working memory as limited. Heavily decorated variables, multiple indices, and custom operators consume more of that budget than simple symbols.

## 12. Priority rules for conflicts

Mathematical style authorities differ on pronouns, equation numbering, punctuation conventions, and other local matters. Resolve conflicts in this order:

1. mathematical correctness;
2. unambiguous meaning;
3. explicit logical structure;
4. reader orientation;
5. internal consistency;
6. cognitive economy;
7. concision;
8. rhythm;
9. elegance;
10. typographic aesthetics.

Follow a journal or venue's house style when supplied, unless it creates mathematical ambiguity.
