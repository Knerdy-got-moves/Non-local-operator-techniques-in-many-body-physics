# Non-Local Operator Techniques in Many-Body Physics

[![arXiv](https://img.shields.io/badge/arXiv-2501.06489-b31b1b.svg)](https://arxiv.org/abs/2501.06489)

> **A Dimension-Agnostic Approach to Interacting Fermi Systems via Sea-Boson Operators**

This repository documents the theoretical development of a novel technique for computing Green's functions in many-body quantum systems using non-local particle–hole operators. The work culminates in our preprint: [*Fermions as a Non-Local Particle–Hole Excitation*](https://arxiv.org/abs/2501.06489).

---

## Table of Contents

1. [Research Motivation](#research-motivation)
2. [Historical Background](#historical-background)
3. [Repository Structure](#repository-structure)
4. [Research Narrative](#research-narrative)
   - [Phase I: Foundations](#phase-i-foundations)
   - [Phase II: Exploratory Approaches](#phase-ii-exploratory-approaches)
   - [Phase III: The Non-Local Operator Framework](#phase-iii-the-non-local-operator-framework)
5. [Key Mathematical Constructs](#key-mathematical-constructs)
6. [Main Results](#main-results)
7. [Future Directions](#future-directions)
8. [References](#references)
9. [Acknowledgements](#acknowledgements)

---

## Research Motivation

The central challenge in condensed matter physics is understanding the behaviour of **interacting many-body systems**. While exact solutions exist in one dimension through techniques like bosonization and the Bethe ansatz, extending these methods to higher dimensions remains a fundamental open problem.

**Our goal**: Develop a *dimension-agnostic* formalism that captures the essential physics of interacting Fermi systems without being restricted to one spatial dimension.

The key insight driving this work is that fermions can be viewed as **non-local particle–hole excitations** above a filled Fermi sea. By systematically exploiting this perspective through "sea-boson" operators, we construct a framework where:

- The kinetic energy becomes quadratic in bosonic variables
- Density–density interactions have a natural representation
- Green's functions can be computed through controlled approximations (RPA-like expansions)

This repository presents the complete journey—from foundational concepts through unsuccessful attempts to the final successful formulation.

---

## Historical Background

The theoretical foundations of this work draw from a rich history of developments in many-body physics:

### Bosonization and Luttinger Liquids

The idea of representing fermionic systems in terms of bosonic degrees of freedom has its origins in **Tomonaga's (1950)** treatment of one-dimensional electron systems and was further developed by **Luttinger (1963)** and **Mattis & Lieb (1965)**. The modern bosonization framework, systematized by **Haldane (1981)**, provides exact solutions for 1D interacting fermions but relies fundamentally on the peculiarities of one-dimensional kinematics.

### Higher-Dimensional Extensions

Attempts to extend bosonization beyond 1D include:

- **Luther (1979)**: Early attempts at 2D bosonization
- **Houghton & Marston (1993)**: Bosonization of the Fermi surface
- **Castro Neto & Fradkin (1994)**: Higher-dimensional bosonization schemes
- **Kopietz, Hermisson & Schönhammer (1995)**: Functional bosonization approaches

### The Sea-Displacement Formalism

The specific operator framework we employ was developed by **Setlur and Chang (1998)** in their seminal work on exactly solvable models of Bose and Fermi liquids. This formalism introduces *sea-displacement operators* that encode particle–hole excitations while preserving the correct fermionic statistics at the operator level. The systematic development of this approach is documented in:

> **G. S. Setlur**, *Dynamics of Classical and Quantum Fields: An Introduction*, CRC Press (2014)

Our work extends this framework by introducing the **resolution of identity** for non-local operators, enabling exact computation of Green's functions in a controlled manner.

---

## Repository Structure

```
Non-local-operator-techniques-in-many-body-physics/
│
├── README.md                                          ← You are here
│
├── New_technique_to_study_many_body_physics_using_non_local_operators/
│   ├── ReportREADME.md                               ← Overview of foundational report
│   ├── Chapter3.tex                                  ← Core derivations and algebra
│   └── [Additional chapters and compiled PDF]
│
├── Definitions_of_Sea_bosons_and_Free_particle_Hamiltonian/
│   ├── DefREADME.md                                  ← Notation and definitions guide
│   └── cs in terms of as.tex                         ← Sea-boson operator definitions
│
├── SRPA_vs_GRPA/
│   ├── ApproxREADME.md                               ← Approximation scheme comparison
│   └── ExactBosons.tex                               ← SRPA/GRPA derivations
│
├── Exact_boson_though_ansatz/
│   ├── AnsatzREADME.md                               ← Ansatz approach (unsuccessful)
│   └── Moving_towards_expectation_value__The_guess_solution_trial_6.pdf
│
├── Exact_bosons_though_iterative_methods/
│   ├── IterativeREADME.md                            ← Iterative expansion approach
│   └── ExponAKQ (1).tex                              ← Iterative derivations
│
├── Random_solution_trials/
│   └── RandomREADME.md                               ← Exploratory trials (unsuccessful)
│
├── Derivations_of_fermion_as_a_non_local_particle_hole_excitation/
│   ├── DerivationREADME.md                           ← ArXiv paper derivations
│   └── [Detailed step-by-step calculations]
│
└── Free_theory_Green_s_function_using_trace/
    ├── VerifyREADME.md                               ← Verification against exact results
    └── [Verification calculations]
```

### Quick Navigation by Topic

| Topic | Primary Location | Description |
|-------|------------------|-------------|
| **Foundations & Notation** | [Definitions/](Definitions_of_Sea_bosons_and_Free_particle_Hamiltonian/) | Sea-boson definitions, Hamiltonian rewriting |
| **Second Quantization** | [New_technique/.../Chapter3.tex](New_technique_to_study_many_body_physics_using_non_local_operators/Chapter3.tex) | Non-local particle-hole creation operators |
| **Approximation Schemes** | [SRPA_vs_GRPA/](SRPA_vs_GRPA/) | RPA variants, physical justification |
| **Failed Approaches** | [Exact_boson_though_ansatz/](Exact_boson_though_ansatz/), [Random_solution_trials/](Random_solution_trials/) | Documented unsuccessful attempts |
| **Successful Method** | [Derivations/.../](Derivations_of_fermion_as_a_non_local_particle_hole_excitation/) | Non-local operator resolution technique |
| **Verification** | [Free_theory_Green_s_function/](Free_theory_Green_s_function_using_trace/) | Exact solution comparison |

---

## Research Narrative

The development of this work followed a systematic exploration of multiple approaches before arriving at the successful non-local operator technique. This section documents that journey.

### Phase I: Foundations

#### Learning Second Quantization

The research began with a thorough study of the second quantization formalism, documented in the report [*New Techniques to Study Many-Body Physics Using Non-Local Operators*](New_technique_to_study_many_body_physics_using_non_local_operators/ReportREADME.md).

**Key concepts established:**
- Occupation number representation and Fock space
- Bosonic and fermionic creation/annihilation operators
- Commutation and anti-commutation relations

#### Defining Sea-Boson Operators

Following Setlur and Chang (1998), we introduced the fundamental operators:

**Projected fermionic operators** (at T = 0):
```
c†_{p,<} = n_F(p) c†_p       (creates fermion below Fermi level)
c†_{p,>} = (1-n_F(p)) c†_p   (creates fermion above Fermi level)
```

**Sea-boson operators:**
```
a†_p(q) = c†_{p+q/2,>} c_{p-q/2,<}   (creates particle-hole pair)
```

**Sea-displacement operators:**
```
A_k(q) = c†_{k-q/2,<} (1/√N_>) c_{k+q/2,>}
```

These definitions allow rewriting the kinetic energy in a quadratic bosonic form:

$$\text{KE} = \sum_{\mathbf{p}} \frac{|\mathbf{p}|^2}{2m} n_F(\mathbf{p}) + \sum_{\mathbf{k},\mathbf{q}} \frac{\mathbf{k} \cdot \mathbf{q}}{m} A^\dagger_{\mathbf{k}}(\mathbf{q}) A_{\mathbf{k}}(\mathbf{q})$$

*See:* [Definitions folder](Definitions_of_Sea_bosons_and_Free_particle_Hamiltonian/DefREADME.md) for complete notation.

#### SRPA vs GRPA Approximations

A critical decision point was choosing the appropriate commutation approximation for sea-boson operators.

**Exact commutator:**
$$[a_{\mathbf{k}}(\mathbf{q}), a^\dagger_{\mathbf{k}'}(\mathbf{q}')] = n_{\mathbf{k}'-\mathbf{q}'/2,<} \delta_{\mathbf{k}+\mathbf{q}/2, \mathbf{k}'+\mathbf{q}'/2} - n_{\mathbf{k}+\mathbf{q}/2,>} \delta_{\mathbf{k}-\mathbf{q}/2, \mathbf{k}'-\mathbf{q}'/2}$$

**Simple RPA (SRPA):**
$$[a_{\mathbf{k}}(\mathbf{q}), a^\dagger_{\mathbf{k}'}(\mathbf{q}')] = \delta_{\mathbf{k},\mathbf{k}'} \delta_{\mathbf{q},\mathbf{q}'} n_F(\mathbf{k}-\mathbf{q}/2)(1-n_F(\mathbf{k}+\mathbf{q}/2))$$

**Generalized RPA (GRPA):**
$$[a_{\mathbf{k}}(\mathbf{q}), a^\dagger_{\mathbf{k}'}(\mathbf{q}')] = \delta_{\mathbf{k},\mathbf{k}'} \delta_{\mathbf{q},\mathbf{q}'} n_F(\mathbf{k}-\mathbf{q}/2)(1-n_F(\mathbf{k}+\mathbf{q}/2))(n_{\mathbf{k}-\mathbf{q}/2} - n_{\mathbf{k}+\mathbf{q}/2})$$

Through careful analysis of nested commutators (documented in [SRPA_vs_GRPA/](SRPA_vs_GRPA/ApproxREADME.md)), we demonstrated that **GRPA is self-consistent** while SRPA leads to contradictions. This finding was crucial for subsequent developments.

*Physical interpretation:* GRPA accounts for fluctuations in the number of particle–hole pairs self-consistently, which is essential for recovering the correct Fermi–Dirac distribution.

---

### Phase II: Exploratory Approaches

With the foundational framework established, we explored several routes toward expressing fermionic operators exactly in terms of sea-bosons.

#### Approach 1: Ansatz Method

**Goal:** Find an exact mapping from fermionic field operators to sea-boson operators.

**Method:** Proposed ansätze of the form:
$$c^\dagger_{p+q_2} = e^{iN_p q_2} c^\dagger_{p+q_2}(1 - n_{p+q_2}) + \cdots$$

with phase factors ensuring correct time evolution.

**Result:** ❌ **Unsuccessful**

**Reason:** The ansatz violated the **area law of entanglement entropy**.

> *True fermionic ground states obey an area law with logarithmic corrections: S_A ~ L log L (1D). The sea-boson approximation, treating excitations as local bosons, implied strict area law S_A ~ boundary. Reinserting into fermionic bilinears generated volume-law entanglement, which is unphysical.*

*See:* [Exact_boson_though_ansatz/](Exact_boson_though_ansatz/AnsatzREADME.md)

#### Approach 2: Iterative Methods

**Goal:** Build exact fermionic operators through iterative expansions in sea-boson operators.

**Method:** Systematic expansion of exponentials involving sea-boson operators, with verification of commutator consistency at each order.

**Result:** ❌ **Unsuccessful**

**Reason:** Commutator approximations (even GRPA) introduced inconsistencies that **amplified across iterations**. Higher-order terms accumulated errors that destroyed the bosonic structure.

*See:* [Exact_bosons_though_iterative_methods/](Exact_bosons_though_iterative_methods/IterativeREADME.md)

#### Approach 3: Random Solution Trials

**Goal:** Identify operators that exactly commute when constructed from fermionic operators.

**Method:** Exploratory calculations probing whether near-commutativity of sea-bosons could yield exactly commuting operators.

**Result:** ❌ **Unsuccessful**

**Reason:** Insufficient constraints led to a **stiff problem** with no consistent solution.

*See:* [Random_solution_trials/](Random_solution_trials/RandomREADME.md)

---

### Phase III: The Non-Local Operator Framework

The breakthrough came from a shift in perspective: rather than trying to express fermionic operators exactly in terms of sea-bosons, we recognized that **the bosonic nature manifests at the level of distributions** (expectation values).

#### Key Insight: Resolution of Identity

Instead of operator-level bosonization, we introduced a **resolution of identity** involving non-local operators. This allowed us to:

1. Write equations of motion for Green's functions
2. Construct four-point functions from the resolution of identity
3. Derive coupled differential equations in auxiliary parameters (λ, λ')
4. Solve these equations using separation of variables

#### The Workflow

The successful method follows this systematic procedure:

```
┌─────────────────────────────────────────────────────────────────┐
│  STEP 1: Write Hamiltonian in Sea-Boson Language                │
│          H = KE(A†A) + V(density-density interactions)          │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│  STEP 2: Derive Equations of Motion                             │
│          Using Heisenberg picture for sea-boson operators       │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│  STEP 3: Construct Four-Point Functions                         │
│          Via resolution of identity for non-local operators     │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│  STEP 4: Substitute and Rearrange                               │
│          Obtain ∂_λ/λ' structure (inverse Wick's theorem)       │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│  STEP 5: Solve Differential Equations                           │
│          Variable separation in λ and λ'                        │
│          Set λ = λ' = 0 to obtain Green's function              │
└─────────────────────────────────────────────────────────────────┘
```

*See:* [Derivations/.../DerivationREADME.md](Derivations_of_fermion_as_a_non_local_particle_hole_excitation/DerivationREADME.md)

#### Verification

We applied this workflow to the **free particle case** and verified all resulting equations against the exact Green's function computed via trace methods.

**Key finding:** The trace-based calculation revealed a *systematic cancellation structure* that aligns precisely with the constraints imposed by our differential equations. This internal consistency provides strong evidence for the correctness of the framework.

*See:* [Free_theory_Green_s_function/](Free_theory_Green_s_function_using_trace/VerifyREADME.md)

---

## Key Mathematical Constructs

### The Correlation Function

The central object is the finite-temperature correlation function:

$$G(\mathbf{k}, \mathbf{q}; \lambda) = \langle e^{-\lambda N_>} a^\dagger_{\mathbf{k}}(\mathbf{q}) a_{\mathbf{k}}(\mathbf{q}) \rangle \equiv \frac{\text{Tr}(e^{-\beta(H-\mu N)} e^{-\lambda N_>} a^\dagger_{\mathbf{k}}(\mathbf{q}) a_{\mathbf{k}}(\mathbf{q}))}{\text{Tr}(e^{-\beta(H-\mu N)})}$$

The auxiliary parameter λ serves as a generating function; physical observables are recovered at λ = 0.

### Momentum Distribution

The momentum distribution is expressed as:

$$\langle \hat{n}_{\mathbf{k},\lambda} \rangle = n_F(\mathbf{k}) \langle e^{-\lambda N_>} \rangle - \sum_{\mathbf{q}} \int_\infty^\lambda d\lambda' G(\mathbf{k}-\mathbf{q}/2, \mathbf{q}; \lambda') + \sum_{\mathbf{q}} \int_\infty^\lambda d\lambda' G(\mathbf{k}+\mathbf{q}/2, \mathbf{q}; \lambda')$$

### Recovery of Fermi–Dirac Distribution

Using GRPA and the cyclic property of the trace, we derive coupled differential equations whose solution yields:

$$\tilde{n}_{>,<}(0, \varepsilon) = \frac{1}{e^{\beta(\varepsilon - \mu)} + 1}$$

This remarkable result demonstrates that the **Fermi–Dirac distribution emerges from a theory that is bosonic in character**, provided the approximation (GRPA) correctly accounts for particle–hole pair fluctuations.

---

## Main Results

1. **GRPA is the consistent approximation** for sea-boson commutators; SRPA leads to internal contradictions.

2. **Direct bosonization of fermionic operators fails** due to entanglement entropy constraints (area law violation).

3. **The non-local operator framework with resolution of identity** provides a viable route to exact Green's functions.

4. **The free-particle Green's function** computed via this method matches exactly with trace-based calculations.

5. **The Fermi–Dirac distribution** is recovered from the bosonic formalism when GRPA is employed.

These results are presented in our preprint:

> **R. P. Joshi and G. S. Setlur**, *Fermions as a Non-Local Particle–Hole Excitation*, [arXiv:2501.06489](https://arxiv.org/abs/2501.06489) (2025).

---

## Future Directions

1. **Interacting systems:** Extend the workflow to include density–density interactions and compute the interacting Green's function.

2. **Higher dimensions:** Apply the dimension-agnostic formalism to 2D and 3D Fermi systems.

3. **Collective modes:** Use the framework to study plasmons, zero sound, and other collective excitations.

4. **Superconductivity:** Investigate whether the formalism can capture pairing instabilities and BCS-like physics.

5. **Non-equilibrium:** Extend to Keldysh formalism for time-dependent phenomena.

---

## References

### Primary Sources

1. **G. S. Setlur and Y.-C. Chang**, *Single-particle Green functions in exactly solvable models of Bose and Fermi liquids*, Phys. Rev. B (1998).

2. **G. S. Setlur**, *Dynamics of Classical and Quantum Fields: An Introduction*, CRC Press (2014).

3. **R. P. Joshi and G. S. Setlur**, *Fermions as a Non-Local Particle–Hole Excitation*, [arXiv:2501.06489](https://arxiv.org/abs/2501.06489) (2025).

### Historical Background

4. **S. Tomonaga**, *Remarks on Bloch's Method of Sound Waves applied to Many-Fermion Problems*, Prog. Theor. Phys. **5**, 544 (1950).

5. **J. M. Luttinger**, *An Exactly Soluble Model of a Many-Fermion System*, J. Math. Phys. **4**, 1154 (1963).

6. **D. C. Mattis and E. H. Lieb**, *Exact Solution of a Many-Fermion System and Its Associated Boson Field*, J. Math. Phys. **6**, 304 (1965).

7. **F. D. M. Haldane**, *'Luttinger liquid theory' of one-dimensional quantum fluids*, J. Phys. C **14**, 2585 (1981).

8. **A. Houghton and J. B. Marston**, *Bosonization and fermion liquids in dimensions greater than one*, Phys. Rev. B **48**, 7790 (1993).

9. **A. H. Castro Neto and E. Fradkin**, *Bosonization of the low energy excitations of Fermi liquids*, Phys. Rev. Lett. **72**, 1393 (1994).

10. **P. Kopietz, J. Hermisson, and K. Schönhammer**, *Bosonization of interacting fermions in arbitrary dimension beyond the Gaussian approximation*, Phys. Rev. B **52**, 10877 (1995).

---

## Acknowledgements

This research was conducted under the guidance of **Prof. Girish Sampath Setlur** at the Indian Institute of Technology Guwahati. Many of the derivations in this repository were developed by Prof. Setlur and verified by the author under his guidance.

---

## Contact

**R. P. Joshi**  
National Institute of Science Education and Research, Bhubaneswar  
Email: [rishi.joshi@niser.ac.in]

---

*Last updated: December 2024*
