# Library Review Checklist

> For reviewers. Work through this checklist when reviewing a library PR.

## Naming and structure

- [ ] Component name follows the naming convention (`Manufacturer_PartNumber`)
- [ ] Component is in the correct file or directory
- [ ] No duplicate of an existing component under a different name

## Symbol review

- [ ] All required fields present and correctly populated
- [ ] Datasheet URL opens and points to the correct document
- [ ] MPN is correct and unambiguous
- [ ] Footprint reference resolves to an existing footprint in this library
- [ ] ERC passes

## Footprint review

- [ ] Pad dimensions match the datasheet land pattern
- [ ] Pad numbering matches the symbol
- [ ] Courtyard is present and reasonable
- [ ] Fab layer shows correct body outline
- [ ] Silkscreen does not overlap pads

## 3D model review

- [ ] File is STEP format (or WRL with justification)
- [ ] Model name matches footprint name
- [ ] Alignment looks correct in 3D viewer

## SPICE model review (if included)

- [ ] Source is noted in the file
- [ ] Model is in the correct subdirectory

## Breaking change review (if applicable)

- [ ] Change is clearly described as breaking in PR description
- [ ] Affected feature repositories are identified

## Final

- [ ] LIBRARY_CHANGELOG.md will be updated automatically by release-please — no manual edit needed
- [ ] Approve and merge
