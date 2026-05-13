# hardware-library

Shared KiCad component library for hardware feature repositories.

Used as a git submodule at `library/` in feature repositories. The exact commit is pinned in each feature's `reviews/library.lock` file at CDR gate.

---

## Contents

| Directory | Contents |
|---|---|
| [`symbols/`](symbols/README.md) | KiCad schematic symbols (`.kicad_sym`) |
| [`footprints/`](footprints/README.md) | KiCad PCB footprints (`.pretty`) |
| [`3d-models/`](3d-models/README.md) | 3D model files (`.step`, `.wrl`) |
| [`spice-models/`](spice-models/README.md) | SPICE simulation models |

---

## Naming conventions

| Type | Convention | Example |
|---|---|---|
| Symbol | `Manufacturer_PartNumber` | `TI_OPA2134`, `MCP3204` |
| Footprint | IPC-7351 where applicable | `SOIC-8_3.9x4.9mm_P1.27mm` |
| 3D model | Match footprint name exactly | `SOIC-8_3.9x4.9mm_P1.27mm.step` |
| SPICE model | `Manufacturer_PartNumber.lib` or `.sub` | `TI_OPA2134.lib` |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full contribution process.

Use the appropriate checklist when raising a PR:
- [Component addition checklist](checklists/component-addition.md) — adding a new symbol, footprint, 3D model, or SPICE model
- [Component update checklist](checklists/component-update.md) — correcting or updating an existing component
- [Library review checklist](checklists/library-review.md) — for reviewers

---

## Versioning

This library uses [Conventional Commits](https://www.conventionalcommits.org/) and [release-please](https://github.com/googleapis/release-please) for changelog generation.

| Commit type | Meaning | Version bump |
|---|---|---|
| `feat:` | New component added | Minor |
| `fix:` | Correction to existing component | Patch |
| `refactor:` | Internal reorganisation, no functional change | Patch |
| `feat!:` or `fix!:` | Breaking change (rename, pad change, removal) | Major |

Release tags (`library-vX.Y.Z`) are created when the release-please Release PR is merged. This is done periodically — not on every commit. Traceability between a feature and the library version it used is maintained by `reviews/library.lock` in the feature repository, which records the exact commit SHA.

---

## Submodule usage

Feature repositories reference this library as a git submodule. See the feature repository's `docs/how-to/library-submodule.md` for guidance on updating the submodule pointer and understanding library.lock.
