# Releases

## `0.1.0-beta.1.9.4` — Public Beta / Pre-release

Published: 2026-09-01

GitHub Release: https://github.com/wonderkast02/panvk-g720-kbase-csf/releases/tag/0.1.0-beta.1.9.4

### Identity

- tag: `0.1.0-beta.1.9.4`
- source branch: `android-candidate-beta-1.9.4`
- source commit: `3549264275c9663ed73e01d652f4c0d16f21df22`
- historical `ci` base: `0521a3257628e811cfead6b5a9753e9f705e2f31`
- package: `PanVK-G720-0.1.0-beta.1.9.4.zip`
- package SHA-256: `01c6304206c6e348cb069e3d04fb1c7b693195b543b4134ad7c108a33906d1fa`
- embedded SO SHA-256: `05f867332924aacd91e6182cc1cc572ff04689cbcebeeba0e70bef61698dc9de`
- `meta.json` SHA-256: `01ef6b466751a5cb375073319ed70f872763ab71858b767c24d4ae9e737dae90`
- GNU Build ID: `4bc1dcd6ade70537a80e64bfc4976cb5936bf2af`
- minimum Android API: `35`

### Status

This is a community-testing beta and GitHub Pre-release. It is not a Vulkan conformance claim or a universal Mali-G720 compatibility claim.

The authoritative Mali-G720 MC8 line has directed/CTS tessellation validation, including two focused CTS repetitions at 160 PASS / 954 NOT_SUPPORTED / 0 FAIL / 0 OTHER. The recorded Winlator/Vortek publication-freeze run reached the first `vkQueueSubmit` but did not reach acquire/present; this remains a known beta limitation.

Release assets include the immutable ZIP, `SHA256SUMS.txt`, and a release manifest containing source and binary provenance.
