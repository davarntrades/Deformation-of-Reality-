<div align="center">

# Dissonance and Structural Truth: A Reachability-Based Model of Cognitive Instability and Topological Change

**Davarn Morrison**

*Independent Research · 2026*

![Type](https://img.shields.io/badge/Type-Formal_Paper-0075ca?style=flat-square)
![Field](https://img.shields.io/badge/Field-Cognitive_Dynamics_·_Topology-0075ca?style=flat-square)
![Contribution](https://img.shields.io/badge/Contribution-Dissonance_as_Geometric_Mismatch-8b0000?style=flat-square)
![Status](https://img.shields.io/badge/Status-Submission_Ready-2d6a2e?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![©](https://img.shields.io/badge/©_Davarn_Morrison-555555?style=flat-square)

</div>

-----

## Abstract

Cognitive dissonance is commonly treated as a psychological phenomenon arising from conflicting beliefs or information. This paper provides a structural reinterpretation: dissonance is a measurable incompatibility between a system’s current reachable set and constraints imposed by new input or experience. We define a metric of dissonance intensity based on geometric and topological mismatch, and formalise the probability that such dissonance results in deformation of the reachable set. We further define ignorance as the inability to estimate or modify reachable structure. We show that dissonance is a necessary but non-sufficient boundary condition for structural intelligence, while topological deformation provides a sufficient condition for structural truth, capturing qualitative changes in reachable structure.

-----

## 1. Introduction

Intelligent systems encounter contradictions between internal models and external reality. Traditional frameworks interpret these contradictions at the level of representation — conflicting beliefs, inconsistent information, mismatched predictions. However, representational inconsistency does not imply structural change [Morrison, 2026a].

This paper proposes a reachability-based formulation: dissonance occurs when incoming constraints cannot be reconciled within the current reachable set; resolution occurs either through representational adjustment or structural deformation; truth is registered only in the latter case [Morrison, 2026b].

We formalise these distinctions and provide measurable quantities for each.

-----

## 2. Preliminaries

Let a system evolve over state space `X`:

|Equation               |Components                                        |
|:---------------------:|:------------------------------------------------:|
|`x_{t+1} = F(x_t, u_t)`|`x_t ∈ X` system state, `u_t ∈ 𝒰` admissible input|

With reachable set:

|Symbol|Definition                          |
|:----:|:----------------------------------:|
|`ℛ(t)`|`{ x(t) ∈ X | x(0) = x₀, u(·) ∈ 𝒰 }`|

Truth condition [Morrison, 2026b]:

|Condition                         |Meaning                                  |
|:--------------------------------:|:---------------------------------------:|
|`∃k ≥ 0 : H_k(ℛ(t₁)) ≇ H_k(ℛ(t₂))`|Topology of the reachable set has changed|

**Assumptions.** The following are assumed throughout: (i) state space X is well-defined, (ii) reachable set `ℛ(t)` is measurable or approximable, (iii) homology groups `H_k` are computable or approximated via persistent homology, (iv) input transformations `Φ_t` are admissible.

-----

## 3. Dissonance as Structural Incompatibility

Let `Φ_t` denote a constraint or transformation induced by new input. Formally, `Φ_t : 𝒫(X) → 𝒫(X)` is a set transformation representing constraints or perturbations applied to reachable structure, mapping subsets of X to subsets of X while preserving system validity.

**Definition (Dissonance Intensity).**

|Symbol     |Formula               |Meaning                                                                          |
|:---------:|:--------------------:|:-------------------------------------------------------------------------------:|
|`D(t; Φ_t)`|`d_H(ℛ(t), Φ_t(ℛ(t)))`|Hausdorff distance between current reachable set and the set as deformed by input|

|Value    |Interpretation                                                        |
|:-------:|:--------------------------------------------------------------------:|
|`D ≈ 0`  |Input is structurally compatible — can be absorbed without change     |
|`D > 0`  |Input cannot be absorbed within current structure — geometric mismatch|
|Large `D`|Strong structural contradiction — significant incompatibility         |

Dissonance is a geometric mismatch between current possibility and imposed constraint. It is a measurable distance between two geometric objects. While the Hausdorff distance provides a natural geometric measure, alternative metrics (e.g. Wasserstein distance, energy distance, or task-specific divergences) may be used depending on system representation and computational constraints.

-----

## 4. Topological Dissonance

Define a discrete structural version:

|Symbol         |Formula                                            |
|:-------------:|:-------------------------------------------------:|
|`D_top(t; Φ_t)`|`Σ_{k=0}^{K} w_k · 𝟙[ H_k(ℛ(t)) ≇ H_k(Φ_t(ℛ(t))) ]`|

|Value      |Interpretation                                                                          |
|:---------:|:--------------------------------------------------------------------------------------:|
|`D_top = 0`|No structural contradiction — homology unchanged                                        |
|`D_top > 0`|At least one topological inconsistency — structure must change or input must be rejected|

This captures dissonance at the level of structure, not magnitude. Topological dissonance detects qualitative incompatibility — not how far the input pushes the manifold, but whether it pushes it into a different topological class.

Topological dissonance captures qualitative incompatibility. However, structural change may also occur at the metric level without altering homology. In such cases, `D(t) > 0` with `D_top = 0` indicates continuous deformation without topological transition — the shape changes but the connectivity does not.

-----

## 5. Resolution Dynamics

Dissonance does not imply change. It induces a bifurcation:

|Resolution|Effect on ℛ     |What Happens                                                           |
|:--------:|:--------------:|:---------------------------------------------------------------------:|
|Rejection |`ℛ(t)` preserved|System adjusts representation to absorb input without structural change|
|Acceptance|`ℛ(t)` deformed |System undergoes structural reconfiguration — topology changes         |

**Definition (Deformation Event).**

|Symbol      |Condition                        |
|:----------:|:-------------------------------:|
|`Def(t, Δt)`|`∃k : H_k(ℛ(t)) ≇ H_k(ℛ(t + Δt))`|

A deformation event occurs when the topology of the reachable set changes within the interval `[t, t + Δt]`. This is the formal registration of truth.

-----

## 6. Probability of Structural Deformation

Define the probability that dissonance results in deformation:

|Symbol        |Formula         |
|:------------:|:--------------:|
|`P_def(t, Δt)`|`Pr(Def(t, Δt))`|

Modelled as:

|Model  |Formula                          |
|:-----:|:-------------------------------:|
|`P_def`|`σ(α·D(t) + β·A(t) − γ·G(t) − θ)`|

where:

|Parameter|Meaning                       |Effect on P_def                                                       |
|:-------:|:----------------------------:|:--------------------------------------------------------------------:|
|`D(t)`   |Dissonance intensity          |`∂P_def/∂D > 0` — more dissonance increases probability of deformation|
|`A(t)`   |Adaptability / plasticity     |`∂P_def/∂A > 0` — more plasticity increases probability               |
|`G(t)`   |Rigidity / constraint strength|`∂P_def/∂G < 0` — more rigidity decreases probability                 |
|`σ`      |Sigmoid function              |Maps to [0, 1]                                                        |
|`θ`      |Threshold bias                |Baseline resistance to deformation                                    |

High dissonance and high plasticity make deformation likely. High rigidity makes deformation unlikely — the system absorbs the contradiction representationally without structural change. This provides a structural account of why some systems encounter truth (they deform) and others encounter the same input and remain unchanged (they reject).

**Grounding A(t) and G(t):**

|Parameter|Interpretation       |Example                                                            |
|:-------:|:-------------------:|:-----------------------------------------------------------------:|
|`A(t)`   |Structural plasticity|Learning rate, architecture flexibility, capacity for restructuring|
|`G(t)`   |Structural rigidity  |Constraints, regularisation, safety filters, governance strength   |

In practice, `P_def` may be estimated empirically via observed frequency of structural deformation events under repeated exposure to comparable dissonance conditions.

-----

## 7. Ignorance as Structural Inaccessibility

Ignorance is defined over reachable structure, not information.

### 7.1 Estimation Ignorance

|Symbol    |Formula          |Meaning                                                                   |
|:--------:|:---------------:|:------------------------------------------------------------------------:|
|`I_est(t)`|`d_H(ℛ̂(t), ℛ(t))`|Distance between the system’s internal estimate and the true reachable set|

A system that cannot accurately estimate its own reachable set does not know what it can become.

### 7.2 Modification Ignorance

|Symbol    |Formula             |Meaning                                    |
|:--------:|:------------------:|:-----------------------------------------:|
|`I_mod(t)`|`1 / (1 + cap_ℛ(t))`|Inverse of the system’s capacity to alter ℛ|

A system that cannot modify its own reachable set is structurally confined — regardless of how much information it possesses.

### 7.3 Total Ignorance

|Symbol    |Formula                        |
|:--------:|:-----------------------------:|
|`I_ign(t)`|`λ₁ · I_est(t) + λ₂ · I_mod(t)`|

A system is ignorant if it cannot accurately estimate `ℛ(t)`, cannot modify `ℛ(t)`, or both. Ignorance is not about what the system knows. It is about what the system can see and do at the structural level. Ignorance is independent of informational content: a system may possess accurate information while remaining structurally ignorant if it cannot estimate or modify `ℛ(t)`.

-----

## 8. Structural Interpretation

|Layer         |Object|What It Governs                      |
|:------------:|:----:|:-----------------------------------:|
|Representation|`π(x)`|Belief, perception, output           |
|Dissonance    |`D(t)`|Instability, tension, incompatibility|
|Structure     |`ℛ(t)`|Reality, possibility, identity       |

**Key Principle.** Dissonance quantifies structural incompatibility. Deformation resolves incompatibility at the level of possibility. Truth corresponds to realised structural change.

A system can experience dissonance indefinitely without encountering truth — if it resolves every contradiction representationally. Dissonance is the boundary condition. Deformation is the event. Truth is registered only when ℛ changes topology.

-----

## 9. Core Result

**Proposition.** Cognitive dissonance is a necessary but non-sufficient condition for structural intelligence.

|Property  |Status|Reason                                                                                         |
|:--------:|:----:|:---------------------------------------------------------------------------------------------:|
|Necessary |Yes   |Deformation requires prior incompatibility — without dissonance, there is no pressure to deform|
|Sufficient|No    |Dissonance may resolve without structural change — rejection preserves ℛ                       |

**Corollary.** `D(t) > 0` does not imply `Def(t, Δt)`. Dissonance does not guarantee truth. It creates the possibility for truth. Whether that possibility is realised depends on adaptability, rigidity, and the magnitude of the mismatch.

-----

## 10. Conclusion

We have formalised dissonance as geometric and topological incompatibility between the current reachable set and constraints imposed by new input, deformation as the mechanism of structural change, and ignorance as structural inaccessibility.

This yields a precise distinction:

*Cognitive dissonance marks the boundary at which structural intelligence becomes possible. Truth is registered only when the reachable set deforms.*

This framework applies directly to artificial systems, where dissonance corresponds to constraint violation, deformation to policy or model restructuring, and ignorance to limitations in estimating or modifying reachable behaviour.

-----

## References

|Citation                    |Work                                                                       |Relevance                  |
|:--------------------------:|:-------------------------------------------------------------------------:|:-------------------------:|
|Blanchini, F. (1999)        |*Set Invariance in Control.* Automatica, 35(11).                           |Invariant set methods      |
|Carlsson, G. (2009)         |*Topology and Data.* Bulletin of the AMS, 46(2).                           |Topological data analysis  |
|Mitchell, I.M. et al. (2005)|*Hamilton-Jacobi Reachability.* IEEE TAC.                                  |Reachable set computation  |
|Morrison, D. (2026a)        |*Geometric Control Theory of Cognition.* Independent Research.             |Base framework             |
|Morrison, D. (2026b)        |*Topological Deformation as a Condition for Reality.* Independent Research.|Truth as topological change|

-----

## Citation

```
Morrison, D. (2026). Dissonance and Structural Truth:
A Reachability-Based Model of Cognitive Instability
and Topological Change. Independent Research.
UK Patent Applications: GB2600765.8, GB2602013.1,
GB2602072.7, GB26023332.5.
```

**BibTeX:**

```bibtex
@misc{morrison2026dissonance,
  author       = {Morrison, Davarn},
  title        = {Dissonance and Structural Truth: A Reachability-Based Model
                  of Cognitive Instability and Topological Change},
  year         = {2026},
  publisher    = {Independent Research},
  note         = {UK Patent Applications: GB2600765.8, GB2602013.1,
                  GB2602072.7, GB26023332.5},
  url          = {https://github.com/davarn/morrison-framework}
}
```

-----

Dissonance and Structural Truth · Morrison Framework™ · Geometric Control Theory of Cognition

GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5

© 2026 Davarn Morrison — All Rights Reserved

-----

## Related Work

- [Topological Deformation as a Condition for Reality](https://github.com/davarn/morrison-framework) — Truth as topological change
- [Basin Escape and Structural Creativity](https://github.com/davarn/morrison-framework) — Learning as basin escape
- [Structural Power in Dynamical Systems](https://github.com/davarn/morrison-framework) — Control without manipulation
- [Computable Intelligence via Reachable Set Expansion](https://github.com/davarn/morrison-framework) — Intelligence defined operationally
- [Geometric Control Theory of Cognition](https://github.com/davarn/morrison-framework) — The base theory
- [Licensing, Citation, and IP](https://github.com/davarn/morrison-framework) — How to cite and licence
