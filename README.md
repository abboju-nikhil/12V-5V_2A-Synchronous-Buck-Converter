# 12 V to 5 V / 2 A Synchronous Buck Converter

A two-layer KiCad design for a synchronous DC-DC converter based on the Texas Instruments LMR33630ADDAR.

## Design targets

| Parameter | Target |
|---|---:|
| Input voltage range | 9–18 V DC |
| Nominal input | 12 V DC |
| Output voltage | 5 V DC |
| Output current | Up to 2 A |
| Switching frequency | 400 kHz |
| Target efficiency | 85% or higher |
| Target output ripple | Below 30 mV peak-to-peak |

Values in this table are design targets, not measured results. No efficiency, ripple, thermal, load-transient, or bench-validation report is included. The project has not been described as industrial-grade or production-qualified.

Review the schematic, layout, component ratings, and manufacturing outputs before fabrication or use. Gerber files are included, but have not been independently checked for manufacturing suitability in this review.

## Project contents

- `12V_5V_2A_Synchronous_Buck_converter.kicad_pro`, `.kicad_sch`, and `.kicad_pcb` — KiCad project, schematic, and board
- `BOM/` — bill of materials
- `Drill Files/` — drill outputs
- `Gerber files/` — board manufacturing layers
- `Layout/` — layer exports and board renders
- `Schematic/` — schematic PDF
- `3D_Image/` and `3D_Models/` — board render and component models
- `Symbol.Kicad_sym/` and `footprints.pretty/` — local KiCad libraries
- `pick and place files/` — component placement data
- `fp-lib-table` — KiCad footprint library table

## Tools

KiCad 10

## License

No license file is included. Do not assume reuse permissions; contact the author for permission.

**Author:** Abboju Nikhil
