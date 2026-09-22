<div align="center">
  <img width="680" alt="DRH - Scene Material Inventory banner" src="docs/media/Logo.png" />
</div>

<br>

<div align="center">

# DRH - Scene Material Inventory

### Public Support Hub · Documentation · Feedback · Blender 4.2+

**Audit scene materials, shader nodes, referenced images, and PBR maps, then export production-ready reports.**

![Status](https://img.shields.io/badge/status-Released-22C55E?style=for-the-badge)
![Version](https://img.shields.io/badge/version-1.0.0-00B7FF?style=for-the-badge)
![Blender](https://img.shields.io/badge/blender-4.2%2B-0B1F4D?style=for-the-badge)
![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux-EAF2FF?style=for-the-badge&labelColor=0B1F4D&color=EAF2FF)

<br>

**Part of the DRH Add-ons ecosystem - Blender tools, updates, and releases.**

[![DRH Add-ons Hub](https://img.shields.io/badge/DRH%20Add--ons%20Hub-Visit%20Hub-1E5BFF?style=for-the-badge&labelColor=0B1F4D)](https://github.com/pacosalasv/DRH_Addons_Hub)
[![DRH on BlendKit](https://img.shields.io/badge/BlendKit-DRH%20Profile-0B1F4D?style=for-the-badge)](https://www.blendkit.com/?query=author_id:205846)

</div>

---

<div align="center">

**DRH - Scene Material Inventory** is a material-auditing and reporting extension for Blender. It reviews scene materials, shader-node usage, referenced images, and common PBR map roles, then exports the results as HTML, XLSX, or CSV.

This repository is the public hub for documentation, support, issue tracking, compatibility feedback, and release notes. The installable add-on package is intentionally **not hosted in this GitHub repository**.

</div>

---

## Support DRH Development

If **DRH - Scene Material Inventory** is useful in your workflow, you can support ongoing DRH development on **Ko-fi**. Support is optional and helps fund maintenance, Blender compatibility work, documentation, testing, and future production tools.

<div align="center">
  <a href="https://ko-fi.com/pacosalasv">
    <img width="520" alt="Donate on Ko-fi to support DRH" src="docs/media/kofi_donate.png" />
  </a>
</div>

<div align="center">

[**Support DRH on Ko-fi**](https://ko-fi.com/pacosalasv)

</div>

---

<details>
  <summary><strong>📚 Table of Contents</strong></summary>

## Menu

- [Overview](#overview)
- [Media preview](#media-preview)
- [What it does](#what-it-does)
- [Key features](#key-features)
- [Export formats](#export-formats)
- [PBR map reporting](#pbr-map-reporting)
- [Accuracy and privacy](#accuracy-and-privacy)
- [Current status](#current-status)
- [Support and feedback](#support-and-feedback)
- [Availability](#availability)
- [Documentation](#documentation)
- [License](#license)

</details>

---

## Overview

**DRH - Scene Material Inventory** helps artists and technical users inspect material usage across a Blender scene without manually opening every material or shader graph.

The extension is designed for material review, look-development cleanup, asset validation, technical art, marketplace preparation, scene handoff, and production reporting.

**Location:** `3D Viewport > Sidebar > DRH Tools > Material Inventory`

## Media preview

> The product-specific media currently in this repository are labeled placeholders. Replace them with final captures when available.

<div align="center">
  <img width="920" alt="DRH - Scene Material Inventory feature preview placeholder" src="docs/media/Featured_Image.png" />
</div>

### Screenshots

| Material inventory | PBR map review |
|---|---|
| <img width="440" alt="Material inventory placeholder" src="docs/media/ScreenShot_01.png" /> | <img width="440" alt="PBR map review placeholder" src="docs/media/ScreenShot_02.png" /> |

| HTML reporting | XLSX / CSV reporting |
|---|---|
| <img width="440" alt="HTML report placeholder" src="docs/media/ScreenShot_03.png" /> | <img width="440" alt="Spreadsheet report placeholder" src="docs/media/ScreenShot_04.png" /> |

## What it does

The extension scans scene materials and reachable shader-node structures to build a deterministic inventory that can be reviewed directly through exported reports.

It can report:

- unique scene-object material usage
- Blender material user counts and material-slot references
- node-based material state and shader types
- image source details and missing-file checks
- optional per-collection material breakdown
- PBR map roles, traced shader targets, naming hints, packing hints, resolution, alpha usage, color-space review hints, and paths
- environment and report-generation context

## Key features

- Blender 4.2+ Extension package format
- recursive shader-node and nested node-group scanning
- Principled BSDF and shader-type reporting
- source-aware image auditing for generated/viewer, file-backed, packed, tiled/UDIM, movie, and sequence images
- deterministic material, image, object, and collection ordering
- connection-aware PBR role tracing with naming fallback
- recognition of common packed conventions such as ORM, ARM, RMA, and MRA
- conservative PBR color-space review hints
- path sanitization enabled by default
- no third-party Python runtime dependencies

## Export formats

### HTML

Self-contained DRH-styled report with search, filters, sortable columns, environment information, optional collection details, and an optional PBR Maps section.

### XLSX

Dependency-free Excel workbook with typed numeric cells, frozen headers, native Excel tables, optional PBR Maps sheet, and optional Collections sheet.

### CSV

UTF-8 BOM material inventory. When PBR details are enabled, a sibling `_PBR-Maps.csv` report is generated alongside the main CSV.

## PBR map reporting

When **Include image info** and **Include PBR map breakdown** are enabled, the scanner can identify common roles including:

- Base Color / Albedo / Diffuse
- Ambient Occlusion
- Metallic / Metalness
- Roughness / Glossiness
- Normal
- Height / Bump / Displacement
- Alpha / Opacity
- Emission
- Specular
- Transmission
- Subsurface
- Coat / Clearcoat
- Sheen
- Anisotropy
- Thin Film
- Cavity / Mask

Role detection uses actual shader-node connections when possible and image/node naming as a fallback or supplement. Inferred PBR roles and traced shader targets remain separate so ambiguous workflows stay visible for review.

## Accuracy and privacy

- Unique scene objects are counted separately from material-slot references.
- Reachable shader node groups are recursively scanned.
- UDIM `<UDIM>` and `<UVTILE>` paths use known Blender image tiles where available.
- Alpha use is based on linked Image Texture Alpha outputs.
- `Sanitize paths` is enabled by default and replaces the local home prefix with `%USERPROFILE%` on Windows or `~` on macOS/Linux.
- The operating-system username is not exported.
- Color Space Check results are review hints rather than hard errors because custom shader workflows can intentionally differ.

## Current status

- **Version:** `1.0.0`
- **Status:** Released
- **Minimum Blender version:** `4.2`
- **Package type:** Blender Extension
- **Runtime dependencies:** None outside Blender/Python standard functionality used by the extension

## Support and feedback

Use **GitHub Discussions** for questions, setup help, workflow guidance, and general suggestions.

Use **GitHub Issues** for reproducible bugs, regressions, compatibility problems, focused feature requests, or distribution/listing problems.

Please do not post confidential project files, account credentials, private customer data, or other sensitive production information.

## Availability

The installable add-on ZIP is **not stored in this GitHub support repository**.

DRH add-ons are distributed through the DRH marketplace/profile channels. See the current DRH listings on BlendKit:

- [Paco Salas | DRH on BlendKit](https://www.blendkit.com/?query=author_id:205846)
- [DRH Add-ons Hub](https://github.com/pacosalasv/DRH_Addons_Hub)

## Documentation

- [Support policy](SUPPORT.md)
- [Changelog](CHANGELOG.md)
- [User manual](docs/manual/user-manual.pdf)
- [Manual changelog](docs/manual/manual-changelog.md)

## License

The add-on is licensed under **GPL-3.0-or-later**. See [LICENSE](LICENSE).

---

Authored by **Paco Salas | DRH**.
