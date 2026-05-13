# Symbols

KiCad schematic symbols (`.kicad_sym` files).

---

## Naming convention

`Manufacturer_PartNumber`

Examples: `TI_OPA2134`, `Microchip_MCP3204`, `ST_STM32F103C8T6`

Use the manufacturer's official part number. Do not abbreviate or paraphrase.

---

## Required fields

Every symbol must have these fields populated:

| Field | Description | Example |
|---|---|---|
| `Value` | Bare part number (without manufacturer prefix) | `OPA2134` |
| `Footprint` | Library-relative footprint reference | `library:SOIC-8_3.9x4.9mm_P1.27mm` |
| `MPN` | Full manufacturer part number | `OPA2134PA` |
| `Datasheet` | URL to the manufacturer's datasheet | `https://www.ti.com/lit/ds/...` |
| `Manufacturer` | Manufacturer name | `Texas Instruments` |
| `SPICE_Model` | Path to SPICE model (if available) | `${KIPRJMOD}/../library/spice-models/active/TI_OPA2134.lib` |

---

## Library file structure

Symbols are grouped into `.kicad_sym` files by manufacturer or component category. Do not create a new `.kicad_sym` file per component — add to the appropriate existing file.

---

## Adding a symbol

Work through the [component addition checklist](../checklists/component-addition.md) before opening a PR.
