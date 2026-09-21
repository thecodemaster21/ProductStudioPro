# User guide

## Install and open

Install `ProductStudioPro-5.2.0.zip` through **Edit → Preferences → Add-ons → Install from Disk**. Enable **Product Studio Pro**, then press **N** in the 3D Viewport and choose **Product Studio**. Use Blender 5.1 or newer; this release was smoke-tested on 5.1.2.

When replacing an older installation, disable it first and restart Blender after installation if the previous modules remain loaded.

## 1. Product

Choose your main mesh in **Product**. For a multi-part product, put its meshes in a dedicated collection and choose that collection too. **Detect** picks the active object's collection; explicitly set the Product field for camera presets. Avoid selecting a collection that also contains unrelated scene geometry.

Use **Analyze** to inspect object, material and missing-texture counts. **Split by Material** and **Add Subdivision** change the selected geometry; inspect the result before continuing.

## 2. Studio

Choose **Automotive**, **Watch**, **Perfume**, **Headphones** or **Packaging**. Add or refine lighting with **Softbox**, **Strip**, **Rim** or **3-Point**. Backdrop controls include black, gray and shadow options. Choose **Setup Cycles** in Render for the intended rendering workflow.

## 3. Materials

Expand the THAR ROXX or Headphone library. Create the library, choose a finish and apply it to your selected object or faces. Headphone **Auto Assign Product** infers parts from names such as cushion, mesh, yoke, plastic and aluminum. Review these assignments on imported assets.

In **Advanced**, use **Import PBR**, **Validate** and **Relink Textures** when working with external materials. Unsupported source shader features may need rebuilding by hand.

## 4. Reflections

Create a rectangle, strip or edge card. Select a card to edit its dimensions, transforms, strength, gradient, visibility and color. Duplicate and mirror cards to balance highlights. Evaluate the result in rendered view or a preview render.

## 5. Camera

Choose Hero, Macro, Beauty 45° or Side Profile. The selected preset becomes the active scene camera. Use **View Camera** to inspect the composition, then adjust lens and depth of field. **Match View** positions the camera from the viewport.

## 6. Render

1. Save the `.blend` file.
2. Choose **Setup Cycles** and a suitable quality preset.
3. Select the output folder and enable at least one deliverable: Beauty, Clay, Wireframe or Transparent.
4. Use **Preview** for a quick check or **Render Shot** for the enabled outputs.
5. Use **Render All Cameras** to process every camera in the current scene, including custom-named cameras.

The production output is relative to the saved `.blend` file unless an absolute output folder is configured. Existing filenames receive a numbered suffix. All-camera rendering includes every scene camera, so remove unwanted cameras first.

## Tools

Visibility tools save and restore the current view layer's hidden-object state. Vehicle preparation tools operate on your selection in Object Mode. **Assign One Material to Selected** replaces every material slot and face assignment on selected meshes. **Join & Rename** uses `SM_TharRoxx_`; grouping uses `GRP_TharRoxx`. These conventions are currently fixed.

## Troubleshooting

| Symptom | What to check |
| --- | --- |
| Add-on does not appear | Install the built add-on ZIP, enable it, and check the Blender version. |
| Camera preset does nothing | Set **Product** to a mesh; selecting only a collection is not enough for these presets. |
| Render asks you to save | Save the `.blend` before production rendering. |
| Render creates no output | Enable at least one deliverable, check the active camera and review Blender's error reports. |
| Missing textures | Use **Advanced → Relink Textures** and select the texture folder. |
| Auto-assigned materials look wrong | Review part names and apply materials manually. |
| Buttons are disabled | Use Object Mode and select editable meshes where required. |

For a bug report, include your Blender version, operating system, steps to reproduce and any traceback. Use the repository's bug-report template.
