## Bill of Materials (BOM)

| Ref | Component Type | Value / Part Number | Description |
|-----|--------------|--------------------|------------|
| M1 | PMOS | IRF4905 | High-side power MOSFET |
| Q1 | PNP BJT | 2N3906 | Gate pull-up (fast turn-off) |
| U1 | Comparator | LM393 | Dual comparator (single used) |
| D1 | Schottky Diode | MBR745 | Reverse polarity protection |
| D2 | Zener Diode | 1N4744A (15 V) | Gate-source protection |
| D3 | Zener Diode | 1N4733A (5.1 V) | Reference voltage |

| R1 | Resistor | 68 kΩ | Voltage divider (upper) |
| R2 | Resistor | 39 kΩ | Voltage divider (lower) |
| R3 | Resistor | 10 kΩ | Reference bias (Rref) |
| R4 | Resistor | 4.7 kΩ | Zener bias (Rz) |
| R5 | Resistor | 600 kΩ | Hysteresis |
| R6 | Resistor | 10 kΩ | Comparator pull-up |
| R7 | Resistor | 4.7 kΩ | Base resistor (Q1) |
| R8 | Resistor | 36 kΩ | Gate pull-down |
| R9 | Resistor | 10 kΩ | Soft-start control |

| C1 | Capacitor | 100 nF | Supply decoupling |
| C2 | Capacitor | 100 pF | Comparator compensation |
| C3 | Capacitor | 4.7 µF | Soft-start timing |

| J1 | Connector | Screw Terminal | Input (VIN) |
| J2 | Connector | Screw Terminal | Output (VOUT) |