# Mathematical Writing Review Rubric

## Contents

1. Severity model
2. Mathematical integrity audit
3. Architecture audit
4. Theorem and proof audit
5. Notation audit
6. Prose audit
7. Cross-reference audit
8. Visual and typesetting audit
9. Recommended review output
10. Final release checklist

## 1. Severity model

Use severity to prevent stylistic polish from obscuring substantive defects.

### Critical

Use for issues that can make the mathematics false, undefined, or materially misleading:

- invalid implication;
- missing necessary hypothesis;
- incorrect theorem;
- proof gap in an essential step;
- contradictory definitions;
- quantifier ambiguity that changes truth conditions;
- unsupported uniqueness or existence claim;
- notation collision that changes meaning.

### Major

Use for issues that substantially impair reliable understanding:

- theorem statement does not match proof;
- important symbol undefined;
- dependency presented before prerequisites;
- proof strategy hidden in a way that makes the proof difficult to verify;
- essential assumption buried in prose;
- main result or contribution not discoverable;
- main text relies on appendix-only definitions or results.

### Moderate

Use for avoidable cognitive burden:

- notation overload;
- excessive long-distance references;
- unexplained algebraic transformations;
- weak section transitions;
- terminology drift;
- repeated substantial arguments that should be factored;
- excessive formalism or excessive informality for the audience.

### Minor

Use for local defects that do not materially change comprehension:

- punctuation;
- local word choice;
- minor rhythm problems;
- typographic spacing;
- house-style inconsistency;
- avoidable but harmless repetition.

## 2. Mathematical integrity audit

For every major result, verify:

- What exactly is claimed?
- What are the quantifiers?
- Does the theorem use “a” or “the” appropriately?
- Are all symbols defined?
- Are assumptions sufficient?
- Is every hypothesis used or justified?
- Are boundary cases covered?
- Does the proof establish exactly the stated conclusion?
- Are imported results cited or clearly identified as standard?
- Are heuristic or numerical claims labeled as such?

When a mathematical issue is found during a writing review, do not silently repair it. Explain the issue and propose a conditional rewrite if appropriate.

## 3. Architecture audit

### Document level

Check:

- main problem visible early;
- main result visible early enough for the venue;
- contribution distinct from background;
- section order follows dependencies;
- background does not delay the core problem unnecessarily;
- repeated material consolidated;
- appendices support rather than fragment the main narrative.

### Section level

Check:

- one coherent purpose;
- useful opening orientation;
- definitions near use;
- internal dependency order;
- examples positioned where they answer a reader question;
- ending clarifies what was accomplished or what comes next when needed.

### Segment level

Check whether the reader can identify:

- current question;
- prerequisites;
- result or argument;
- local interpretation;
- relation to surrounding material.

## 4. Theorem and proof audit

### Theorem statement

Check:

- theorem appears before proof;
- statement is concise;
- irrelevant assumptions removed;
- no proof commentary inside statement;
- consequences moved outside when not part of the formal result;
- defined concepts used to reduce clutter;
- notation locally understandable.

### Proof

Check:

- strategy visible for nontrivial arguments;
- proof proceeds mostly forward;
- cases announced before use;
- each substantial step has a reason;
- difficult steps not hidden behind “clearly” or “standard”; 
- routine algebra not over-expanded;
- contradiction used only when helpful;
- repeated proof patterns factored appropriately;
- reader can distinguish proof from motivation.

### Reader-state test

At representative points, ask whether the reader knows:

- KNOWN: what facts are established;
- GOAL: what is being proved;
- CURRENT STEP: what is happening now;
- WHY: why the step advances the argument.

If one of these becomes unclear for more than a short passage, add orientation.

## 5. Notation audit

Create or inspect the notation ledger.

Check:

- one object uses one symbol consistently;
- one symbol is not reused incompatibly;
- terms are canonical and stable;
- notation matches semantic type when practical;
- every symbol is defined near first serious use;
- temporary symbols are worth their cost;
- excessive indices or decorations are reduced;
- function/value distinctions are preserved where needed;
- operators and sets have consistent typography.

### Notation budget test

Flag pages or paragraphs that introduce many high-cost objects at once:

- multi-index variables;
- decorated variables;
- custom operators;
- multiple new abbreviations;
- one-use shorthand.

Stage or simplify their introduction.

## 6. Prose audit

Check:

- sentences are interpretable left to right;
- formulas are grammatically integrated;
- normal sentences do not begin with bare symbols;
- adjacent symbolic clauses are separated by words;
- formal logic symbols are not used as ordinary prose without reason;
- “that” and “then” are present when they improve parsing;
- pronoun antecedents are clear;
- active direct constructions are preferred;
- jargon is necessary and audience-appropriate;
- long noun stacks are rewritten;
- parallel mathematics uses parallel prose;
- evaluative words such as “obvious,” “trivial,” “easy,” and “clearly” are justified or replaced.

### Formula deletion test

Replace substantial formulas mentally with `[EQUATION]` and read the prose. The narrative should still explain what the mathematics is doing.

### Left-to-right test

Read each difficult sentence incrementally. If later words force reinterpretation of earlier words, rewrite.

## 7. Cross-reference audit

Check:

- important equations/results have descriptive references;
- naked number chains are avoided;
- simple expressions are repeated when lookup would cost more;
- unusual notation receives reminders after long gaps;
- displays are numbered only when useful;
- theorem/lemma labels are consistent;
- remote references are not required for every local step.

## 8. Visual and typesetting audit

Check:

- prose and display math are visually balanced;
- long formulas are broken logically;
- equation punctuation matches sentence grammar;
- delimiters scale appropriately;
- operators such as `max`, `sup`, and `inf` use operator/roman styling;
- conditional bars have readable spacing;
- fractions do not unnecessarily destroy line spacing;
- figures are simple and purposeful;
- captions explain what the reader should see;
- line breaks do not isolate important symbols awkwardly.

## 9. Recommended review output

Use this structure unless the user requests another format.

### Summary

State the paper or proof's current strengths and the dominant failure mode without giving an overall score.

### Critical

For each issue:

- location;
- problem;
- mathematical consequence;
- recommended correction.

### Major

For each issue:

- location;
- reader difficulty;
- structural recommendation.

### Moderate

Group related patterns when possible, such as notation drift or excessive cross-references.

### Minor

Keep local style comments concise. Do not overwhelm the author with low-value edits when substantive problems remain.

### Optional rewrite

Provide a revised passage only after explaining the underlying problem when the user asked for review rather than direct rewriting.

## 10. Final release checklist

### Mathematical integrity

- [ ] Main claims are correctly stated.
- [ ] Quantifier order is unambiguous.
- [ ] Uniqueness is claimed only when established.
- [ ] Assumptions are sufficient and relevant.
- [ ] Boundary cases are handled.
- [ ] Proofs match statements.
- [ ] Heuristics and numerical observations are labeled.

### Architecture

- [ ] Main problem is visible early.
- [ ] Main contribution is visible early.
- [ ] Section order follows dependencies.
- [ ] Each section has one coherent job.
- [ ] Definitions and lemmas occur near use.

### Proofs

- [ ] Result precedes proof.
- [ ] Nontrivial strategy is announced.
- [ ] Proof is mostly forward.
- [ ] Essential steps are explicit.
- [ ] Repetition is factored appropriately.

### Notation

- [ ] Every symbol is defined or standard for the audience.
- [ ] Same object uses same notation.
- [ ] Same symbol is not reused incompatibly.
- [ ] Excessive indices and decorations are removed.
- [ ] Terminology is consistent.

### Prose

- [ ] Sentences read naturally left to right.
- [ ] Bare symbols do not start normal sentences.
- [ ] Formulas are integrated grammatically.
- [ ] Vague pronouns are resolved.
- [ ] Evaluative shortcuts are replaced by reasons where useful.
- [ ] Parallel concepts use parallel language.

### Navigation

- [ ] Cross-references identify content as well as number.
- [ ] Equation numbering is purposeful.
- [ ] Distant definitions are reminded when necessary.
- [ ] Figures and captions support skimming.

### Revision

- [ ] Correctness pass completed.
- [ ] Structural pass completed.
- [ ] Notation pass completed.
- [ ] Sentence-level pass completed.
- [ ] Cold-reader pass completed.
