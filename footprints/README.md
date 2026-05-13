# Footprints

KiCad PCB footprints (`.pretty` directories containing `.kicad_mod` files).

---

## Naming convention

Use IPC-7351 naming where applicable:

`Package_Body-PinCount_WidthxHeightmm_PitchPmm`

Examples:
- `SOIC-8_3.9x4.9mm_P1.27mm`
- `QFN-32_5x5mm_P0.5mm`
- `0402_1005Metric`

---

## Required layers

Every footprint must include:

| Layer | Requirement |
|---|---|
| `F.Cu` (pads) | Correct pad size and shape per datasheet land pattern |
| `F.Courtyard` | Minimum clearance envelope — no overlap with adjacent components |
| `F.Fab` | Component outline at exact body dimensions |
| `F.Silkscreen` | Reference designator and component outline (must not overlap pads) |
| `F.Mask` | Solder mask (normally auto-generated from pad size) |

---

## Pad numbering

Pad numbering must match the symbol pin numbering exactly. Verify against the component datasheet.

---

## 3D model reference

Each footprint should reference the corresponding 3D model in `3d-models/`. Use a path relative to `${KIPRJMOD}`:

```
${KIPRJMOD}/../library/3d-models/SOIC-8_3.9x4.9mm_P1.27mm.step
```

---

## Adding a footprint

Work through the [component addition checklist](../checklists/component-addition.md) before opening a PR.
