<div align="center">

<img width="860" alt="DRH Scene Material Inventory" src="docs/media/Logo.png" />

# DRH - Scene Material Inventory

**Before you send the .blend, know every material, texture, and missing file inside it.**

![Status](https://img.shields.io/badge/Status-Released-22C55E?style=for-the-badge) ![Version](https://img.shields.io/badge/Version-1.0.0-00B7FF?style=for-the-badge) ![Blender](https://img.shields.io/badge/Blender-4.2%2B-0B1F4D?style=for-the-badge) ![Exports](https://img.shields.io/badge/Exports-HTML%20%7C%20XLSX%20%7C%20CSV-334155?style=for-the-badge)

[![Download](https://img.shields.io/badge/Download-Free%20on%20BlendKit-0B1F4D?style=for-the-badge)](https://www.blendkit.com/asset-gallery-detail/8225a754-32cd-482d-a0d3-84ea3850fc8f/) [![Issues](https://img.shields.io/badge/Support-Issues-1E5BFF?style=for-the-badge)](https://github.com/pacosalasv/DRH_Scene_Material_Inventory-Support/issues) [![Hub](https://img.shields.io/badge/DRH-Hub-334155?style=for-the-badge)](https://github.com/pacosalasv/DRH_Addons_Hub)

</div>

## The wall

A scene you built over three weeks. Forty materials, ninety images, half of them packed, two with paths pointing at a folder that moved. You export, the other artist opens it, and the shirt is pink.

Scene Material Inventory reads the scene and writes down what's there. Which materials exist, how many objects and slots use them, which node trees are reachable, what images they reference, whether those files resolve, and what the PBR maps look like. Then it hands you a report you can actually send.

<img src="docs/media/ScreenShot_01.png" alt="Scene material inventory panel" width="100%" />

## What the report covers

**Materials and where they're used.** Material names, datablock users, material-slot references, and object counts, so an unused material with 12 textures behind it stops being invisible.

**Shader internals.** Reachable node trees, shader types, node counts, nested groups, and Principled BSDF usage.

**Images.** Source type, resolution, packing state, alpha use, file size, and whether the file is missing.

**PBR maps.** Common map roles, the shader they feed, naming fallback for files that don't follow your convention, packed-map conventions, and color-space hints worth checking.

**Collections.** Optional per-collection material usage, useful when the scene is really six scenes pretending to be one.

Output goes to searchable HTML, a structured XLSX workbook, or CSV. Path sanitization is on by default, so a report you forward doesn't carry your local user directory with it. Report options can be saved as defaults and reapplied to other scenes.

## Who it's for

Freelancers handing files to clients. Studio artists inheriting someone else's scene. Pipeline and asset managers who need a list instead of a screenshot. Anyone who has ever said "it worked on my machine."

## Get it

Free on BlendKit, Blender 4.2 or newer. Pairs with [Color Ramp Studio](https://github.com/pacosalasv/DRH_Color_Ramp_Studio-Support) when the audit turns up ramps that need rebuilding.

[![Download on BlendKit](https://img.shields.io/badge/Get%20Scene%20Material%20Inventory-BlendKit-1597E5?style=for-the-badge&logo=blender)](https://www.blendkit.com/asset-gallery-detail/8225a754-32cd-482d-a0d3-84ea3850fc8f/)

Bugs and requests: [open an issue](https://github.com/pacosalasv/DRH_Scene_Material_Inventory-Support/issues)

<div align="center">
  <a href="https://ko-fi.com/pacosalasv">
    <img width="560" alt="Support on Ko-fi" src="docs/media/SupportMe.png" />
  </a>
</div>
