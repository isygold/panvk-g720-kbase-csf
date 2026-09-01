# Validation matrix

## Native Mali-G720 MC8

Validated within the recorded scope:

- direct Kbase/CSF execution;
- compute/graphics and offscreen readback;
- Android AHB import;
- AIMapper v5 FullPlane metadata;
- GPU/CPU coherency regressions;
- `tessellationShader=true`; physical subgroup size 16;
- Direct/P7/Replay 9/9;
- common-edge triangles 6/6 and quads 6/6;
- winding 48/48; domain-origin 4 PASS / 8 NOT_SUPPORTED / 0 FAIL;
- simultaneous-use sync64 64/64; DYN256 19/19;
- stress through 8192 triangle patches;
- focused CTS, twice: 160 PASS / 954 NOT_SUPPORTED / 0 FAIL / 0 OTHER.

This is not a Vulkan conformance claim.

## FullPlane + O_RDONLY native candidate

The native qualification passed the exact fake-swapchain, bridge and core matrices used by R3F: control 10/10, candidate 10/10, bridge 18/18, core 18/18.

## Winlator/Vortek

`0.1.0-beta.1.9.4` remains unresolved/failed at the current Gate A boundary. No acquire/present was reached in that run. Do not infer a GPU fatal from `_wassert` alone; a later forensic stage was prepared specifically to classify the first-submit boundary, but had not been executed at publication freeze.
