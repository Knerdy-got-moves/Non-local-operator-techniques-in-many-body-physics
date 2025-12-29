# Momentum-Space Fermion-to-Sea Boson Mapping Using Ansatz

This repository derives momentum-space fermionic creation/annihilation operators in terms of "sea bosons" for a momentum-agnostic approach to Green's functions, extending bosonization ideas to equilibrium quantum many-body systems.

## Project Overview

The core goal is expressing fermionic fields $c_{p+q}$ and bilinears via sea bosons $b_{k}(q)$, enabling exact time evolution and correlation functions without position-space limitations. Key steps include Fermi bilinears in terms of Sea bosons $a_{k}(q)$, field operators with phase factors $e^{iN_p}$, and commutator verifications.

## Key Derivations

- **Fermi Bilinears**: $c_{p-q/2, <} c^\dagger_{p + q/2, <} = \sum_{q_1} a^\dagger_{p-q/2 + q_1/2}(q_1) \frac{1}{N_{>}+1} a_{p+q_1/2}(-q+q_1)$
 and off-diagonal terms.
- **Field Operators**: $c_{p+q_2}^\dagger = e^{i N_p q_2} c_{p+q_2}^\dagger (1 - n_{p+q_2}) + \cdots$, preserving free fermion time evolution $c_{p,t} \sim e^{i p t}$.
- **Sea Bosons**: $b_{k}(q)^\dagger b_{k}(q) = n_F(k+q_2)(1 - n_F(k+q_2)) + n_{k+q_2}(1 - n_{k+q_2})$, with implicit equations for occupation numbers.
- **Green's Functions**: Leads to RPA-like correlations $G_{d}(k,q)$ and 1D/3D density responses via integrals over $a_{k}(q)$.


## Main Document

Detailed derivations and verifications are in the attached PDF: [Moving_towards_expectation_value__The_guess_solution_trial_6.pdf](https://github.com/Knerdy-got-moves/Non-local-operator-techniques-in-many-body-physics/blob/main/Exact_boson_though_ansatz/Moving_towards_expectation_value__The_guess_solution_trial_6.pdf).

## End Result
We weren't successful in this approach. There is a violation of area law of entanglement entropy. 
### Entanglement Entropy Violation

True fermionic ground states obey an area law with logarithmic corrections $S_A \sim L \log L$ (1D) or surface area times log terms (higher D) due to finite Fermi surface, where distant modes decouple.

The sea boson approximation treats excitations as free/local bosons, implying strict area law $S_A \sim$ boundary.

Inserting back into fermionic bilinears $c^\dagger_{p+q_2} c_{p+q_2}$ generates volume-law entanglement $S_A \sim |A|$ from delocalized bosonic correlations across the subsystem.

