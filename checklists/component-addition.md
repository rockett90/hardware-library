# Component Addition Checklist

> Work through this checklist when raising a PR to add a new component to the shared library.
> Tick every item. If an item does not apply (e.g. no SPICE model available), tick it and add a note.

## Naming

- [ ] Symbol name follows `Manufacturer_PartNumber` convention
- [ ] Footprint name follows IPC-7351 convention where applicable
- [ ] 3D model name matches footprint name exactly

## Symbol

- [ ] Symbol created in the correct `.kicad_sym` library file (not a new file per component)
- [ ] All required fields populated: `Value`, `Footprint`, `MPN`, `Datasheet` (URL), `Manufacturer`
- [ ] Datasheet URL is valid and points to the correct document
- [ ] Footprint reference is correct and the footprint exists in this library
- [ ] `SPICE_Model` field populated if a SPICE model is being added
- [ ] Symbol passes KiCad ERC with zero errors

## Footprint

- [ ] Footprint created in the correct `.pretty` directory
- [ ] Pad dimensions match the datasheet recommended land pattern
- [ ] Pad numbering matches symbol pin numbering
- [ ] `F.Courtyard` layer present — no overlap with adjacent standard component spacing
- [ ] `F.Fab` layer shows component body at correct dimensions
- [ ] `F.Silkscreen` does not overlap pads
- [ ] 3D model reference added and path is correct

## 3D model

- [ ] 3D model file added (`.step` preferred, `.wrl` acceptable)
- [ ] Model dimensions verified against datasheet
- [ ] Model origin and rotation aligned correctly (verified in KiCad 3D viewer)

## SPICE model (if applicable — tick and note N/A if not)

- [ ] Model file added to correct subdirectory (`passive/`, `active/`, or `ic/`)
- [ ] Model source noted in a comment at the top of the file
- [ ] Model tested in a minimal simulation — no convergence errors
- [ ] Model referenced in symbol `SPICE_Model` field

## Sign-off

- [ ] PR description includes the component name, MPN, and datasheet link
- [ ] Reviewed and approved by at least one CODEOWNER before merge
