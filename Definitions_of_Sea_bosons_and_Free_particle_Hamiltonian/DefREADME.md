# Sea Displacement Operators and Sea Bosons

This repository documents the definitions and basic structure of **sea displacement operators** and **sea bosons** as used in the bosonization-based treatment of interacting Fermi systems.  
The material follows the formalism developed by **Girish S. Setlur** and collaborators, and closely mirrors the definitions summarized in the attached note:

> *Definitions of Sea bosons and free particle Hamiltonian* — R. P. Joshi  

The goal of this README is to serve as a **precise reference** for notation, operator definitions, and their role in rewriting the fermionic Hamiltonian.

---

## 1. Motivation

Bosonization beyond one dimension requires a careful identification of collective particle–hole degrees of freedom around the Fermi surface.  
The **sea displacement operator** formalism provides such a construction by explicitly encoding particle–hole excitations while preserving fermionic statistics at the operator level.

This framework allows:
- A quadratic (bosonic) rewriting of the kinetic energy
- A transparent treatment of density–density interactions
- A controlled large-$N$ (or RPA-like) expansion

---

## 2. Sea Displacement Operators (General Definition)

Following Setlur and Chang (1998), the **sea displacement operator** is defined as

$$
A_{\mathbf{k}}(\mathbf{q})
=\frac{1}{\sqrt{n_{\mathbf{k}-\mathbf{q}/2}}}
\,
c^\dagger_{\mathbf{k}-\mathbf{q}/2}
\left(
\frac{n_\beta(\mathbf{k}-\mathbf{q}/2)}{\langle N \rangle}
\right)^{1/2}
e^{i\theta(\mathbf{k},\mathbf{q})}
c_{\mathbf{k}+\mathbf{q}/2}.
$$

Here:
- $c^\dagger, c$ are fermionic creation/annihilation operators
- $n_\beta(k)$ is the momentum distribution
- $\theta(\mathbf{k},\mathbf{q})$ is a phase ensuring generality
- $\langle N \rangle$ is the average particle number

With this definition, the **kinetic energy** can be rewritten as

$$
\mathrm{KE}
=\sum_{\mathbf{k},\mathbf{q}}
\frac{\mathbf{k}\cdot\mathbf{q}}{m}
\,
\Lambda_{\mathbf{k}}(-\mathbf{q})
A^\dagger_{\mathbf{k}}(\mathbf{q})
A_{\mathbf{k}}(\mathbf{q})
+
N\varepsilon_0,
$$

where

$$
\Lambda_{\mathbf{k}}(\mathbf{q})
=\frac{n_{\mathbf{k}+\mathbf{q}/2} - n_{\mathbf{k}-\mathbf{q}/2}}{1}.
$$

---

## 3. Interacting Hamiltonian

Including density–density interactions, the fermionic Hamiltonian becomes

$$
H=\sum_{\mathbf{k},\mathbf{q}}
\omega_{\mathbf{k}}(\mathbf{q})
A^\dagger_{\mathbf{k}}(\mathbf{q})
A_{\mathbf{k}}(\mathbf{q})
+\sum_{\mathbf{q}\neq 0}
\frac{v_{\mathbf{q}}}{2V}
\sum_{\mathbf{k},\mathbf{k}'}
\Big[\Lambda_{\mathbf{k}}(\mathbf{q})A_{\mathbf{k}}(-\mathbf{q})
+\Lambda_{\mathbf{k}}(-\mathbf{q})A^\dagger_{\mathbf{k}}(\mathbf{q})
\Big]\Big[\Lambda_{\mathbf{k}'}(-\mathbf{q})A_{\mathbf{k}'}(\mathbf{q})
+\Lambda_{\mathbf{k}'}(\mathbf{q})A^\dagger_{\mathbf{k}'}(-\mathbf{q})
\Big].
$$

The dispersion is

$$
\omega_{\mathbf{k}}(\mathbf{q})=
\frac{\mathbf{k}\cdot\mathbf{q}}{m}
\Lambda_{\mathbf{k}}(-\mathbf{q}),
$$

and $v_{\mathbf{q}}$ is the Fourier transform of the interaction potential.

---

## 4. Zero-Temperature Sea Bosons

At $T=0$, the Fermi distribution is

$$
n_F(\mathbf{k}) = \Theta(k_F - |\mathbf{k}|).
$$

Define projected fermionic operators:

$$
c^\dagger_{\mathbf{p},<} = n_F(\mathbf{p}) c^\dagger_{\mathbf{p}},
\quad c^\dagger_{\mathbf{p},>} = [1 - n_F(\mathbf{p})] c^\dagger_{\mathbf{p}},
$$

with analogous definitions for annihilation operators.

The **sea boson** operator is then

$$
a^\dagger_{\mathbf{p}}(\mathbf{q})
=c^\dagger_{\mathbf{p}+\mathbf{q}/2,>}
c_{\mathbf{p}-\mathbf{q}/2,<}.
$$

The corresponding sea displacement operator can be written as

$$
A_{\mathbf{k}}(\mathbf{q})
=c^\dagger_{\mathbf{k}-\mathbf{q}/2,<}
\frac{1}{\hat N_>}
c_{\mathbf{k}+\mathbf{q}/2,>},
$$

where

$$
\hat N_> = \sum_{\mathbf{k}} c_{\mathbf{k},<} c^\dagger_{\mathbf{k},<}.
$$

---

## 5. Kinetic Energy in Sea-Boson Language

With these definitions, the kinetic energy becomes

$$
\mathrm{KE}
=\sum_{\mathbf{p}}
\frac{|\mathbf{p}|^2}{2m}
n_F(\mathbf{p})
+
\sum_{\mathbf{k},\mathbf{q}}
\frac{\mathbf{k}\cdot\mathbf{q}}{m}
A^\dagger_{\mathbf{k}}(\mathbf{q})
A_{\mathbf{k}}(\mathbf{q}),
$$

or equivalently,

$$
\mathrm{KE}
=\sum_{\mathbf{p}}
\frac{|\mathbf{p}|^2}{2m}
n_F(\mathbf{p})
+
\sum_{\mathbf{k},\mathbf{q}}
\frac{\mathbf{k}\cdot\mathbf{q}}{m}
\frac{1}{N_>}
a^\dagger_{\mathbf{k}}(\mathbf{q})
a_{\mathbf{k}}(\mathbf{q}).
$$

---

## 6. Relation to Girish Setlur’s Book

These constructions are part of a broader program developed by **Girish S. Setlur** on higher-dimensional bosonization and Fermi liquids.  
For a systematic and conceptual treatment—including derivations, physical interpretation, and applications—see Setlur’s monograph on bosonization and interacting Fermi systems.

This README should be viewed as a **definitions-and-notation companion**, not a replacement for the full theoretical development in the book.

---

## 7. References

1. G. S. Setlur and Y.-C. Chang,  
   *Single-particle Green functions in exactly solvable models of Bose and Fermi liquids*, 1998.

2. G. S. Setlur, *Dynamics of Classical and Quantum Fields: An Introduction* (book).

---

## 8. Scope

This repository focuses strictly on:
- Operator definitions
- Hamiltonian rewriting
- Kinematic structure

It intentionally avoids:
- Diagrammatics
- Correlation-function calculations
- Renormalization or RG analysis

Those belong in follow-up notes or code modules.
