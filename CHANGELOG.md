# Changelog

## 1.0.0 - Revision candidate

Status: **Under revision (not approved yet)**.

This candidate documents the feature set submitted for review. It is not described as an approved public release until marketplace approval is complete.

- Blender 4.2+ Extension package with `blender_manifest.toml`.
- Material inventory with unique scene-object counts, Blender material user counts, and material-slot reference counts.
- Recursive shader-node and node-group scanning.
- Principled BSDF detection and shader-type reporting.
- Source-aware image auditing for generated/viewer, file-backed, packed, tiled/UDIM, movie, and sequence images.
- Deterministic image, material, object, and collection ordering.
- Optional PBR map breakdown subordinate to Image Info.
- Connection-aware PBR role tracing through nested node groups.
- PBR naming fallback and packed-channel recognition for common ORM/ARM/RMA/MRA conventions.
- PBR color-space review hints and per-material PBR summary fields.
- HTML export with search, filters, sorting, collapsible sections, and DRH styling.
- XLSX export with typed numeric cells, frozen headers, native Excel tables, optional PBR Maps sheet, and optional Collections sheet.
- CSV export with optional companion `_PBR-Maps.csv`.
- Optional per-collection material breakdown.
- Extension Preferences for default report options plus Load/Apply Defaults and Save Scene as Defaults.
- Path sanitization enabled by default.
- Blender `//` output-folder resolution.
- Clean `PropertyGroup` registration/unregistration lifecycle.
- No third-party Python runtime dependencies.
- GPL-3.0-or-later license.
