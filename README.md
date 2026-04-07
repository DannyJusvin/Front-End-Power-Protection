# 🔌 Front-End Power Protection System

### Discrete 12V DC Safeguard with Soft-Start Logic

---

## 📌 Overview

This project presents a **discrete front-end power protection circuit** designed for 12V DC systems. It protects sensitive electronics from unsafe input conditions using a **P-channel MOSFET-based high-side topology**.

The design integrates:

* Over-voltage protection (OVP) with hysteresis
* Reverse polarity protection
* Controlled soft-start to mitigate inrush current

The circuit was designed, simulated, and validated in **LTspice**, and documented with a complete engineering workflow.

---

## 🎯 Key Features

* ⚡ **Over-Voltage Protection (OVP)**

  * Trip: ~13.9 V
  * Release: ~13.3 V (hysteresis ≈ 0.6 V)

* 🔄 **Reverse Polarity Protection**

  * Implemented using a high-current Schottky diode (MBR745)

* ⏱️ **Soft-Start Control**

  * ~10–13 ms controlled ramp
  * Reduces inrush current stress

* ⚡ **Fast Protection Response**

  * ~1.6 µs detection and cutoff (comparator + gate drive)

---

## 🧠 Design Highlights

* Discrete implementation (no integrated protection ICs)
* Demonstrates:

  * Comparator-based decision making
  * Positive feedback (hysteresis)
  * MOSFET gate control dynamics
  * Real-world non-idealities (Zener knee region, MOSFET capacitances)

---

## 🧩 System Architecture

* Input Protection (Schottky diode)
* Power Switching (PMOS – IRF4905)
* Analog Control (LM393 comparator + reference + hysteresis)
* Gate Drive & Soft-Start (PNP + RC network + clamp)

---

## 📊 Performance Summary

| Parameter         | Value                            |
| ----------------- | -------------------------------- |
| Nominal Input     | 12 V                             |
| OVP Trip          | ~13.9 V                          |
| OVP Release       | ~13.3 V                          |
| Soft-Start Time   | ~10–13 ms                        |
| Response Time     | ~1.6 µs                          |
| Efficiency        | ~96%                             |
| Practical Current | ~2–3 A (continuous, no heatsink) |

---

## 🧪 Simulation & Validation

* LTspice transient simulations
* Tested scenarios:

  * Normal startup
  * Over-voltage event
  * Load variation (10Ω, 2Ω, 1Ω)
  * Reverse polarity

---

## ⚠️ Limitations

* No over-current protection (OCP)
* No under-voltage lockout (UVLO)
* Diode voltage drop reduces efficiency
* Zener-based reference has limited accuracy

---

## 🚀 Future Improvements

* Add current sensing (INA180 / shunt-based OCP)
* Replace Zener with precision reference (TL431)
* Use ideal diode MOSFET for lower loss
* Add UVLO and thermal protection

---

## 📁 Repository Contents

* KiCad schematic (PDF)
* LTspice simulation files
* Block diagram
* Waveform results
* Full project documentation (PDF)
* Project Log
* BOM	

---

## 🛠 Tools Used

* LTspice (Simulation)
* KiCad (Schematic)
* draw.io (Block Diagram)

---

## 💡 Author Note

This project was developed to deeply understand **analog power protection design**, including transient behavior, feedback systems, and real-world component limitations.

---
