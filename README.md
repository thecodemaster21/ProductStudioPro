<p align="center">
  <img src="docs/images/main-preview.png" alt="Product Studio Pro — studio presets, reflection controls, camera presets and render deliverables inside Blender" width="100%">
</p>

<h1 align="center">Product Studio Pro</h1>

<p align="center">
  <strong>Build the studio. Shape the light. Frame the product.</strong><br>
  A complete product-shot workflow in one Blender sidebar.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-5.2.0-343a40?style=flat-square" alt="Version 5.2.0">
  <img src="https://img.shields.io/badge/Blender-5.1%2B-E87D0D?style=flat-square" alt="Requires Blender 5.1 or newer">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-GPL--2.0--or--later-227A67?style=flat-square" alt="GPL-2.0-or-later license"></a>
</p>

<p align="center">
  <a href="https://github.com/thecodemaster21/ProductStudioPro/releases"><strong>Download / Releases</strong></a>
  &nbsp; · &nbsp;
  <a href="#quick-start">Installation</a>
  &nbsp; · &nbsp;
  <a href="docs/USER_GUIDE.md">User guide</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/thecodemaster21/ProductStudioPro/issues">Feedback</a>
</p>

---

**Spend more time refining the image and less time rebuilding the setup.**

Product Studio Pro brings product preparation, studio lighting, materials, reflection cards, camera presets and rendering into a single, organized workspace. Built by **Rahul Gambhir**, it gives product artists a practical starting point for automotive, watch, perfume, headphone and packaging scenes.

<p align="center">
  <strong>5 studio presets &nbsp; / &nbsp; 4 main camera presets &nbsp; / &nbsp; 4 render deliverables</strong>
</p>

## What makes it useful

| | What you can do |
| :--- | :--- |
| 💡 **Build a studio in fewer steps** | Start with **Automotive, Watch, Perfume, Headphones or Packaging**. Refine the scene with softbox, strip, rim and three-point lighting. |
| ✨ **Take control of reflections** | Place **rectangle, strip and edge cards**. Adjust their size, position, rotation, strength and gradients, with RGB or Kelvin color controls. |
| 📷 **Find your angle** | Start with **Hero, Macro, Beauty 45° or Side Profile**. Fine-tune focal length, depth of field and composition, or match the viewport. |
| 🎨 **Give the product its finish** | Explore **25 THAR ROXX materials** and an **11-material headphone library**, with variants and name-based headphone assignments. |
| 🖼️ **Create your deliverables** | Produce **beauty, clay, wireframe and transparent-background outputs** for one camera or every camera in the scene. |
| 🧰 **Prepare assets for the workflow** | Analyze imports, split meshes by material, relink textures, organize parts and check static vehicle parts before FBX export. |

[Explore the full feature tour →](docs/FEATURES.md)

## From product to final render

<p align="center">
  <strong>Product → Studio → Materials → Reflections → Camera → Render</strong>
</p>

| Step | Your next move |
| :--- | :--- |
| **01 · Product** | Choose the main product object and its collection for multi-part assets. |
| **02 · Studio** | Build a preset studio, then refine lights and backdrop. |
| **03 · Materials** | Choose a finish from a library or import your PBR maps. |
| **04 · Reflections** | Position cards to shape highlights on reflective surfaces. |
| **05 · Camera** | Choose a shot, check the framing and adjust focus. |
| **06 · Render** | Save the scene, choose deliverables and render one or all cameras. |

## Quick start

**Requirement:** Blender **5.1 or newer**. Focused release checks were completed on **Blender 5.1.2 / macOS**; other versions and platforms have not been verified for this release.

1. Open [Releases](https://github.com/thecodemaster21/ProductStudioPro/releases) and download **`ProductStudioPro-5.2.0.zip`**, if available.
2. In Blender, open **Edit → Preferences → Add-ons** and choose **Install from Disk** from the menu.
3. Select the installer ZIP and enable **Product Studio Pro**.
4. In the **3D Viewport**, press **N** and open the **Product Studio** tab.
5. Set your **Product** object, choose a studio and begin refining the shot.

> **Before rendering:** Save your `.blend` file, check the active camera and enable at least one render deliverable.

<details>
<summary><strong>No installer available? Build it from the source.</strong></summary>

Clone the repository or extract a source download. From its root folder, run:

```sh
python3 scripts/build_release.py
```

Install the ZIP created in `dist/`. GitHub's automatic **Source code (zip)** download contains the repository; build the Blender installer from it using the command above.

</details>

[Read the installation and workflow guide →](docs/USER_GUIDE.md)

## Inside the sidebar

<details>
<summary><strong>See the original Blender interface</strong></summary>

<p align="center">
  <img src="docs/images/sidebar-original.png" alt="Original Product Studio Pro sidebar with the Product and Tools sections expanded" width="253">
</p>

Six numbered sections keep the core workflow together. **Advanced** contains additional import and scene tools; **Tools** contains visibility and vehicle-part preparation actions.

</details>

<sub>The header is a designed feature illustration based on the supplied screenshot. The expandable image above shows the original interface.</sub>

## A few things to know

- **Product selection:** Set the Product object explicitly for camera presets. Use a dedicated collection for multi-part products.
- **Vehicle tools:** Naming currently uses `SM_TharRoxx_`, with `GRP_TharRoxx` for grouping. FBX checks report preparation issues; they do not export files or create Unreal variants.
- **Material assignment:** Headphone auto-assignment uses object names. Review the results for your model.
- **Imported shaders:** 3ds Max import and material translation depend on the source file and supported nodes. Complex shaders may need manual adjustments.
- **Scene changes:** Save before applying broad studio or material changes. Some legacy operators remain available through Blender search.

## License and commercial inquiries

**Product Studio Pro is available free of charge to individual users.** The software is licensed under **GNU GPL version 2 or, at your option, any later version**.

Planning to use it commercially or in a studio? You are welcome to [contact the maintainer through the project’s Issues page](https://github.com/thecodemaster21/ProductStudioPro/issues) to discuss your workflow, support needs or custom development.

**Contact is voluntary. The GPL permits both personal and commercial use without separate permission.**

Read the [full license](LICENSE) and [third-party notices](THIRD_PARTY_NOTICES.md). The bundled 3ds Max importer retains its original credits. Product and brand names identify presets and workflows; no affiliation or endorsement is implied.

## Feedback and contributions

Found a bug, tested a workflow or have an idea for the next improvement? [Open an issue](https://github.com/thecodemaster21/ProductStudioPro/issues) and include your Blender version and a clear example.

Contributions are welcome. Start with the [contribution guide](CONTRIBUTING.md).

<details>
<summary><strong>Developer checks and packaging</strong></summary>

```sh
python3 scripts/validate.py
python3 scripts/build_release.py
blender --background --factory-startup --python-exit-code 1 --python scripts/smoke_test.py
blender --background --factory-startup --python-exit-code 1 --python scripts/render_test.py
```

The checks cover source validation, packaging, representative studio and material operations, camera presets, reflection cards and eight small render outputs. See [validation notes](docs/VALIDATION.md) for the full scope and limitations.

[Changelog](CHANGELOG.md) · [Release guide](docs/RELEASING.md)

</details>

---

<p align="center">
  Created by <strong>Rahul Gambhir</strong> · <a href="https://github.com/thecodemaster21">thecodemaster21</a><br>
  If Product Studio Pro helps your workflow, consider giving the repository a star. ⭐
</p>
