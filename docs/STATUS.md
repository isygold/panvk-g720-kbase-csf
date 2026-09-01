# PanVK G720 — Current status

Updated: 2026-09-01

## Repository layout

- `main`: landing and release-facing documentation.
- `ci`: historical full-Mesa checkpoint `0521a3257628e811cfead6b5a9753e9f705e2f31`.
- `android-candidate-beta-1.9.4`: candidate Android source lineage based on `ci`.

`main` and `ci` have unrelated Git histories and are intentionally not merged/rebased just to normalize the graph.

## Candidate identity

Community candidate: `0.1.0-beta.1.9.4`. Distribution is **HOLD** and there is no Git tag/GitHub Release yet.

- ZIP SHA-256: `01c6304206c6e348cb069e3d04fb1c7b693195b543b4134ad7c108a33906d1fa`
- clean `libvulkan_panfrost.so`: `05f867332924aacd91e6182cc1cc572ff04689cbcebeeba0e70bef61698dc9de`
- raw candidate SO: `54a3a7dc9c972cc364058846e9b7ede57d4ac32d0902e8c8288e8fe89b9bb9bb`
- `meta.json`: `01ef6b466751a5cb375073319ed70f872763ab71858b767c24d4ae9e737dae90`
- Build ID: `4bc1dcd6ade70537a80e64bfc4976cb5936bf2af`

The same clean driver bytes were first natively qualified under the internal Beta1.1 package identity; later `beta.1.9.4` changed package identity, not the embedded SO.

## Live boundary

The latest standard-wrapper Gate A reached swapchain/images/views, pre-render image setup, sampler, graphics pipeline and one `vkQueueSubmit`, then hit an AIO `_wassert` before acquire/present. `_wassert` alone is not proof of GPU fatal. No R3H execution had superseded this evidence at publication freeze.
