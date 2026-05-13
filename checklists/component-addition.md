# Component Addition Checklist

> Use this checklist when raising a PR to add a new component to the shared library.

## Symbol

- [ ] Symbol created in correct library file
- [ ] All required fields populated (Value, Footprint, MPN, Datasheet)
- [ ] Symbol passes ERC

## Footprint

- [ ] Footprint created in correct `.pretty` directory
- [ ] Courtyard, fab, silkscreen layers correct
- [ ] Pad numbering matches symbol

## SPICE Model (if applicable)

- [ ] SPICE model added to `spice-models/`
- [ ] Model referenced in symbol

## Sign-off

- [ ] Reviewed by lead before merge
