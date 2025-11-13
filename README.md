# Gesture-Controlled-Music-Player
# Gesture-Controlled Music Player using Arduino UNO

## 1. Project Overview
This project is a **Gesture-Controlled Music Player** built using **Arduino UNO**, **DFPlayer Mini MP3 Module**, **Ultrasonic Sensors (HC-SR04)**, and a **speaker**.  
The system detects hand gestures using ultrasonic sensors to control music playback — such as **play/pause**, **volume up**, **volume down**, and **switching between previous/next songs**.

---

## 2. Required Components
- Arduino UNO (1 piece)  
- DFPlayer Mini MP3 Player Module (1 piece)  
- HC-SR04 Ultrasonic Sensor (4 pieces)  
- Speaker (8Ω, 3W) (1 piece)  
- Micro SD Card (with MP3 files named `001.mp3`, `002.mp3`, etc.)  
- Jumper Wires (male-to-male, male-to-female as needed)  
- Breadboard (optional)  
- 5V Power Supply or USB Power  

---

## 3. Sensor Function Mapping
The project uses **4 ultrasonic sensors**, each performing a specific control function:

| Sensor | Function       | Trig Pin | Echo Pin | Description |
|:------:|----------------|:--------:|:--------:|-------------|
| 1 | Play / Pause | 2 | 3 | Hand near (≤15 cm) toggles play/pause |
| 2 | Volume Up | 4 | 5 | Hand near (≤15 cm) increases volume |
| 3 | Volume Down | 6 | 7 | Hand near (≤15 cm) decreases volume |
| 4 | Previous / Next | 8 | 9 | ≤10 cm → Previous song<br>≥20 cm → Next song |

---

## 4. Wiring and Pin Connections

### DFPlayer Mini → Arduino UNO
| DFPlayer Pin | Arduino Pin |
|:-------------|:------------|
| VCC | 5V |
| GND | GND |
| TX | Pin 10 |
| RX | Pin 11 |
| SPK_1 | Speaker (+) |
| SPK_2 | Speaker (–) |

---

### Ultrasonic Sensors (HC-SR04) → Arduino UNO
| Sensor | Trig | Echo |
|:-------|:----:|:----:|
| 1 | 2 | 3 |
| 2 | 4 | 5 |
| 3 | 6 | 7 |
| 4 | 8 | 9 |

**All VCC → 5V**  
**All GND → GND**

---

## 5. Testing and Usage
- **Sensor 1 (Play/Pause):** Place your hand near (≤15 cm)  
- **Sensor 2 (Volume Up):** Place your hand near (≤15 cm)  
- **Sensor 3 (Volume Down):** Place your hand near (≤15 cm)  
- **Sensor 4 (Track Control):**  
  - Hand close (≤10 cm) → **Previous Song**  
  - Hand far (20–40 cm) → **Next Song**

> 💡 **Note:** Ensure your SD card contains MP3 files named sequentially as `001.mp3`, `002.mp3`, `003.mp3`, etc.

---

**✅ Your Gesture-Controlled Music Player is now ready to use!**
