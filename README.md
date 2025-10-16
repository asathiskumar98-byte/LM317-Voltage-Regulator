## ⚡ LM317 Adjustable Voltage Regulator

This project is a **variable DC voltage regulator** built around the **LM317T** IC.  
It converts an unregulated DC or AC input into a smooth, adjustable DC output using a bridge rectifier, filter capacitors, and precision voltage control components.

The design is ideal for powering microcontroller circuits, sensors, and embedded systems where variable regulated power is required.

---

### 🔍 Features

- Input: 12V–24V DC or AC (via bridge rectifier)
- Output: Adjustable **1.25V to ~12V DC** (using potentiometer)
- Current: Up to **1.5A** (with proper heatsink)
- Built-in short-circuit and thermal protection
- Clean output with low ripple and noise
- Compact, single-sided PCB layout suitable for hobby or lab use

---

### 🧾 Components List (PCB Labels)

| **Name** | **Value** | **PCB Label** | **Description / Function** |
|-----------|------------|----------------|-----------------------------|
| J1 | Screw_Terminal_2Pin | **IN** | DC Input terminal (AC or DC supply) |
| D1 | B40C2300-1500A | **BR1** | Bridge rectifier – converts AC to DC |
| C1 | 1000µF / 25V | **C1** | Input filter capacitor – smooths rectified voltage |
| C2 | 0.1µF | **C2** | Ceramic decoupling capacitor (stabilizes LM317 input) |
| U1 | LM317T | **U1** | Adjustable voltage regulator IC |
| C3 | 10µF / 25V | **C3** | Capacitor between Adj & GND – improves regulation |
| RV1 | 5kΩ / 10kΩ | **VR1** | Potentiometer – adjusts output voltage |
| R1 | 220Ω / 240Ω | **R1** | Fixed resistor – sets reference voltage with VR1 |
| C4 | 0.1µF | **C4** | Ceramic capacitor at output – reduces noise |
| C5 | 470µF / 25V | **C5** | Output filter capacitor – smooth DC output |
| J2 | Screw_Terminal_2Pin | **OUT** | DC Output terminal (regulated output) |

---

### 🧠 Circuit Overview

The **bridge rectifier (BR1)** converts AC input into DC, filtered by **C1** and **C2**.  
The **LM317T (U1)** regulates the voltage, with **R1** and **VR1** forming an adjustable divider to set the output voltage.  
**C3**, **C4**, and **C5** provide additional stability and reduce output ripple.  

Output voltage can be varied using the potentiometer **VR1**:[\
V_{OUT} = 1.25 \times \left(1 + \frac{R1}{VR1}\right)
\]

---

### 🧰 Applications

- Embedded and IoT development boards  
- Sensor testing and prototyping  
- Variable bench power supply  
- Educational / DIY electronics labs  

---

### 🪛 Notes

- Use a **heat sink** with the LM317 if load current > 500 mA.  
- Ensure capacitors have voltage ratings at least **25–35% higher** than the input voltage.  
- Connect all grounds to a **common GND plane** on the PCB for stability.  

---

💡 *Designed with KiCad 9 — clean schematic, simple routing, and ready for fabrication.*
