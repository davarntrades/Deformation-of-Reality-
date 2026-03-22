<div align="center">

# Structural Power in Dynamical Systems: Control Without Manipulation via Reachability Constraints

**Davarn Morrison**

*Independent Research · 2026*

![Type](https://img.shields.io/badge/Type-Formal_Paper-0075ca?style=flat-square)
![Field](https://img.shields.io/badge/Field-Control_Theory_·_Structural_Analysis-0075ca?style=flat-square)
![Contribution](https://img.shields.io/badge/Contribution-Structural_Power_Principle-8b0000?style=flat-square)
![Status](https://img.shields.io/badge/Status-Submission_Ready-2d6a2e?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![©](https://img.shields.io/badge/©_Davarn_Morrison-555555?style=flat-square)

</div>

-----

## Abstract

Traditional notions of power are framed in terms of influence, persuasion, or control over behaviour. These accounts implicitly assume that systems must be acted upon to be directed. This paper proposes a structural alternative: power is not the ability to manipulate trajectories, but the configuration of the system’s reachable set. We show that when a system’s reachable set is constrained, its trajectories are determined without requiring intervention. This renders deception, persuasion, and continuous control unnecessary for systems whose reachable set is fixed. We formalise this principle and demonstrate that systems lacking access to their own reachable structure are automatically positioned within it. Power is therefore a property of geometry, not action.

-----

## 1. Introduction

Power is commonly understood as the capacity to influence or control the behaviour of others. In political theory, psychology, and artificial intelligence, this influence is typically modelled through mechanisms such as persuasion, incentives, or information transmission.

However, these approaches assume that behaviour must be actively shaped. They focus on how systems are acted upon, rather than how systems are structurally constrained.

This paper argues that such accounts are incomplete. A system does not need to be manipulated if its space of possible trajectories is already restricted [Blanchini, 1999; Mitchell et al., 2005]. In such cases, behaviour is not controlled through intervention, but determined by the geometry of the system’s reachable set.

We propose a reachability-based definition of power: the configuration of the set of states a system can attain. This paper considers systems whose behaviour is fully characterised by state-space dynamics and admissible controls.

-----

## 2. Dynamical Systems and Reachability

Let a system evolve over a state space `X` under dynamics:

|Equation               |Components                                        |
|:---------------------:|:------------------------------------------------:|
|`x_{t+1} = F(x_t, u_t)`|`x_t ∈ X` system state, `u_t ∈ 𝒰` admissible input|

The forward reachable set is:

|Symbol|Definition                          |Meaning                                        |
|:----:|:----------------------------------:|:---------------------------------------------:|
|`ℛ(t)`|`{ x(t) ∈ X | x(0) = x₀, u(·) ∈ 𝒰 }`|All possible trajectories the system can follow|

Behaviour is constrained by system dynamics and admissible inputs to lie within `ℛ(t)`. We assume admissible inputs `u(t)` are bounded and the system dynamics are well-defined over X.

-----

## 3. Behaviour as a Function of Reachability

All observable behaviour satisfies:

|Condition                 |Meaning                                |
|:------------------------:|:-------------------------------------:|
|`x(t) ∈ ℛ(t)`             |What a system does is a trajectory in ℛ|
|`ℛ(t)` defines possibility|What a system can do is defined by ℛ   |

Control over behaviour reduces to control over `ℛ(t)`, as all trajectories are contained within it. Whoever configures the reachable set configures the behaviour — without needing to intervene in any specific trajectory.

-----

## 4. Manipulation vs Structural Constraint

### 4.1 Manipulation-Based Control

Traditional models of power operate through intervention:

|Mechanism  |What It Does                  |Where It Acts     |
|:---------:|:----------------------------:|:----------------:|
|Persuasion |Changes beliefs or preferences|Representations   |
|Deception  |Alters perceived reality      |Projections `π(x)`|
|Incentives |Shifts reward landscape       |Value functions   |
|Information|Updates knowledge state       |Symbolic layer    |

These act on representations or decisions, attempting to redirect trajectories within `ℛ(t)`. They require continuous application. They can be resisted, detected, or reversed. They operate on the projection, not the dynamics. Manipulation alters trajectory selection within `ℛ(t)`, but does not alter `ℛ(t)` itself.

### 4.2 Structural Control

We define structural control as:

|Condition |Meaning                                                   |
|:--------:|:--------------------------------------------------------:|
|`ℛ(t) ⊆ S`|The reachable set is contained within the desired region S|

Under structural control: invalid trajectories are not generated, no correction is required, no manipulation is needed. Behaviour is constrained by construction. The system cannot reach states outside S — not because something prevents it at the boundary, but because the dynamics do not admit trajectories that lead there.

-----

## 5. The Structural Power Principle

**Principle (Structural Power).** A system does not need to be manipulated if its reachable set already constrains its trajectories.

Formally: if all admissible trajectories satisfy `x(t) ∈ ℛ(t) ⊆ S`, then behaviour is confined to S and external intervention is unnecessary.

|Type of Power |Mechanism              |Requires Continuous Action? |Resilient to Resistance?                           |
|:------------:|:---------------------:|:--------------------------:|:-------------------------------------------------:|
|Manipulation  |Acts on representations|Yes — must be maintained    |No — can be detected and countered                 |
|**Structural**|**Configures ℛ(t)**    |**No — built into dynamics**|**Cannot be resisted without modification of ℛ(t)**|

**Interpretation.** Power is not the ability to change trajectories. Power is the ability to define the space within which trajectories exist. Resistance requires expansion or deformation of `ℛ(t)`, not merely alternative trajectory selection.

### 5.1 Structural Power Invariance Theorem

**Theorem (Structural Power Invariance).** Let a dynamical system have reachable set `ℛ(t)` such that `ℛ(t) ⊆ S` for all admissible inputs, and system dynamics preserve reachability within S. Then for any trajectory `x(t)`: `x(t) ∈ S` for all `t`, and no admissible control sequence can produce `x(t) ∉ S` without modification of `ℛ(t)`.

**Proof.** By definition of reachability, all admissible trajectories lie within `ℛ(t)`. Given `ℛ(t) ⊆ S`, it follows that all trajectories lie in S. Any trajectory outside S would require a state `x ∉ ℛ(t)`, contradicting the definition of the reachable set. Thus, deviation from S requires expansion or deformation of `ℛ(t)` itself — not merely alternative trajectory selection within it. ∎

**Consequence.** Behavioural deviation outside S is impossible unless the reachable set is altered. This formalises the Structural Power Principle: control is embedded in the geometry of `ℛ(t)`, not in intervention over trajectories.

-----

## 6. Ignorance as Structural Confinement

We define ignorance not as lack of information, but as lack of access to reachable structure.

Let outputs be given by `y_t = π(x_t)`. A system operating only on `y_t` cannot access `ℛ(t)`.

|What the System Can See|What It Cannot See              |
|:---------------------:|:------------------------------:|
|Its own outputs `y_t`  |The reachable set `ℛ(t)`        |
|Its representations    |The geometry of possible futures|
|Changes in `π(x)`      |Whether `ℛ(t)` has changed      |

Such a system satisfies `ℛ(t₁) = ℛ(t₂)` under representational change. Behaviour remains structurally invariant. The system cannot alter its position within `ℛ(t)`, even if information changes.

This does not necessarily reflect a failure of intelligence under definitions based on representation or optimisation, but rather a limitation at the level of reachable structure. Access to `ℛ(t)` refers to the ability of a system to (i) evaluate counterfactual trajectories within ℛ, and (ii) select or induce transitions that alter `ℛ(t)` itself.

-----

## 7. Automatic Positioning

A system that lacks access to `ℛ(t)` cannot evaluate alternative trajectories outside `ℛ(t)`, cannot modify `ℛ(t)`, and cannot determine whether its current position is chosen or imposed.

|Condition                   |Consequence                                                  |
|:--------------------------:|:-----------------------------------------------------------:|
|System cannot perceive ℛ(t) |Cannot evaluate what is possible beyond current constraints  |
|System cannot modify ℛ(t)   |Cannot expand or restructure the space of futures            |
|System operates on π(x) only|All actions occur within a fixed ℛ, regardless of information|

Position within `ℛ(t)` is not chosen. It is determined. No manipulation is required. The system is already positioned by the geometry it cannot see. Formally, the system cannot realise trajectories outside `ℛ(t)`, and therefore cannot alter its position without modifying `ℛ(t)` itself.

-----

## 8. Relation to Representation and Deception

Deception operates on projections:

|What Deception Does  |Formal Effect          |
|:-------------------:|:---------------------:|
|Alters `y_t = π(x_t)`|Changes representation |
|Does not alter `ℛ(t)`|Reachable set unchanged|

Deception is effective only for systems operating on `π(x)`. Systems aware of `ℛ(t)` are invariant to representational manipulation — changing the projection does not change the dynamics.

This explains a structural principle: theatricality and deception are powerful agents to systems confined to the representational layer. They are irrelevant to systems that perceive reachable structure. The initiated operate on ℛ. The uninitiated operate on π. The gap between them is the Orthogonality Law [Morrison, 2026b]: `C ⊥ L`. Orthogonality here denotes that transformations in the representational layer do not imply transformations in the underlying dynamical structure. Thus, deception affects perceived trajectories but not admissible trajectories.

-----

## 9. Implications

### 9.1 Power Without Action

Structural power does not require continuous intervention, persuasion, or monitoring once `ℛ(t)` is fixed. It is embedded in system design. Once `ℛ(t) ⊆ S` is established, the constraint persists without maintenance.

### 9.2 Stability of Control

Structural constraints are persistent (they do not decay), robust to noise (small perturbations do not escape ℛ), and invariant under representation (changing π does not change ℛ). These properties follow from invariance of `ℛ(t)` under admissible dynamics. This makes structural control fundamentally more stable than manipulation-based control.

### 9.3 Alignment and Safety

In artificial systems, the distinction maps directly:

|Approach                            |Type of Control                 |Formal Object         |
|:----------------------------------:|:------------------------------:|:--------------------:|
|Output filtering, RLHF, prompt rules|Manipulation — acts on π(x)     |Representational layer|
|**Reachability constraints**        |**Structural — configures ℛ(t)**|**Dynamical layer**   |

Safe systems require `ℛ(t) ∩ Ω = ∅` [Morrison, 2026c] — not post hoc filtering. This is the AI safety application of the Structural Power Principle: govern the reachable set, not the output. Alignment failure occurs when unsafe states remain within `ℛ(t)`, regardless of output-level compliance. Output alignment without reachability constraint corresponds to selecting trajectories within an unsafe `ℛ(t)`, not eliminating unsafe trajectories from `ℛ(t)`.

-----

## Discussion

While exact computation of `ℛ(t)` is intractable in high-dimensional systems, structural control can be implemented through constraint parameterisation, invariant set approximation [Blanchini, 1999], or barrier functions [Ames et al., 2019]. The framework is structural and does not require exact enumeration of ℛ. Conservative over-approximations preserve the containment guarantee: if the over-approximation of ℛ lies within S, the true reachable set does too.

-----

## 10. Conclusion

We have shown that power can be understood as a structural property of dynamical systems. By defining power in terms of reachable sets, we eliminate the need for manipulation and reframe control as a property of geometry.

*Power is not the ability to influence trajectories. Power is the ability to define the reachable set within which all trajectories must lie.*

*A system is controlled not when it is persuaded, but when it cannot become otherwise.*

-----

## References

|Citation                    |Work                                                                           |Relevance                                          |
|:--------------------------:|:-----------------------------------------------------------------------------:|:-------------------------------------------------:|
|Ames, A.D. et al. (2019)    |*Control Barrier Functions: Theory and Applications.* IEEE TAC.                |Barrier function methods for constraint enforcement|
|Blanchini, F. (1999)        |*Set Invariance in Control.* Automatica, 35(11).                               |Invariant set methods — structural constraint      |
|Mitchell, I.M. et al. (2005)|*Hamilton-Jacobi Reachability.* IEEE TAC.                                      |Reachable set computation                          |
|Morrison, D. (2026a)        |*Geometric Control Theory of Cognition.* Independent Research.                 |Base framework                                     |
|Morrison, D. (2026b)        |*Orthogonal Decomposition of Consciousness and Language.* Independent Research.|C ⊥ L — why representation ≠ dynamics              |
|Morrison, D. (2026c)        |*The Reachability Safety Invariant.* Independent Research.                     |Safety as geometric exclusion                      |

-----

## Citation

```
Morrison, D. (2026). Structural Power in Dynamical Systems:
Control Without Manipulation via Reachability Constraints.
Independent Research. UK Patent Applications: GB2600765.8,
GB2602013.1, GB2602072.7, GB26023332.5.
```

**BibTeX:**

```bibtex
@misc{morrison2026power,
  author       = {Morrison, Davarn},
  title        = {Structural Power in Dynamical Systems: Control Without
                  Manipulation via Reachability Constraints},
  year         = {2026},
  publisher    = {Independent Research},
  note         = {UK Patent Applications: GB2600765.8, GB2602013.1,
                  GB2602072.7, GB26023332.5},
  url          = {https://github.com/davarn/morrison-framework}
}
```

-----

Structural Power in Dynamical Systems · Morrison Framework™ · Geometric Control Theory of Cognition

GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5

© 2026 Davarn Morrison — All Rights Reserved

-----

## Related Work

- [Why Reachability, Not Information](https://github.com/davarn/morrison-framework) — Why ℛ is the fundamental object
- [Representation Is Not Dynamics](https://github.com/davarn/morrison-framework) — Why output-level control is insufficient
- [Structural Orthogonality Proof](https://github.com/davarn/morrison-framework) — Language has no control authority under decoupled dynamics
- [The Reachability Safety Invariant](https://github.com/davarn/morrison-framework) — Safety as geometric exclusion
- [Geometric Control Theory of Cognition](https://github.com/davarn/morrison-framework) — The base theory
- [Licensing, Citation, and IP](https://github.com/davarn/morrison-framework) — How to cite and licence
