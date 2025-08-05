# ⚡ Voltage Gain Controller using Arduino

Measure. Calculate. Control.  
A minimal yet powerful Arduino-based system that lets you measure voltage, calculate gain, and switch outputs—all through a serial interface.

---

## 🚀 Project Overview

This project is a simple but effective tool to:

✅ Read analog voltage from a sensor or input source  
✅ Calculate gain based on user-defined input voltage  
✅ Control output pins to select gain modes (or any user-defined function)  
✅ Interact via **Serial commands** (compatible with Serial Monitor or Nextion displays)

---

## 🧠 How It Works

### 📥 Input
- Analog voltage is read from **A7**
- Input voltage is entered via Serial

### 📤 Output
- Output voltage (`Vout`) is printed on command
- Gain = Vout / Vin is calculated
- Based on selection, **one of D2–D5** is set HIGH (others LOW)

---

## 🔧 Supported Serial Commands

| 🔤 Command | 🧾 Description |
|-----------|----------------|
| `Vout`    | Displays the real-time analog voltage at pin A7 |
| `input`   | Takes user input voltage after delay, calculates and prints gain |
| `gain`    | Waits for value `1` to `4` and activates corresponding digital output |

### 📟 Example Usage

```plaintext
> Vout
< t1.txt="3.12 V"

> input
(wait 5 sec...)
> 2.00
< t6.txt="1.56"

> gain
(wait 3 sec...)
> 2
(Output pin D3 is set HIGH, others LOW)
```

<img width="857" alt="image" src="https://github.com/user-attachments/assets/e8854b88-c2a2-485b-bc1c-0df9b221f8ea" />

![WhatsApp Image 2025-04-10 at 11 48 17_c4eb3015](https://github.com/user-attachments/assets/52b8c595-f0a0-4259-915e-a7202dc74503)
![WhatsApp Image 2025-04-10 at 11 48 33_d62d58b5](https://github.com/user-attachments/assets/940c978e-b586-4148-b7e8-4d81cff3cca5)
![WhatsApp Image 2025-04-10 at 11 49 05_93c8d874](https://github.com/user-attachments/assets/ff3962e8-d0c9-4c83-b124-9f094e494d70)
