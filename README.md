# ESP32-OBD2-Scanner

## 📁 Project Structure
ESP32-OBD2-Scanner/
├── src/        Arduino source code
├── docs/       Schematics (PDF)
├── images/     Pictures and screenshots
└── README.md   Informations and instructions


A simple and standalone **ESP32-based OBD2 scanner** with a **WiFi web interface**.  
The ESP32 creates its own WiFi Access Point, allowing you to connect directly with your smartphone and view OBD2 data and clear trouble codes (DTCs) via a web browser.

✅ No mobile app required  
✅ No internet connection required  
✅ Works directly in the car  

---

## ✨ Features

- ESP32 runs as **WiFi Access Point**
- Read CAN with SN65HVD230
- Read Faults and other informations directly in web browser
- Web dashboard accessible from any smartphone or browser
- Clear Diagnostic Trouble Codes (OBD Mode 04)
- You can add your own Features later
---

## 🧰 Hardware Requirements

- ESP32 (tested with **ESP32-WROOM-32U**)   ~ 5$
- CAN Transceiver: **SN65HVD230**           ~ 3$
- OBD2 connector                            ~ 3$
- 12V → 5V  **DC-DC converter**             ~ 2$
- Android or iOS smartphone

### Wiring
| OBD2 connector Pin 16 12V+ | DC-DC converter IN+ |
| OBD2 connector Pin 4 + Bridge to Pin 5 GRN | DC-DC converter IN- |

| DC-DC converter OUT+ | ESP32 5V |
| DC-DC converter OUT- | ESP32 GND |

| CAN Transceiver TX | GPIO 21 |
| CAN Transceiver RX | GPIO 22 |
| CAN Transceiver 3.3V | ESP32 3.3V |
| CAN Transceiver GND | ESP32 GND |
| CAN Transceiver CANH | OBD2 connector Pin 6 |
| CAN Transceiver CANL | OBD2 connector Pin 14 |

⚠️ **Important:**  
Never connect 12V directly to the ESP32.

---

## 📡 WiFi Access Point

The ESP32 creates its own WiFi network:

- **SSID:** `ESP32_OBD` ** Change to your SSID
- **Password:** `12345678` ** Change to your Password
- **IP Address:** `192.168.4.1`

After connecting with your phone, open in Browser:
192.168.4.1

*** to be continued
