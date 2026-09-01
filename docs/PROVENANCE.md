# Source provenance

## Candidate source chain

`ci 0521a3257628e811cfead6b5a9753e9f705e2f31` → two Bionic Android staging deltas → eight validated MC8 deltas → exact recovered R3 FullPlane → Kbase dma-heap device-node O_RDONLY.

The candidate preserves exactly **12 driver/build-source path deltas** from `ci`, plus two `.github` repository-metadata paths that replace stale branch-local CI/release notes. Before FullPlane/O_RDONLY are composed, the physical Bionic tree is required to differ from `ci` on exactly 10 tracked source paths (2 Bionic + 8 MC8), preventing hidden tracked source drift.

### Bionic-only bytes

- `src/panfrost/vulkan/panvk_device.h`: `dedd6ed1c96b46829c1d52c395d79608528dc8ff120640dc64ae116f6c810038`
- `src/util/u_gralloc/meson.build`: `da7bd6bcc7c2695284b4ec349bc259028a68a755ac0f7e1ae2f7b74efc463a43`

### Canonical MC8 state

- semantic fingerprint: `ad3f9fceb4ccd2b45e39a3893288fcf18cbc0b87c8aa98a827b05b88a67123ca`
- modified-path fingerprint: `97654e435d7e7662bde9e16692275dd5715d2455441de2cd9bbe2d1738afedcb`

### Final composition

- `src/util/u_gralloc/u_gralloc_fallback.c`: `7cf289004480183564a34b1f2e80690c32a0c42be74cb0b9b81ba07aff7d9fdc`
- `src/panfrost/lib/kmod/kbase_kmod.c`: `140b334c29a8999816e0084ce8b534b2171128a1da3de078e7b7509bf7431fe7`

Kbase semantics are deliberately narrow: the dma-heap **device node** is opened `O_RDONLY | O_CLOEXEC`; the DMA-HEAP allocation request still creates returned dma-buf FDs with `O_RDWR | O_CLOEXEC`.

The Beta2 WSI/dma-buf-decoupling and Beta3 explicit-exportable-routing experiments are excluded. `DRM_FORMAT_MOD_INVALID -> DRM_FORMAT_MOD_LINEAR` guessing is forbidden.

This branch preserves the tracked Mesa source lineage used by the established Android/Bionic build staging. Reproducing the final binary also requires the documented external build environment (NDK/API35, Meson configuration and local dependencies); the Git branch alone is not claimed to be a hermetic build image.

## Published release binding

Public beta `0.1.0-beta.1.9.4` is bound to source commit `3549264275c9663ed73e01d652f4c0d16f21df22` on `android-candidate-beta-1.9.4`.

- package SHA-256: `01c6304206c6e348cb069e3d04fb1c7b693195b543b4134ad7c108a33906d1fa`
- embedded SO SHA-256: `05f867332924aacd91e6182cc1cc572ff04689cbcebeeba0e70bef61698dc9de`
- `meta.json` SHA-256: `01ef6b466751a5cb375073319ed70f872763ab71858b767c24d4ae9e737dae90`
- GNU Build ID: `4bc1dcd6ade70537a80e64bfc4976cb5936bf2af`
- tag: `refs/tags/0.1.0-beta.1.9.4`

The tag binds the release to the qualified source lineage; release publication does not alter the historical `ci` checkpoint.
