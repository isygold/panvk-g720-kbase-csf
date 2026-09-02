# Licensing

PanVK G720 is built from Mesa/PanVK source code plus project-specific integration and documentation work.

This repository is **not relicensed under one project-wide license**. Licensing is determined **per file and per component**, following the original upstream terms and the licensing metadata carried by the relevant source.

## Authoritative licensing information

For source code derived from Mesa, the authoritative licensing information is:

1. the `SPDX-License-Identifier` in each source file, when present;
2. the corresponding license text in the source tree's `licenses/` directory;
3. component-specific license files or notices where applicable;
4. original copyright notices and attribution retained in the source.

The frozen source lineage for the current public beta is:

- branch: `android-candidate-beta-1.9.4`
- commit: `3549264275c9663ed73e01d652f4c0d16f21df22`

Mesa's own licensing documentation in that source lineage states that the distribution contains multiple components, that different licenses may apply to different components, and that individual source-file SPDX identifiers should be consulted for the applicable terms.

Relevant source locations include:

- [`docs/license.rst`](https://github.com/wonderkast02/panvk-g720-kbase-csf/blob/android-candidate-beta-1.9.4/docs/license.rst)
- [`licenses/`](https://github.com/wonderkast02/panvk-g720-kbase-csf/tree/android-candidate-beta-1.9.4/licenses)

## Current PanVK G720 changes

Most driver/source files changed by the current PanVK G720 candidate carry the upstream Mesa `MIT` SPDX identifier.

Some repository metadata, workflow, documentation, generated, imported, or component-specific files may not carry the same identifier or may be governed by separate terms. Their original licensing and copyright information remains authoritative.

No statement in this document:

- replaces an existing SPDX identifier;
- removes or changes an original copyright notice;
- relicenses third-party or upstream code;
- assigns MIT, Apache-2.0, or any other single license to the repository as a whole;
- changes the licensing terms of the published `0.1.0-beta.1.9.4` binaries or their corresponding source components.

## Project-authored material

Project-authored documentation, integration material, or other original work may receive an explicit license only where ownership and provenance permit that choice.

If a project-authored file does not currently carry an explicit license, this document does not assign one implicitly.

## Contributions

Contributors must preserve the applicable license, SPDX identifier, copyright notice, and attribution requirements of the component they modify.

When adding a new file derived from existing Mesa/PanVK code, follow the licensing terms of the source component and preserve its provenance.

## Release provenance

The current public beta remains tied to its immutable release, exact source lineage, and recorded asset digests. Licensing documentation does not alter release bytes, source history, or provenance.
