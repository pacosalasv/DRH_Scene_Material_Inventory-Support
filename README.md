<div align="center">
  <img width="680" alt="DRH - Scene Material Inventory banner" src="docs/media/Logo.png" />

# DRH - Scene Material Inventory

### Support · Documentation · Review feedback · Blender 4.2+

Audit scene materials, shader nodes, referenced images, PBR maps, and exportable project reports.

![Status](https://img.shields.io/badge/status-Under%20revision%20%28not%20approved%20yet%29-F59E0B?style=for-the-badge)
![Version](https://img.shields.io/badge/version-1.0.0%20candidate-00B7FF?style=for-the-badge)
![Blender](https://img.shields.io/badge/blender-4.2%2B-0B1F4D?style=for-the-badge)

[![DRH Add-ons Hub](https://img.shields.io/badge/DRH%20Add--ons%20Hub-Catalog-1E5BFF?style=for-the-badge&labelColor=0B1F4D)](https://github.com/pacosalasv/DRH_Addons_Hub)
</div>

> **Current status:** **Under revision (not approved yet).** This repository documents the submitted candidate and provides a place for support/review feedback. It does not represent an approved BlendKit release, and no installable ZIP is hosted here.

## Overview

DRH - Scene Material Inventory is a Blender material-auditing and reporting extension designed to inspect material usage across a scene without manually opening every material or shader graph.

It can inventory materials, reachable shader nodes, referenced images, common PBR map roles, and collection usage, then export review data as HTML, XLSX, or CSV.

**Location:** `3D Viewport > Sidebar > DRH Tools > Material Inventory`

## Media preview

> The product-specific media currently in this repository are placeholders and can be replaced with final review-approved captures.

<div align="center">
  <img width="920" alt="DRH - Scene Material Inventory feature preview placeholder" src="docs/media/Featured_Image.png" />
</div>

### Screenshots

| Material inventory | PBR map review |
|---|---|
| <img width="440" alt="Material inventory placeholder" src="docs/media/ScreenShot_01.png" /> | <img width="440" alt="PBR map review placeholder" src="docs/media/ScreenShot_02.png" /> |

## What it reviews

| Area | Report coverage |
|---|---|
| Material usage | Unique scene-object use, Blender material users, and material-slot references. |
| Shader structure | Node-based state, shader types, reachable node groups, and Principled BSDF use. |
| Images | Source type, dimensions when available, packing/file information, missing-file checks, and sanitized paths. |
| PBR maps | Common map roles, traced shader targets, naming hints, packed-channel hints, alpha use, and color-space review hints. |
| Collections | Optional per-collection material breakdown. |
| Environment | Blender/report context useful for handoff and review. |

## Export formats

- **HTML** — self-contained DRH-styled report with search, filters, sorting, environment information, and optional PBR/collection sections.
- **XLSX** — dependency-free workbook with typed numeric cells, frozen headers, native Excel tables, and optional PBR/collection sheets.
- **CSV** — UTF-8 BOM material inventory with an optional companion `_PBR-Maps.csv`.

## Technical scope

| Item | Details |
|---|---|
| Blender | 4.2+ |
| Candidate version | 1.0.0 |
| Status | **Under revision (not approved yet)** |
| Package format | Blender Extension candidate |
| Runtime dependencies | None outside Blender/Python standard functionality used by the extension |
| Privacy | Path sanitization is enabled by default; the operating-system username is not exported |
| Distribution | No approved BlendKit product page is linked until review is complete |

PBR role detection uses shader-node connections when possible and naming as a fallback or supplement. Color-space checks are review hints rather than hard errors because custom shader workflows can intentionally differ.


## Availability

**BlendKit approval is still pending.** Until the add-on is approved, this repository intentionally avoids presenting a generic author-profile link as if it were a product download.

For the released DRH catalog, visit:

- [DRH Add-ons Hub](https://github.com/pacosalasv/DRH_Addons_Hub)
- [Paco Salas | DRH on BlendKit](https://www.blendkit.com/?query=author_id:205846)

## Documentation

- [User manual](docs/manual/user-manual.pdf)
- [Manual changelog](docs/manual/manual-changelog.md)
- [Product changelog](CHANGELOG.md)
- [Support guide](SUPPORT.md)

## Support

Use [GitHub Discussions](https://github.com/pacosalasv/DRH_Scene_Material_Inventory-Support/discussions) for setup questions, workflow guidance, usage help, and general feedback. Use [GitHub Issues](https://github.com/pacosalasv/DRH_Scene_Material_Inventory-Support/issues/new/choose) for reproducible bugs, regressions, compatibility problems, and focused feature requests.

See [SUPPORT.md](SUPPORT.md) for the shared DRH support format, the information to include in a report, and public-information guidance.

## Support DRH development

DRH development support is optional. Ko-fi contributions help cover maintenance, Blender compatibility work, documentation, testing, and continued development of free tools.

<div align="center">
  <a href="https://ko-fi.com/pacosalasv">
    <img width="520" alt="Support DRH development on Ko-fi" src="docs/media/kofi_donate.png" />
  </a>
</div>

## Ecosystem links

- [DRH Add-ons Hub](https://github.com/pacosalasv/DRH_Addons_Hub)
- [DRH catalog on BlendKit](https://www.blendkit.com/?query=author_id:205846)
- [Paco Salas | DRH on GitHub](https://github.com/pacosalasv)
- [Ko-fi](https://ko-fi.com/pacosalasv)

## License

This repository is distributed under GPL-3.0-or-later. See [LICENSE](LICENSE).

---

Authored by Paco Salas | DRH.
