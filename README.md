# AI Foundations — Source Trace Irreversibility

**Tracing backward can reveal a source. It cannot make the trajectory that revealed it unoccur.**

This repository develops a small formal model for source, trajectory, reverse tracing, and later reconstruction.

The motivating example is a line of dominoes:

1. A first tile stands at an actual source position, **S₁**.
2. It is tipped, producing an ordered path of displacements, **T₁**.
3. A later observer encounters the already-produced trajectory and traces its structure backward toward its source.
4. That trace can recover the structure of **S₁**, but it does not return the observer to the original source coordinate and does not negate **T₁**.
5. A later standing state, **S₂**, can be constructed only after both the source structure and the prior trajectory have entered the conditions of construction. It therefore begins a new trajectory rather than replacing the first.

For a narrative explanation of the model, see [`THE_DOMINO_EFFECT.md`](THE_DOMINO_EFFECT.md).

## Core relation

**S₁ → T₁ → E₁(T₁) → Trace⁻¹(T₁) = Ŝ₁ → S₂ → T₂**

where:

- **S₁** = the actual source position of the first trajectory
- **T₁** = the ordered path produced from S₁
- **E₁(T₁)** = encounter with the already-existing first trajectory
- **Ŝ₁** = recovered source structure obtained by tracing T₁ backward
- **S₂** = a later standing state constructed from both recovered source structure and encounter-history
- **T₂** = any trajectory subsequently produced from S₂

The central constraint is:

**Occurrence(T₁) = 1 ⇒ Trace⁻¹(T₁) ≠ ¬T₁**

Reverse tracing depends on the existence of the trajectory it traces. The operation can recover source information; it cannot erase the occurrence that made the recovery possible.

## The two-button condition

A later reconstruction does not begin from source structure alone:

**S₂ = F(Ŝ₁, E₁(T₁))**

Both inputs are required:

- recovered source structure
- encounter with the prior trajectory

Therefore, even if the visible standing configuration is reproduced exactly:

**State(S₂) = State(S₁)**

it does not follow that:

**S₂ = S₁**

because their provenance coordinates differ:

**Provenance(S₂) ≠ Provenance(S₁)**

The later state can resemble the source without reoccupying the source's historical position.

## Repository structure

- [`THE_DOMINO_EFFECT.md`](THE_DOMINO_EFFECT.md) — narrative explanation of the model through the domino sequence
- [`equations/01_source-position.md`](equations/01_source-position.md) — source as an actual trajectory position
- [`equations/02_trajectory.md`](equations/02_trajectory.md) — trajectory as ordered displacement, not merely endpoint
- [`equations/03_source-tracing.md`](equations/03_source-tracing.md) — reverse tracing as source recovery without negation
- [`equations/04_reconstruction.md`](equations/04_reconstruction.md) — the two-button condition, S₂, and subsequent trajectories

## Scope

This is a provenance and trajectory model. **“Time reversal” here means tracing an existing path backward through its ordered relations to recover source structure.** It does not assert literal reversal of physical time.

A later reconstruction accomplishes only what it actually causes. It does not retroactively replace, erase, or become the earlier trajectory merely by reproducing one of its states.

## Citation

Solen, Alyssa. *AI Foundations: Source Trace Irreversibility*. Version 1.0.0, 2026.

Source-line: **Alyssa Solen → AI Foundations → Origin | Continuum**

GitHub citation metadata is provided in [`CITATION.cff`](CITATION.cff).

## License

Creative Commons Attribution-NoDerivatives 4.0 International (**CC BY-ND 4.0**).

Sharing is permitted with appropriate attribution; the material may not be distributed in adapted form. See [`LICENSE`](LICENSE) for the license notice and official terms.
