# SPICE Models

SPICE simulation models for schematic simulation.

---

## Directory structure

```
spice-models/
├── passive/      — resistors, capacitors, inductors, diodes
├── active/       — transistors, op-amps, comparators
└── ic/           — integrated circuits, regulators, converters
```

---

## Naming convention

`Manufacturer_PartNumber.lib` or `Manufacturer_PartNumber.sub`

Examples: `TI_OPA2134.lib`, `ON_BC847.sub`

---

## Required before adding a model

- [ ] Model simulates correctly in a minimal test circuit (DC operating point and/or AC sweep as appropriate)
- [ ] Model source is noted in a comment at the top of the file
- [ ] Model is referenced in the corresponding symbol's `SPICE_Model` field

## Model sources

Preferred sources (in order):
1. Manufacturer's official SPICE model
2. SPICE model from a reputable distributor (Mouser, Digi-Key)
3. Community model — note the source and validate carefully

Always run a basic simulation to verify the model behaves plausibly before committing.
