# Upload and release guide

## Repository contents

Use the contents of the prepared repository folder as the GitHub repository root. It contains `README.md`, `LICENSE`, `.github/`, `docs/`, `scripts/` and the inner `ProductStudioPro/` add-on package. Include hidden files such as `.gitignore` and `.github/`.

Suggested repository name: **ProductStudioPro**

Suggested description: **A Blender product visualization add-on for studio lighting, materials, reflection cards, camera presets and render deliverables.**

Suggested topics: `blender`, `blender-addon`, `product-visualization`, `studio-lighting`, `materials`, `rendering`, `python`.

The README automatically displays `docs/images/main-preview.png` at the top. The same image can be uploaded in GitHub's social-preview settings if desired.

## Build and publish a release

1. Run `python3 scripts/validate.py` and `python3 scripts/build_release.py`.
2. Run the Blender smoke and render checks described in `CONTRIBUTING.md`.
3. Commit and push the repository contents to your GitHub repository.
4. Create a release tagged `v5.2.0`, using `docs/RELEASE_NOTES.md` for the description.
5. Attach `dist/ProductStudioPro-5.2.0.zip` and `dist/SHA256SUMS.txt` as release assets.

Do not install the outer GitHub source ZIP in Blender. The install ZIP contains one top-level `ProductStudioPro` folder with `__init__.py`, runtime modules, assets and license notices.

The GitHub Actions workflow validates source and builds an artifact on pushes, pull requests and manual runs. It does not publish a release automatically and does not claim to run Blender.

Before public release, record the provenance of bundled `.blend` and image assets if they came from other creators. The source folder did not supply separate asset credits.
