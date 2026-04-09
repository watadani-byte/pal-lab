# PAL LAB Glossary

Core terms used across PAL LAB documentation.

> This glossary is a working document.
> Definitions are subject to revision as the
> repository develops.
> Trust rank applies: see
> [governance/trust_rank_policy.md](../governance/trust_rank_policy.md)

-----

## Re-anchoring

Re-anchoring is the operation of restoring generation
to a valid anchor state after contextual drift,
contamination, or local overcommitment.

Within PAL, re-anchoring functions as a basic
generative operation for recovering:

- character stability
- generation continuity
- readable coherence

Re-anchoring is not a retry.
It is a deliberate return to a verified anchor state —
one that has been adopted, retained, and remains
available for restoration.

The conditions required for re-anchoring to be possible
are defined in the re-anchoring principle:
see [declarations/pal_declaration.md](../declarations/pal_declaration.md).

*See also: [pal/anti_drift.md](../pal/anti_drift.md)*  
*See also: [persona/governance_pal.md](../persona/governance_pal.md)*

-----

## Inter-PAL Conflict

A condition in which two or more active PAL layers
impose partially incompatible continuity requirements,
such that preserving one layer increases drift,
distortion, or instability in another.

Inter-PAL Conflict is distinct from ordinary drift
and from contamination:

|Condition         |Description                                                                            |
|------------------|---------------------------------------------------------------------------------------|
|Drift             |A continuity target moves away from its reference point                                |
|Contamination     |Harmful or misleading material accumulates in the continuity environment or anchor base|
|Inter-PAL Conflict|Two or more PAL layers conflict; preserving one continuity target destabilizes another |

Inter-PAL Conflict is not the absence of continuity
control. It is the collision of multiple
continuity-control demands.

In image workflows, this may occur when Character PAL,
Sequence PAL, Costume PAL, Background PAL, or Style PAL
compete for reconstruction priority.

Resolution requires explicit priority decisions
under Governance PAL, not prompt adjustment alone.

*Also referred to as: PAL interference*

*See: [pal/anti_drift.md](../pal/anti_drift.md)*  
*See: [persona/governance_pal.md](../persona/governance_pal.md)*