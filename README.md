# ⚡ Industrial 12V to 5V / 2A Synchronous Buck Converter

> High-efficiency synchronous DC-DC buck converter designed using **KiCad 10**, converting **9V–18V DC** to a regulated **5V / 2A** output using the **Texas Instruments LMR33630ADDAR** switching regulator.

---

# 📖 Overview

This project presents the design of an industrial-grade **12V to 5V synchronous buck converter** capable of delivering up to **2A continuous output current** with high efficiency and low output ripple. The converter is intended for embedded systems, industrial automation, robotics, automotive electronics, IoT devices, and battery-powered applications.

The design incorporates comprehensive protection circuitry, efficient power conversion, optimized filtering, and stable voltage regulation while following industry-standard PCB layout practices.

---

# 🎯 Design Specifications

| Parameter | Specification |
|-----------|---------------|
| Topology | Synchronous Buck Converter |
| Input Voltage | 9V–18V DC |
| Nominal Input | 12V DC |
| Output Voltage | 5V DC |
| Continuous Output Current | 2A |
| Peak Output Current | 2.5A |
| Switching Frequency | 400kHz |
| Controller | TI LMR33630ADDAR |
| PCB Layers | 2 Layer |
| Target Efficiency | ≥85% |
| Target Output Ripple | <30mVpp |

---

# 🏗 System Architecture

```
9V–18V DC Input
        │
        ▼
 Input Protection
(Fuse + TVS + Reverse Polarity)
        │
        ▼
 Input Filtering
        │
        ▼
LMR33630A Buck Controller
        │
        ▼
 Switching Stage
        │
        ▼
     10µH Inductor
        │
        ▼
 Output Capacitor Bank
        │
        ▼
 Feedback Network
        │
        ▼
 Stable 5V Output
```

---

# 🔋 Features

- Wide 9V–18V input voltage range
- Regulated 5V output
- Continuous 2A output current
- High-efficiency synchronous topology
- Reverse polarity protection
- TVS surge protection
- Input fuse protection
- Low output ripple
- Optimized LC output filtering
- Compact two-layer PCB
- Industrial-grade design

---

# ⚙ Functional Description

## 1. Input Protection Stage

The converter includes multiple protection mechanisms to improve reliability.

### Fuse (F1)

A 3A input fuse protects the circuit from excessive current and short-circuit conditions.

### Reverse Polarity Protection

A P-channel MOSFET (DMP3028LK3-13) prevents damage if the supply is connected with reversed polarity while maintaining minimal voltage drop.

### TVS Protection

A 12V TVS diode suppresses voltage spikes caused by hot plugging and transient events.

---

## 2. Input Filtering

Multiple ceramic and electrolytic capacitors reduce input ripple and provide a low-impedance source to the switching regulator.

Benefits include:

- Reduced input noise
- Improved transient response
- Lower EMI
- Stable converter operation

---

## 3. Buck Converter Controller

The converter uses the **Texas Instruments LMR33630ADDAR** synchronous switching regulator.

Key features include:

- Integrated high-side and low-side MOSFETs
- 3A output capability
- Wide input voltage range
- Current mode control
- Thermal shutdown
- Over-current protection
- High conversion efficiency

---

## 4. Bootstrap Circuit

A 100nF bootstrap capacitor supplies the internal high-side MOSFET driver, enabling efficient switching operation.

---

## 5. Inductor

A 10µH power inductor stores energy during switching cycles and smooths current delivered to the output.

Proper inductor selection minimizes ripple current and improves efficiency.

---

## 6. Output Filter

The output capacitor bank consists of multiple ceramic and electrolytic capacitors that provide:

- Low output ripple
- Stable voltage regulation
- Fast transient response
- Reduced switching noise

---

## 7. Feedback Network

The output voltage is regulated using a resistor divider connected to the FB pin.

| Component | Value |
|-----------|-------|
| R3 | 100kΩ |
| R4 | 24.9kΩ |
| C14 | 15pF |

The feedback loop continuously adjusts the PWM duty cycle to maintain a regulated 5V output.

---

# 🔄 Working Principle

1. The input voltage enters through the power connector.
2. The fuse protects against excessive current.
3. Reverse polarity protection prevents damage from incorrect wiring.
4. The TVS diode absorbs voltage transients.
5. Input capacitors filter supply noise.
6. The LMR33630A switches at approximately 400kHz.
7. The inductor stores and transfers energy.
8. Output capacitors smooth the switching waveform.
9. The feedback network regulates the output voltage to maintain a constant 5V.

---

# 📊 Expected Performance

| Parameter | Expected Value |
|-----------|----------------|
| Efficiency | 85–92% |
| Output Ripple | <30mVpp |
| Load Regulation | ±2% |
| Output Current | 0–2A |
| Switching Frequency | 400kHz |

---

# 🛠 PCB Design Considerations

- Use a solid ground plane.
- Keep the switching loop as small as possible.
- Place input capacitors close to the VIN pin.
- Place the bootstrap capacitor close to the controller.
- Route the feedback trace away from the switching node.
- Use wide copper pours for high-current paths.
- Minimize parasitic inductance.

---

# 📦 Major Components

| Reference | Component |
|-----------|-----------|
| U1 | TI LMR33630ADDAR |
| Q1 | DMP3028LK3-13 |
| L1 | 10µH Power Inductor |
| F1 | 3A Fuse |
| Z1 | 12V TVS Diode |
| D2 | 60V Schottky Diode |

---

# 🔬 Applications

- Embedded Systems
- Industrial Automation
- PLC Controllers
- Robotics
- IoT Devices
- Automotive Electronics
- Battery Management Systems
- Communication Equipment
- FPGA Development Boards
- Single Board Computers

---

# 📂 Repository Structure

```
Industrial-Buck-Converter/
│
├── Schematic/
│   └── Buck_Converter.kicad_sch
│
├── PCB/
│   └── Buck_Converter.kicad_pcb
│
├── Gerber/
│
├── BOM/
│
├── Images/
│   ├── Schematic.png
│   ├── PCB_Layout.png
│   └── 3D_Render.png
│
├── Datasheets/
│
└── README.md
```

---

# 🚀 Future Improvements

- Thermal analysis
- EMI optimization
- Efficiency measurements
- Load transient testing
- Current sensing
- Soft-start implementation
- Power Good monitoring
- Four-layer PCB version
- Automotive qualification

---

# 🧰 Software Used

- KiCad 10.0.3
- Texas Instruments Webench (Reference)
- LTspice (Optional Simulation)

---

# 👨‍💻 Author

**Abboju Nikhil**

M.Tech Power Electronics Engineer

### Areas of Interest

- Power Electronics
- DC-DC Converter Design
- PCB Design
- Embedded Hardware
- Industrial Electronics
- Control Systems

---

# ⭐ Project Highlights

- Industrial-grade synchronous buck converter
- Wide 9V–18V input operating range
- Stable regulated 5V / 2A output
- High-efficiency switching topology
- Low ripple output
- Reverse polarity and surge protection
- Designed using KiCad 10
- Optimized for embedded and industrial applications

---

## 📜 License

This project is released under the MIT License. Feel free to use, modify, and contribute while providing appropriate attribution.
