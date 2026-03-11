# Reviewer Map

## Claim Scope

- Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
- Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.

## Theorem Dependency Chain

1. `EG1`: coercive response and active control floor.
2. `EG2`: capture and admissible continuation.
3. `EG3`: compactness and no-collapse spacing.
4. `EG4`: rigidity and transfer.
5. Identification bridge: strict coherence on the determining class.
6. Scalar closure: `S4P_G1, S4P_G2, S4P_G3, S4P_G4, S4P_G5, S4P_G6, S4P_GM` all `PASS`.

Primary files:

- `paper/SMOOTH_4D_POINCARE_CONJECTURE_PREPRINT.md`
- `notes/EG1_public.md`
- `notes/EG2_public.md`
- `notes/EG3_public.md`
- `notes/EG4_public.md`
- `notes/IDENTIFICATION_BRIDGE.md`

## Closure Gates

| Gate | Constant | Description |
|------|----------|-------------|
| `S4P_G1` | `kappa_smoothing` | projected smoothing response has a strict positive floor |
| `S4P_G2` | `sigma_handle` | handle defect stays above capture floor across admissible surgeries and restart losses |
| `S4P_G3` | `kappa_compact` | normalized near-failure families are precompact and smoothing windows do not collapse |
| `S4P_G4` | `rho_rigidity` | bad exotic countermodels are excluded |
| `S4P_G5` | `sphere_transfer` | rigid limit transfers to the standard 4-sphere endpoint class |
| `S4P_G6` | `eps_coh` | strict coherence / identification closure |
| `S4P_GM` | derived | final strict margin |

## Falsification Conditions

- `repro/certificate_runtime.json` has any non-`PASS` gate.
- `lane.active_lane != "manifold_constrained"`.
- `all_pass != true`.
- Any manifest hash mismatch under `repro/repro_manifest.json`.
- A verified counterexample to any EG theorem statement used in the paper.
