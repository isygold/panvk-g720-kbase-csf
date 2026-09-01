# Repository governance

## Branch roles

- `main`: active public landing/documentation branch.
- `ci`: frozen historical full-Mesa checkpoint.
- `android-candidate-beta-1.9.4`: frozen source lineage for release `0.1.0-beta.1.9.4`.

`main` and `ci` intentionally retain unrelated histories; they are not merged or rebased merely to normalize the graph.

## Release integrity

Published driver bytes are versioned immutably by policy: if driver/package bytes change, the public version changes.

The current public beta is tied to:

- tag `0.1.0-beta.1.9.4`;
- source commit `3549264275c9663ed73e01d652f4c0d16f21df22`;
- package SHA-256 `01c6304206c6e348cb069e3d04fb1c7b693195b543b4134ad7c108a33906d1fa`.

Repository governance requires release tags to be protected from update/deletion and frozen source branches to remain unchanged. `main` should block deletion and non-fast-forward history rewrites while retaining normal fast-forward maintenance.

Future releases should use GitHub Immutable Releases. GitHub documents that repository-level release immutability applies only to releases published after enablement, so the already-published `0.1.0-beta.1.9.4` remains anchored by its exact tag, source commit and recorded asset digests.

## Security and reports

Private vulnerability reporting is enabled. Community test reports should follow `docs/COMMUNITY_TESTING.md`.

## Licensing

This governance change does not add, replace, or reinterpret project licensing. License normalization is intentionally outside the scope of this repository-hardening transaction.
