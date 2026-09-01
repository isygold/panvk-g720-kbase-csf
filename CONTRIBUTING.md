# Contributing to PanVK G720

Thanks for helping test, document, or improve the PanVK G720 / Kbase CSF work.

## Repository layout

- `main` is the public landing/documentation branch.
- `ci` is a frozen historical full-Mesa checkpoint.
- `android-candidate-beta-1.9.4` is the frozen source lineage for the public `0.1.0-beta.1.9.4` release.
- Published release tags and release assets must never be silently replaced.

Do not open a source-code pull request directly against a frozen release branch unless a maintainer explicitly asks for it. Documentation improvements should normally target `main`.

## Bug reports

Use the GitHub bug-report form and include:

- device model, SoC and GPU;
- Android version;
- kernel/Kbase version when known;
- exact PanVK release tag;
- exact ZIP SHA-256;
- runtime path (native, Winlator/Vortek, Wine/Box64, etc.);
- DXVK/VKD3D version when applicable;
- application/game and exact reproduction steps;
- relevant logs with timestamps.

Keep the original release ZIP unchanged so results remain attributable to exact published bytes.

## Code changes

A useful source change should:

1. identify the causal problem it addresses;
2. keep Kbase/CSF-specific behavior in the appropriate low-level layer;
3. avoid feature advertisement without implementation and validation;
4. include build/test evidence appropriate to the change;
5. avoid converting `DRM_FORMAT_MOD_INVALID` to `DRM_FORMAT_MOD_LINEAR` by assumption;
6. preserve release/version provenance.

## Claims and validation

Hardware-specific directed tests are evidence for the tested scope only. Do not describe the project as Vulkan conformant, universally compatible with Mali-G720, or compatible with all games unless that claim is independently established.

## Security

Do not place credentials, tokens, private device data, or sensitive vulnerability details in a public issue. See [SECURITY.md](SECURITY.md).
