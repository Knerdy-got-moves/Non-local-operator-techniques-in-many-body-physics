# Exact Bosons through Iterative Methods

## Motivation

These notes develop a dimension-agnostic method for solving Green's functions in interacting fermionic systems via extended bosonization. Fermionic momentum-basis operators express in terms of sea-boson operators $a_k(q)$, enabling iterative solutions starting from SRPA and advancing to GRPA. Commutator approximations in sea-boson relations create inconsistencies during iteration, which these constructions identify and verify.

## Methods

The core approach uses iterative expansions of exponentials involving sea-boson operators. Key steps include deriving operator expressions, applying SRPA/GRPA approximations, and checking commutators like $[a_k(q), a^\dagger_{k'}(q')]$ for consistency across iterations. All derivations appear in the LaTeX manuscript with explicit verification.

## Contents

- `ExponAKQ (1).tex` – Full LaTeX source with iterative expansions, commutator algebra, and approximation checks.


## Build Instructions

Compile the PDF locally with:

```bash
pdflatex "ExponAKQ (1).tex"
```

Run twice for resolved references and cross-links.

## Results

Iterative constructions reveal tensions in sea-boson commutators under SRPA/GRPA, exposing non-exact bosonization beyond lowest order. Higher iterations amplify approximation errors, confirming the need for exact treatments in strongly interacting regimes.

## Conclusion

This framework highlights limitations of approximate bosonization for Green's functions, paving the way for exact iterative methods in quantum many-body systems. Future work could integrate symmetry constraints to resolve commutator issues.
