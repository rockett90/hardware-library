# 3D Models

3D model files for PCB visualisation and mechanical clearance checking.

---

## File formats

| Format | Use |
|---|---|
| `.step` (preferred) | Accurate geometry — use for all new models |
| `.wrl` | Legacy/visualisation only — acceptable if STEP is not available |

If only a `.wrl` is available, add it and note in the PR that STEP is unavailable.

---

## Naming convention

Match the footprint name exactly:

`SOIC-8_3.9x4.9mm_P1.27mm.step`

This allows KiCad to find the 3D model automatically when the footprint is used.

---

## Alignment

The model origin must align with the footprint origin:
- X/Y origin at the footprint anchor point
- Z origin at the top of the PCB surface (bottom of the component body)
- Rotation: pin 1 in the correct orientation per the footprint

Verify alignment visually in KiCad's 3D viewer before committing.

---

## Sources

Preferred sources (in order):
1. Manufacturer's official STEP model
2. [SnapEDA](https://www.snapeda.com)
3. [Ultra Librarian](https://www.ultralibrarian.com)
4. [GrabCAD](https://grabcad.com)
5. Generated from datasheet dimensions (note the source in the PR)

Always verify the model dimensions against the component datasheet.
