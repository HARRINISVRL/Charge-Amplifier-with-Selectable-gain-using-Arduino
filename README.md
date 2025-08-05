# ⚡ Charge Amplifier with Selectable Gain using Arduino

A smart, scalable **charge amplifier** project built around the Arduino Mega and Nextion touchscreen interface. Designed primarily for **Faraday Cup** current measurement, this amplifier converts extremely low input currents into measurable voltages and features **software-controlled selectable gain**.

---

## 🎯 Project Objective

To build a current-to-voltage **charge amplifier** with **selectable gain**, enabling users to switch amplification levels using a **Graphical User Interface (GUI)**. The aim is to accurately measure input currents (such as from a Faraday Cup) and adjust gain dynamically via the GUI.

---

## 🔬 Application: Faraday Cup

A **Faraday Cup** is an instrument used to detect and measure the charge of a beam of charged particles (ions/electrons). When the beam hits the isolated metal cup, it accumulates charge which produces a tiny current. This current is often in the **pico-ampere to nano-ampere range**.

A **charge amplifier** boosts this signal by integrating the input current and producing a voltage proportional to the total charge received. This project does exactly that:

* Reads current from the Faraday Cup
* Converts it to voltage via a charge amplifier
* Uses an Arduino Mega for data processing
* Enables **gain control via GUI** on a Nextion Display

---

## 🔧 Components Used

| Component                             | Description                                                                                                          |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **LM358AD**                           | Dual op-amp used for signal amplification. Works with single or dual power supplies.                                 |
| **HEF4066BT**                         | Quad analog switch for selecting different gain resistors in the feedback path. Controlled digitally by Arduino.     |
| **Arduino Mega**                      | Microcontroller with ample I/O and memory to handle analog reads, control logic, and GUI communication.              |
| **Nextion Display (NX8048P070-011C)** | 7" TFT touchscreen used to interact with the circuit. Users can select gain and monitor voltage values in real-time. |
| **Nextion Editor**                    | Software used to design and program the touchscreen GUI.                                                             |
| **Ceramic Capacitors**                | 1nF, 10nF, 100nF - for filtering and integrating current signals.                                                    |
| **Resistors**                         | 10kΩ, 100kΩ, 1MΩ - used in gain selection.                                                                           |

---

## 🖥️ Features

* 📊 Real-time current-to-voltage conversion and display
* 🔁 Multiple gain levels selectable via touchscreen
* 🧪 Suitable for precision measurements from Faraday Cups
* 🔋 Low-power op-amp based design
* 🛠 Modular and extendable with more gain levels or digital output

---

## 🧱 Project Implementation

1. **Hardware**: Op-amp configured as charge amplifier with selectable feedback resistors.
2. **Analog Switch**: Controlled by Arduino to change feedback resistor, altering the gain.
3. **Microcontroller**: Arduino reads amplified signal and controls switch states.
4. **GUI**: Built using Nextion Editor and displayed on a Nextion touchscreen.

Users interact with the GUI to select gain. The system then adjusts the HEF4066BT switch accordingly, changing the feedback resistance and therefore the amplification factor.

---

## 📂 Repository Structure

```
Charge-Amplifier-with-Selectable-gain-using-Arduino/
├── ArduinoCode/
│   └── amplifier.ino
├── GUI/
│   └── nextion_gui.hmi
├── Docs/
│   └── schematic.pdf
│   └── block_diagram.png
├── LICENSE
└── README.md
```

---

## 🚀 Getting Started

1. **Assemble the circuit** using the provided schematic.
2. **Upload the Arduino code** (`amplifier.ino`) using the Arduino IDE.
3. **Flash the GUI** to the Nextion display using Nextion Editor.
4. **Power up and interact** with the touchscreen to select gain.

---

## 📈 Future Improvements

* Auto-ranging based on input current
* Data logging via SD card or IoT
* Wireless gain switching (BLE or Wi-Fi)
* Improved noise filtering for ultra-low current sources

---

## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---


---

> "Measuring the invisible currents that shape the future of particle science."
