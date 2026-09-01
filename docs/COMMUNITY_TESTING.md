# Community testing guide

## Current public beta

Release: `0.1.0-beta.1.9.4`

Official package:

`PanVK-G720-0.1.0-beta.1.9.4.zip`

Expected SHA-256:

`01c6304206c6e348cb069e3d04fb1c7b693195b543b4134ad7c108a33906d1fa`

Verify before testing:

```sh
sha256sum PanVK-G720-0.1.0-beta.1.9.4.zip
```

Do not repack or edit the ZIP when producing a result intended to describe this release.

## Minimum report

Include:

1. device model;
2. SoC;
3. GPU model/core count when known;
4. Android version;
5. kernel/Kbase version when known;
6. exact release tag and ZIP SHA-256;
7. runtime path (native / Winlator / Vortek / Wine / Box64);
8. wrapper version when applicable;
9. DXVK/VKD3D version when applicable;
10. application/game;
11. exact reproduction steps;
12. logs and timestamps;
13. whether the device rebooted, the application aborted, or only the test process failed.

## Interpretation

An application assertion or non-zero `VkResult` does not by itself prove a GPU fatal. Preserve the original logs and report what was directly observed.

The current public beta is not a Vulkan-conformance claim and not a universal Mali-G720 compatibility claim.

## Safety

Experimental GPU-driver tests can hang applications, fault the GPU, or require a device reboot. Save important work before testing.

Never attach passwords, API tokens, account cookies, private keys, or unrelated personal data to a report.
