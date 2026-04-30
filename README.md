# hardware-library

Shared KiCad component library.

## Contents

- **Symbols** (`.kicad_sym`) — schematic symbols
- **Footprints** (`.pretty`) — PCB footprints
- **3D Models** (`.3dshapes`) — 3D model files
- **Spice Models** — simulation models
  - `spice-models/passive/` — passive components
  - `spice-models/active/` — active components
  - `spice-models/ic/` — integrated circuits

## Usage

Referenced as a git submodule at `library/` in the features repo.

## Adding Components

Open a PR with changes under `library/<description>`. Review is required before merging.

## Versioning

- **PATCH** — correction to an existing component
- **MINOR** — new component added
- **MAJOR** — breaking change
