# ImpuriTree README Progress Update Design

## Goal

Update the challenge registration README so readers can find the two public
development repositories and understand the challenge-relevant development
sequence without implying that issue #81's verification targets are complete.

## Content

Keep the existing Team and Challenge tables unchanged, then add:

1. A **Development repositories** section:
   - `GraftTN/Graft.jl`: the general tree tensor-network core, including
     purification, time evolution, and adaptive bond machinery.
   - `GraftTN/GraftImpurity.jl`: the impurity-specific layer for bath fitting,
     Hamiltonian construction, topology mapping, and Green-function workflows.
2. A **Brief development history** section with five chronological,
   challenge-relevant milestones:
   - July 9: establish the Graft.jl TTN core and initial bath/evolution
     primitives.
   - July 11: add deterministic purification and thermal correlators, then
     separate impurity functionality into GraftImpurity.jl.
   - July 12–14: develop impurity bath fitting, Hamiltonian lowering, and
     star/Cayley topology mapping.
   - July 28: add direct global-Krylov bootstrapping for initially small
     purified-state bonds.
   - July 29–30: implement and harden residual-driven expansion and
     implicit-step residual/truncation controls.

## Accuracy rules

- Link repository names directly to GitHub.
- Attribute milestones to public commit history rather than team recollection.
- Use “implemented,” “added,” or “developed” for code capabilities.
- Do not say that the ED 10⁻⁶ target, continuous-bath cross-check, β = 100
  frontier, or complete error budget has passed unless separate evidence is
  linked.
- Keep the history brief: one sentence per milestone.

## Verification

- Confirm both repository links resolve.
- Compare each milestone against the public commit history.
- Run a Markdown whitespace check with `git diff --check`.
- Confirm the implementation commit changes only files under
  `tracks/mps/solutions/ImpuriTree/`.
