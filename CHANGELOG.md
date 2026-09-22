# Changelog

## 1.0.0 - Initial release

- Initial public release of DRH - Scene Material Inventory as a Blender Extension.
- Blender 4.2+ Extension package with `blender_manifest.toml`.
- DRH metadata and maintainer identity: `Paco Salas | DRH`.
- Material inventory with unique scene-object counts, Blend user counts, and material-slot reference counts.
- Recursive shader-node and node-group scanning.
- Principled BSDF detection and shader-type reporting.
- Source-aware image auditing for generated/viewer, file-backed, packed, tiled/UDIM, movie, and sequence images.
- Deterministic image/material/object/collection ordering.
- Optional PBR map breakdown subordinate to Image Info.
- Connection-aware PBR role tracing through nested node groups.
- PBR naming fallback and packed-channel recognition for common ORM/ARM/RMA/MRA conventions.
- PBR color-space review hints and per-material PBR summary fields.
- HTML export with DRH styling, search, filters, sorting, collapsible sections, and full-page background.
- XLSX export with typed numeric cells, frozen headers, native Excel tables, PBR Maps sheet, optional Collections sheet, and Excel-compatible table filters.
- CSV export with optional companion `_PBR-Maps.csv`.
- Optional per-collection material breakdown.
- Extension Preferences for default report options plus Load/Apply Defaults and Save Scene as Defaults.
- Direct GitHub and BlendKit links in Preferences.
- Path sanitization enabled by default.
- Blender `//` output-folder resolution.
- Clean `PropertyGroup` registration/unregistration lifecycle.
- No third-party Python runtime dependencies.
- GPL-3.0-or-later license.
