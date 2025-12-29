# Derivations of Fermion as a Non-Local Particle–Hole Excitation

## Motivation
The purpose of this folder is to provide a detailed, step-by-step derivation that supports and expands the paper **“Fermion as a non-local particle-hole excitation”** ([arXiv:2501.06489](https://arxiv.org/html/2501.06489v1)). The goal is to make the technical path explicit and reproducible, from the Hamiltonian formulation to the closed-form Green’s function obtained from non-local operator methods.

## Content
This folder collects materials that walk through the derivation and supporting calculations:
- **LaTeX sources** for derivations, including the construction of non-local operators and their algebraic identities.
- **Supplementary notes** that clarify intermediate steps and assumptions used in the derivation.
- **Auxiliary calculations** that connect the equations of motion to the resulting Green’s functions.

## Workflow
1. **Writing the Hamiltonian in terms of the Sea bosons.**
2. **Finding the equations of motion.**
3. **Constructing the respective four-point functions** we get from resolving the identity of nonlocal operators.
4. **Substituting in the equation of motion and solving it.** Rearranging the terms in order to obtain a $\partial_{\lambda/\lambda'}$ by summing (inverse of Wick’s theorem).
5. **Solving the first-order coupled differential equation** using the variable separable technique in $\lambda$ and $\lambda'$, which allows us to obtain the Green’s function by setting $\lambda$ and $\lambda'$ to 0.

## Results
Following the workflow above yields an explicit form of the Green’s function in terms of non-local particle–hole operators. The derivation demonstrates how the equations of motion and the structure of the four-point functions combine to reproduce the fermionic propagator, validating the non-local operator framework presented in the paper.

## Conclusion
This folder serves as a complete derivation companion to the paper, emphasizing the operational steps needed to pass from the Sea-boson Hamiltonian to the Green’s function. It highlights how the non-local operator resolution and inverse Wick-like summations produce a consistent, closed-form description of fermionic excitations as non-local particle–hole modes.
