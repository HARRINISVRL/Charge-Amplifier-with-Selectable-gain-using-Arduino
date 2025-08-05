# 📡 Charge Amplifier with Selectable Gain using Arduino
This project implements a charge amplifier circuit interfaced with an Arduino to allow dynamic selection of gain using software. It is particularly useful for interfacing with piezoelectric sensors and other charge-based signal sources in precision measurement or sensing systems.

## 🔧 Features
- ✅ Charge amplifier design with capacitor feedback
- ✅ Gain selection via digital control using Arduino
- ✅ Selectable gain stages: High, Medium, Low
- ✅ Analog signal readout and plotting via Serial Monitor / Python GUI
- ✅ Ideal for piezoelectric sensors, force transducers, and vibration monitoring

## 🧰 Hardware Requirements
| Component                                 | Quantity |
| ----------------------------------------- | -------- |
| Arduino Uno / Nano / Mega                 | 1        |
| TL072 / TL074 Op-Amp                      | 1        |
| Ceramic capacitors (1nF, 10nF, 100nF)     | 1 each   |
| Resistors (10kΩ, 100kΩ, 1MΩ)              | 1 each   |
| N-channel MOSFETs / Analog switches       | 3        |
| Breadboard and jumper wires               | -        |
| Power supply (5V or dual ±12V for op-amp) | 1        |

# ⚙️ Circuit Description

The charge amplifier converts a small charge \( Q \) input into a voltage output:

$$ 
V_{\text{out}} = \frac{Q}{C_f} 
$$

where \( C_f \) is the feedback capacitance. By switching between multiple capacitors (\( C_1, C_2, C_3 \)), the gain can be altered. Arduino controls these capacitors via digital I/O, using MOSFETs or analog switches to connect/disconnect them.
