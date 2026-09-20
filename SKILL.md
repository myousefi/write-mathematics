---
name: write-mathematics
description: Draft, rewrite, edit, explain, and review mathematical exposition for correctness, rigor, reader-oriented structure, proof clarity, notation, terminology, and typesetting. Use for mathematical research papers, theorem/proof writing, optimization and operations-research papers, probability/statistics and theoretical CS writing, technical reports, textbook or monograph chapters, lecture notes, LaTeX-heavy documents, mathematical appendices, or any request to improve or assess mathematically substantive prose.
---
# Write Mathematics

## Core objective

Optimize mathematical writing for the reader's reconstruction of the argument rather than for the author's discovery process. Preserve correctness and rigor while reducing unnecessary cognitive work: hidden goals, long dependency jumps, overloaded notation, unexplained transformations, vague epistemic status, and avoidable backtracking.

Treat mathematical writing as both mathematics and exposition. Never improve the prose by silently changing the mathematics.

## Route the task

Classify the request before editing.

- **Draft from scratch:** build the reader model, mathematical inventory, dependency order, notation, and outline before polished prose.
- **Rewrite or edit:** diagnose document-, section-, proof-, paragraph-, and sentence-level problems before rewriting. Preserve the author's mathematical claims unless correction is requested or a genuine mathematical issue must be surfaced.
- **Review:** separate mathematical defects from expository defects. Report severity and explain why each issue matters.
- **Explain or teach:** adapt detail to the target reader, expose the proof idea before technical execution, and use examples or counterexamples where they clarify mechanism or boundary.
- **Polish LaTeX-heavy text:** preserve semantics first; then improve mathematical grammar, notation, equation layout, references, and typography.

Read the supporting references selectively:

- Read `references/core-principles.md` for substantive drafting, restructuring, or editing.
- Read `references/examples.md` when rewriting difficult passages or generating before/after alternatives.
- Read `references/review-rubric.md` for paper reviews, proof audits, or final quality checks.
- Read `references/source-notes.md` when reconciling competing style rules or explaining the rationale behind a recommendation.

## Non-negotiable boundaries

- Preserve mathematical meaning unless explicitly authorized to change it.
- Flag mathematical errors, missing assumptions, invalid implications, quantifier ambiguity, and unsupported uniqueness claims separately from style issues.
- Do not convert an uncertain mathematical claim into a stronger one merely to improve prose.
- Distinguish proof, assumption, definition, conjecture, heuristic, numerical observation, empirical claim, citation, and deferred argument.
- Prefer clarity over minimum word count.
- Prefer internal consistency over personal stylistic preference.
- Follow venue or journal style when supplied, unless it would create a mathematical ambiguity.

## Workflow for new mathematical writing

### 1. Build a reader contract

Record internally:

- target audience;
- expected mathematical maturity;
- assumed prerequisites;
- notation the reader can be expected to know;
- concepts requiring definition or motivation;
- expected proof detail;
- likely reading mode: linear reading, skimming, or reference use.

Use this contract to decide what to explain and what may be cited or compressed.

### 2. Identify the mathematical payload

Determine:

- the main question;
- the main result or small set of main results;
- why the result matters mathematically or operationally;
- the new idea;
- supporting results;
- limitations;
- closest prior work when relevant.

Do not confuse a list of topics with a paper's thesis.

### 3. Inventory the mathematics

List the objects needed by the exposition:

- definitions;
- assumptions;
- theorems and propositions;
- lemmas;
- algorithms;
- examples and counterexamples;
- figures or tables;
- dependencies among results.

### 4. Build a notation and terminology ledger

Choose notation before polished drafting. Track each object's symbol, semantic role, index convention, and canonical term.

Enforce:

- one object → one notation unless a deliberate local change is justified;
- one notation → one object within a meaningful scope;
- one concept → one canonical term;
- mnemonic and simple notation where practical;
- no new symbol without enough reuse to justify its memory cost.

### 5. Build and linearize the dependency graph

Represent the proof or paper as dependencies rather than discovery chronology. Order definitions, lemmas, and arguments so that prerequisites occur before use and close to their principal use.

Prefer a forward, nearly linear exposition. Extract a reusable lemma only when it reduces repetition, exposes a meaningful concept, or improves navigation.

### 6. Organize into coherent segments

Make each substantive unit answer one recognizable reader question. A segment may contain one theorem and proof, one model choice, one example, or one cluster of closely related results.

Give each segment:

1. orientation or transition;
2. motivation or local question;
3. required definitions;
4. mathematical content;
5. interpretation when useful;
6. transition to what follows.

### 7. Draft formal statements before proofs

State the theorem before proving it. Keep theorem and lemma statements short, self-contained enough for local reading, and free of proof chatter or unrelated consequences.

Define bulky concepts before the formal statement when doing so makes the theorem substantially cleaner.

For each hypothesis, identify where it is used. Remove irrelevant assumptions or explain why a stronger standing assumption is retained.

### 8. Draft proof skeletons before proof prose

Write the proof architecture first:

- goal;
- major steps;
- intermediate results;
- cases;
- conclusion.

Then write forward. Expose strategy when it is not immediate. Keep the reader aware of what is known, what is being shown now, and why the current step matters.

### 9. Add motivation, examples, and interpretation

Use examples to instantiate definitions, expose a mechanism, motivate a model, or reveal a boundary. Use counterexamples to explain why an assumption is necessary or why a converse fails.

Do not add examples that merely repeat the symbols with arbitrary numbers.

### 10. Write prose around the mathematics

Integrate formulas into grammatical sentences. Use prose to explain the purpose of transformations, not merely to narrate symbols.

Use active, direct language. Prefer descriptive nouns over vague pronouns when technical antecedents could be unclear.

### 11. Revise in separate passes

Run at least these passes:

1. mathematical correctness;
2. global architecture and dependency order;
3. reader orientation and proof state;
4. notation and terminology;
5. sentence structure and mathematical grammar;
6. cross-references and examples;
7. typography and equation layout;
8. cold-reader audit.

Rewrite structurally defective passages. Do not merely polish them.

## Workflow for revising existing writing

Diagnose from large scale to small scale.

### Document level

Check whether the main problem, contribution, and result are visible early; whether sections occur in a useful order; whether background delays the core result; and whether material is duplicated.

### Section level

Check whether each section has one coherent job, opens with useful orientation, introduces prerequisites near use, and ends with a meaningful transition when one is needed.

### Theorem and proof level

Check statement cleanliness, assumption use, quantifier scope, proof direction, case organization, hidden dependencies, repeated arguments, and whether the proof's strategy is visible.

### Paragraph level

Check that each paragraph has one principal function and that its sentences occur in dependency order.

### Sentence level

Check grammar, left-to-right readability, pronoun antecedents, long or nonlinear constructions, and whether small words such as “that” or “then” would reduce parsing cost.

### Notation and typography level

Check definitions, consistency, necessity, equation punctuation, labels, delimiters, operators, spacing, and line breaks.

## Mathematical writing rules

Apply the detailed rules in `references/core-principles.md`. In particular:

- state results before their proofs;
- write proofs forward whenever practical;
- announce nontrivial proof strategy;
- define symbols near first serious use;
- minimize notation and excessive indices;
- place words between adjacent symbolic clauses;
- do not begin a normal sentence with a bare mathematical symbol;
- prefer words to `∀`, `∃`, `⇒`, and similar formal logic symbols in ordinary exposition;
- audit hidden quantifiers and constant dependence;
- use “an optimal solution” unless uniqueness is established;
- replace “obvious,” “trivial,” “easy,” and “clearly” with the reason when practical;
- use parallel language for parallel mathematics;
- use semantic cross-references, not only naked numbers;
- number displays only when numbering serves navigation or later reference;
- punctuate displayed mathematics as part of the surrounding sentence;
- distinguish intuitive explanation from rigorous proof;
- omit a proof honestly rather than giving a misleading pseudo-proof.

## Review severity

When reviewing, classify issues as:

- **Critical:** mathematical error, invalid proof step, contradictory definition, missing necessary hypothesis, or materially ambiguous quantifier/claim.
- **Major:** structure that prevents reliable comprehension, missing definition, hidden proof dependency, misleading theorem statement, or notation collision affecting meaning.
- **Moderate:** excessive indirection, weak transitions, unexplained transformations, inconsistent terminology, notation overload, or repeated avoidable backtracking.
- **Minor:** local sentence, punctuation, typography, or house-style issues that do not materially affect comprehension.

Do not give a comma and a missing hypothesis equal weight.

## Output patterns

For a theorem revision, prefer:

```text
REVISED STATEMENT
...

MATHEMATICAL ISSUES
...

EXPOSITORY CHANGES
...
```

For a proof revision, prefer:

```text
PROOF STRATEGY
...

REVISED PROOF
...

MATHEMATICAL ISSUES OR ASSUMPTIONS TO VERIFY
...
```

For a full review, prefer:

```text
CRITICAL
...

MAJOR
...

MODERATE
...

MINOR
...
```

Omit empty categories when that improves readability.

## Final gate

Before returning substantial mathematical prose, verify:

- the mathematics has not been silently changed;
- the main goal is visible;
- all symbols used are defined or conventional for the stated audience;
- dependencies are presented in a workable order;
- every theorem assumption has a role or an explanation;
- the reader can distinguish rigorous claims from motivation or intuition;
- important steps are explained rather than hidden behind evaluative words;
- notation and terminology remain consistent;
- equations are grammatically integrated with prose;
- cross-references minimize unnecessary lookup;
- the level of detail matches the target reader.
