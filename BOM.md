## Bill of Materials (BOM)

**DC-12V Protection System** — component mapping from the original THT design (LTspice/KiCad) to the current SMT design (Altium, PCB layout).

| Ref | Type | Value | THT Part (Package) | SMT Part / MPN (Package) | Description |
|-----|------|-------|---------------------|----------------------------|--------------|
| M1 | PMOS | — | IRF4905 (TO-220AB) | IRF4905STRLPBF (D2PAK) | High-side power MOSFET |
| Q1 | PNP BJT | — | 2N3906 (TO-92) | MMBT3906 (SOT-23) | Gate pull-up (fast turn-off) |
| U1 | Comparator | — | LM393 (PDIP-8) | LM393D (SOIC-8) | Dual comparator (2nd half unused) |
| D1 | Schottky Diode | — | MBR745 (TO-220AC) | MBRB745 (SMB / DO-214AA) | Reverse polarity protection |
| D2 | Zener Diode | 15 V | 1N4744A (DO-41) | MMSZ5245B (SOD-123) | Gate-source protection |
| D3 | Zener Diode | 5.1 V | 1N4733A (DO-41) | MM1Z4733A (SOD-123FL) | Reference voltage |
| R1 | Resistor | 22 kΩ | Generic axial (THT) | RC0805FR-0722KL (0805) | Voltage divider (upper) |
| R2 | Resistor | 13 kΩ | Generic axial (THT) | RC0805FR-0713KL (0805) | Voltage divider (lower) |
| R3 | Resistor | 10 kΩ | Generic axial (THT) | RC0805FR-0710KL (0805) | Reference bias (Rref) |
| R4 | Resistor | 1 kΩ | Generic axial (THT) | RC0805FR-071KL (0805) | Zener bias (Rz) |
| R5 | Resistor | 600 kΩ* | Generic axial (THT) | RC0805FR-07590KL* (0805) | Hysteresis |
| R6 | Resistor | 10 kΩ | Generic axial (THT) | RC0805FR-0710KL (0805) | Comparator pull-up |
| R7 | Resistor | 4.7 kΩ | Generic axial (THT) | RC0805FR-074K7L (0805) | Base resistor (Q1) |
| R8 | Resistor | 36 kΩ | Generic axial (THT) | RC0805FR-0736KL (0805) | Gate pull-down |
| R9 | Resistor | 10 kΩ | Generic axial (THT) | RC0805FR-0710KL (0805) | Soft-start control |
| C1 | Capacitor | 100 nF | Generic ceramic (THT) | 08053C104KAT2A (0805) | Supply decoupling |
| C2 | Capacitor | 100 pF | Generic ceramic (THT) | TBD (0805) | Comparator compensation |
| C3 | Capacitor | 4.7 µF | Generic (THT) | CC1210KKX7R9BB475 (1210) | Soft-start timing |
| J1 | Connector | — | Screw Terminal | 282814-2 (THT, 2-pos) | Input (VIN) |
| J2 | Connector | — | Screw Terminal | 282814-2 (THT, 2-pos) | Output (VOUT) |

\* R5's nominal 600 kΩ is not a stocked standard value in Yageo's RC0805FR-07 (E96) series. The nearest real, in-stock part is 590 kΩ (~1.7% off nominal), used here as the practical substitute.

Note: J1/J2 remain THT screw terminals in the SMT revision — all other components were converted to SMD.
