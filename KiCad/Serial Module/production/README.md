# Serial Module: production files

Generated 2026-11-10 from `Serial Module.kicad_pcb`. DRC: 0 errors, 0 unconnected items, 0 schematic-parity issues, with the 0.09 mm minimum connection width enforced. 24 silkscreen warnings remain: outline overlaps between tightly packed parts.

## Files
| File | Use |
|---|---|
| `Serial Module gerbers.zip` | Upload to JLCPCB. Contains the six copper layers, masks, paste, silkscreen, outline, and PTH/NPTH Excellon drills (mm). |
| `gerbers/` | Same files, unzipped. |
| `jlcpcb_BOM.csv` | JLCPCB assembly BOM (Comment, Designator, Footprint, LCSC Part #). 44 lines, 557 placements. |
| `jlcpcb_CPL.csv` | JLCPCB pick-and-place (Designator, Mid X, Mid Y, Layer, Rotation). All parts are on the top side. |
| `BOM_full.csv` | Full BOM with manufacturer part numbers, including the 4 jumper shunts. |
| `Serial Module.step` | 3D assembly for the enclosure (DNP parts left out). |
| `Serial Module schematic.pdf` | Schematic. |

## Board order settings
- **Layers:** 6
- **Size:** 85 × 100 mm
- **Thickness:** 1.6 mm
- **Stackup:** 7628 prepreg (JLC06161H-7628 or equivalent)
- **Copper weight:** 1 oz outer, 0.5 oz inner
- **Surface finish:** HASL lead-free
- **Minimums:** 0.09 mm track, 0.1 mm clearance, 0.2 mm via drill with 0.45 mm pad
- **Via-in-pad:** 4 vias are epoxy-filled and capped. They sit next to QFN pads on CONFIG_OE_N and U18-QG. Choose "epoxy filled & capped" vias, which JLCPCB includes at no extra cost on 6-layer boards.

## Assembly notes
- **Hand-fit parts:** JS1–JS4 are 2.54 mm jumper shunts (C100114). They have no footprint, so they're left out of the JLC BOM and CPL. Fit them by hand on JP1–JP4.
- **Do not populate:** C114 and C135. They're excluded from the BOM and CPL.
- **No part to place:** J2 and J4 are Tag-Connect programming footprints.
- **Through-hole parts:** J1 (card connector), J3 (RJ45 2×4), J5 (terminal header) and JP1–JP4. Order through-hole assembly, or hand-solder them.
- **Rotations:** the CPL uses KiCad's rotations. Check part orientation in JLCPCB's placement preview before ordering, especially the SOT-23, SC-70, QFN and DHVQFN parts, whose zero orientation often differs from LCSC's.

## Stock check (LCSC, 2026-11-10)
- **TPS274160BRLHR** (U15, U19, U22, U23): 1 in stock, 4 needed per board.
- **SN74HCS596QPWRQ1** (U24, U25): 8 in stock, enough for 4 boards.
- **STM32F411RET6** (U1): 0 in stock.
- **Everything else:** in stock for at least 10 boards.
- **Part class:** all 46 parts are JLCPCB "Extended" parts.
