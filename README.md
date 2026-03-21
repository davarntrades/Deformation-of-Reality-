<div align="center">

# Topological Deformation as a Condition for Reality in Dynamical Systems: A Reachability-Based Definition of Truth

**Davarn Morrison**

*Independent Research · 2026*

![Type](https://img.shields.io/badge/Type-Formal_Paper-0075ca?style=flat-square)
![Field](https://img.shields.io/badge/Field-Dynamical_Systems_·_Topology-0075ca?style=flat-square)
![Contribution](https://img.shields.io/badge/Contribution-Geometric_Truth_Condition-8b0000?style=flat-square)
![Status](https://img.shields.io/badge/Status-Submission_Ready-2d6a2e?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![©](https://img.shields.io/badge/©_Davarn_Morrison-555555?style=flat-square)

</div>

-----

## Abstract

Conventional accounts of truth are typically framed in linguistic, logical, or probabilistic terms, describing correspondence between statements and reality. Such formulations operate at the level of representation rather than system dynamics. This paper proposes a structural alternative: truth is defined as a topological deformation of the system’s reachable state space. We formalise this condition using homology, showing that a system encounters reality when the topology of its reachable set changes. This distinguishes genuine structural change from internal rearrangement or representation updates. The result provides a geometric definition of truth, independent of language, grounded in reachability theory and dynamical systems.

-----

## 1. Introduction

Truth is traditionally defined as correspondence between a proposition and the world. In artificial intelligence and cognitive systems, this notion is operationalised through prediction accuracy, consistency, or agreement. However, these approaches evaluate outputs or representations rather than the underlying system dynamics that generate them.

This paper argues that such definitions are incomplete. A system may update its representations, change its outputs, or improve predictions without undergoing any structural change in what it can become. Conversely, a system may undergo a fundamental shift in its space of possible futures even if its outputs appear superficially unchanged.

To capture this distinction, we propose a dynamical definition of truth based on reachability [Mitchell et al., 2005; Blanchini, 1999]. Instead of evaluating statements, we evaluate transformations of the system’s reachable state space. Truth is identified not by correctness of representation, but by structural change in possibility.

-----

## 2. Dynamical Systems and Reachability

Let a system evolve over a state space `X` under dynamics:

|Equation               |Components                                        |
|:---------------------:|:------------------------------------------------:|
|`x_{t+1} = F(x_t, u_t)`|`x_t ∈ X` system state, `u_t ∈ 𝒰` admissible input|

The forward reachable set from initial condition `x₀` is:

|Symbol|Definition                          |Meaning                                                   |
|:----:|:----------------------------------:|:--------------------------------------------------------:|
|`ℛ(t)`|`{ x(t) ∈ X | x(0) = x₀, u(·) ∈ 𝒰 }`|All states the system can attain under admissible dynamics|

This set encodes not only what the system does, but what it can become. Reachability is the minimal object that encodes all possible trajectories of a dynamical system, and therefore subsumes behaviour, representation, and capability as projections. We treat `ℛ(t)` as the primary object of analysis.

-----

## 3. Structural vs Representational Change

We distinguish between two classes of change:

### 3.1 Representational Change

A system updates internal variables or outputs without altering its reachable set:

|Condition      |Meaning                |
|:-------------:|:---------------------:|
|`ℛ(t₁) = ℛ(t₂)`|Reachable set unchanged|

Such changes include belief updates, parameter adjustments, output variation, and symbolic recombination. These operations may alter representation but do not change the structure of possible futures.

### 3.2 Structural Change

A system undergoes structural change when its reachable set is altered:

|Condition      |Meaning                                                                                |
|:-------------:|:-------------------------------------------------------------------------------------:|
|`ℛ(t₁) ≠ ℛ(t₂)`|Reachable set changed — new states accessible, old states lost, or connectivity altered|

Structural change affects the geometry of possibility itself.

-----

## 4. Topological Deformation of Reachable Sets

To detect structural change at a fundamental level, we consider topological invariants of the reachable set. Let `H_k(ℛ(t))` denote the k-th homology group of `ℛ(t)`, capturing its connectivity and hole structure [Carlsson, 2009].

**Definition (Topological Reality Condition).** A system encounters reality if:

|Condition                    |Equation                          |
|:---------------------------:|:--------------------------------:|
|Topological Reality Condition|`∃k ≥ 0 : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`|

|Symbol  |Meaning                                                                 |
|:------:|:----------------------------------------------------------------------:|
|`t₁, t₂`|Two time points — before and after interaction                          |
|`H_k(·)`|k-th homology group — measures connectivity, holes, voids at dimension k|
|`k ≥ 0` |Topological dimension index                                             |
|`≇`     |Non-isomorphic as abelian groups — structurally different               |

**Interpretation.** Homology change implies the reachable sets are not topologically equivalent. No continuous deformation maps one to the other. The structure of possible futures has fundamentally changed.

-----

## 5. Truth as Structural Deformation

**Definition (Truth).** Truth corresponds to structural change in the reachable set, with topological deformation providing a sufficient condition:

|Definition|Equation                          |
|:--------:|:--------------------------------:|
|Truth     |`∃k ≥ 0 : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`|

**Clarification.** Topological change is a strong signal of structural transformation. However, homology is coarse — it detects holes and connectivity but does not capture all geometric deformation. Metric deformation without homology change may still represent weaker forms of structural change. Thus topological change is a sufficient condition for truth, not strictly necessary for all forms of meaningful change. Finer-grained detection may employ persistent homology [Carlsson, 2009] or Riemannian metrics on ℛ.

-----

## 6. Illusion vs Reality

The framework provides a geometric distinction:

|Type    |Condition                          |Interpretation                                  |
|:------:|:---------------------------------:|:----------------------------------------------:|
|Illusion|`H_k(ℛ(t₁)) ≅ H_k(ℛ(t₂))` for all k|Internal rearrangement without structural change|
|Reality |`∃k : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`     |Structural deformation of possibility           |

A system may process information indefinitely without encountering reality if its reachable structure remains unchanged. Information arrives. The topology does not move. The system updated internally but did not register reality.

**Structural Interpretation of Reality.** We interpret reality as the source of constraints that cannot be absorbed by internal reparameterisation of the system. Formally, an interaction corresponds to reality if it induces a transformation of the reachable set that is not homotopy-equivalent to its prior configuration. Internal updates that preserve the topology of `ℛ(t)` constitute representational change, while interactions that alter its topological invariants constitute structural encounters with reality. Reality is therefore defined operationally: it is the class of constraints that forces deformation not producible by internal dynamics alone.

-----

## 7. Relation to Basin Escape

Let `B ⊂ X` be a basin of attraction.

|Condition              |Equation                      |What It Detects                           |
|:---------------------:|:----------------------------:|:----------------------------------------:|
|Basin escape           |`ℛ(t₂) ⊄ B`                   |Leaving a region of state space           |
|Topological deformation|`∃k : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`|Changing the structure of the space itself|

The relationship between them:

|Direction                             |Holds?         |Meaning                                                      |
|:------------------------------------:|:-------------:|:-----------------------------------------------------------:|
|Topological deformation ⟹ basin escape|Yes            |If the topology changed, the system must have left some basin|
|Basin escape ⟹ topological deformation|Not necessarily|A system can leave a basin without changing the topology of ℛ|

Topological deformation is the stronger condition. Basin escape is necessary but not sufficient for structural truth.

-----

## 8. Implications

### 8.1 Independence from Language

Let outputs be given by `y_t = π(x_t)`. Language operates on `y_t`, while structure resides in `x_t`.

|Observation                                              |Consequence                                                     |
|:-------------------------------------------------------:|:--------------------------------------------------------------:|
|Language may change without structural change            |Fluent output does not imply truth was encountered              |
|Structural change may occur without linguistic difference|Truth may arrive silently — the topology moved, the words didn’t|

Truth is therefore not a property of statements, but of state-space transformation.

### 8.2 Limits of Behavioural Evaluation

Behavioural metrics evaluate outputs rather than reachable structure. As a result, systems may appear to learn without structural change, and apparent improvement may correspond to internal rearrangement. Evaluation based on outputs cannot detect whether a system has encountered truth — it can only detect whether the system’s projection changed, which is a weaker condition.

### 8.3 Connection to Intelligence

|Property       |Equation                               |Effect on ℛ   |
|:-------------:|:-------------------------------------:|:------------:|
|Intelligence   |`I(t) = d/dt μ(ℛ(t))` [Morrison, 2026b]|Expands ℛ     |
|Truth / Reality|`∃k : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`         |Restructures ℛ|

Intelligence explores — it expands the space of reachable futures. Reality reshapes — it deforms the structure of that space. They act on the same object `ℛ(t)` in different ways. A system can be intelligent without encountering truth (expanding within a fixed topology). A system can encounter truth without being intelligent (deformed by external constraint while static). Both acting together — expansion and structural deformation — characterises a system that is growing in contact with reality.

-----

## 9. Discussion

The proposed definition shifts truth from a semantic to a geometric domain. It replaces correspondence between statements and reality with structural transformation of reachable state space.

The framework is compatible with reachability theory [Mitchell et al., 2005], invariant set analysis [Blanchini, 1999], and topological data analysis [Carlsson, 2009]. Its contribution lies in identifying topological deformation of reachable sets as the defining condition for truth — applying existing mathematical tools to a question traditionally addressed through logic and language.

**Limitations.** The definition is structural, not computational; practical systems may use approximations (e.g., reachable over-approximations or persistent homology) while preserving the logical form of the condition. Homology is coarse as a topological descriptor and may miss metric deformations that carry meaningful information. Persistent homology offers finer resolution but at greater computational cost. The definition provides a sufficient condition for truth, not a complete characterisation of all forms of meaningful change.

-----

## 10. Conclusion

We presented a reachability-based definition of truth as topological deformation of the system’s reachable state space:

**∃k ≥ 0 : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))**

This distinguishes structural change from representational change and provides a geometric criterion for when a system encounters reality.

*Truth is not what is said or represented. It is what changes the structure of possible futures.*

*Reality is that which forces a topological deformation of the reachable set.*

-----

## References

|Citation                    |Work                                                                        |Relevance                                                   |
|:--------------------------:|:--------------------------------------------------------------------------:|:----------------------------------------------------------:|
|Blanchini, F. (1999)        |*Set Invariance in Control.* Automatica, 35(11).                            |Invariant set methods                                       |
|Carlsson, G. (2009)         |*Topology and Data.* Bulletin of the AMS, 46(2).                            |Topological data analysis — homology for structure detection|
|Mitchell, I.M. et al. (2005)|*Hamilton-Jacobi Reachability.* IEEE TAC.                                   |Reachable set computation                                   |
|Morrison, D. (2026a)        |*Geometric Control Theory of Cognition.* Independent Research.              |Base framework                                              |
|Morrison, D. (2026b)        |*Computable Intelligence via Reachable Set Expansion.* Independent Research.|Intelligence as `d/dt μ(ℛ)`                                 |
|Shannon, C.E. (1948)        |*A Mathematical Theory of Communication.* Bell System TJ.                   |Information-theoretic foundations                           |

-----

## Citation

```
Morrison, D. (2026). Topological Deformation as a Condition
for Reality in Dynamical Systems: A Reachability-Based
Definition of Truth. Independent Research.
UK Patent Applications: GB2600765.8, GB2602013.1,
GB2602072.7, GB26023332.5.
```

**BibTeX:**

```bibtex
@misc{morrison2026truth,
  author       = {Morrison, Davarn},
  title        = {Topological Deformation as a Condition for Reality in
                  Dynamical Systems: A Reachability-Based Definition of Truth},
  year         = {2026},
  publisher    = {Independent Research},
  note         = {UK Patent Applications: GB2600765.8, GB2602013.1,
                  GB2602072.7, GB26023332.5},
  url          = {https://github.com/davarn/morrison-framework}
}
```

-----

Topological Deformation as a Condition for Reality · Morrison Framework™ · Geometric Control Theory of Cognition

GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5

© 2026 Davarn Morrison — All Rights Reserved

-----

## Related Work

- [Truth and Reality — Teachable Version](https://github.com/davarn/morrison-framework) — Visual explanation of the truth condition
- [Basin Escape and Structural Creativity](https://github.com/davarn/morrison-framework) — Learning as basin escape
- [Computable Intelligence via Reachable Set Expansion](https://github.com/davarn/morrison-framework) — Intelligence defined operationally
- [Geometry as the Substrate of Intelligence](https://github.com/davarn/morrison-framework) — Why reachability is the correct object
- [Geometric Control Theory of Cognition](https://github.com/davarn/morrison-framework) — The base theory
- [Licensing, Citation, and IP](https://github.com/davarn/morrison-framework) — How to cite and licence
