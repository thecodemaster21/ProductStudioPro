# Release validation

Checked on 2026-09-21 using Blender 5.1.2 on macOS (Apple Silicon).

| Check | Result |
| --- | --- |
| Python syntax and relative imports | Passed for all package and helper scripts |
| Documentation links and required assets | Passed |
| Sidebar operator registration | All 56 referenced operator IDs registered |
| Register/unregister lifecycle | Passed |
| Studios | Automotive, Watch, Perfume, Headphones and Packaging created lights successfully |
| Cameras | Hero, Macro, Beauty 45° and Side Profile created and activated the expected cameras |
| Reflection cards | Rectangle, Strip and Edge created successfully |
| Material libraries | 25 THAR ROXX and 11 headphone materials created |
| Bundled assets | Rock base loaded; concrete material loaded and applied to the selected mesh |
| Render setup | Cycles setup and widescreen output preset completed |
| Real render integration | Eight PNG outputs: Beauty, Clay, Wireframe and Transparent for each of two differently named cameras |
| State after successful batch render | Active camera and material override restored |
| Install ZIP | CRC integrity, package root and required notices checked; deterministic rebuild verified |

## Fixes found by validation

1. Hero camera creation did not set the active scene camera. The release copy now does so.
2. Appending the concrete material through a context-sensitive operator disrupted the mesh selection. It now uses the library loading API.
3. The camera batch filter could omit PSP/custom cameras when studio-prefixed cameras were present. All cameras in the scene are now included.

## Limits

The checks use synthetic geometry and tiny 32 × 32 CPU renders. They establish basic execution and output creation, not final image quality or complete shader equivalence. They do not cover every legacy operator, third-party MAX/FBX files, complex PBR translation, every UI interaction, GPU rendering, other operating systems or later Blender releases.

The GitHub Actions workflow runs source validation and packaging only. Blender checks are provided as local scripts and were run for this prepared release.
