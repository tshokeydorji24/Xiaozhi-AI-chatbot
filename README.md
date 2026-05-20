# 🤖 XiaoZhi AI Chatbox — XiaoZhi + Custom Face UI

An interactive AI chatbot with a custom animated face UI, running on a **Xiao ESP32-S3** microcontroller. It combines voice interaction, animated OLED expressions, and DeepSeek-powered AI responses into a compact embedded system.

> Animated face design inspired by the **Dasai Mochi** by Huykhong.

---

## ✨ Features

### 🎙️ Voice Interaction
- Real-time voice input via the **INMP441** digital microphone
- AI-powered conversational responses using **XiaoZhi + DeepSeek**
- Audio output through **MAX98357A** I2S amplifier and 8Ω 3W speaker

### 😄 Animated Face UI
- Expressive animated facial expressions on an **OLED** screen
- Custom UI design inspired by Dasai Mochi
- Visual status indicators: Listening, Thinking, Speaking, Idle (Standby)

### ⚙️ General
- Compact, low-power embedded design
- Wireless Bluetooth/Wi-Fi via the ESP32-S3 chip
- Open source and extensible codebase

---

## 🧱 System Architecture

```
        USER INTERACTION LAYER
   Voice Input (Mic) ←→ Voice Output (Speaker)
              │
       XIAO ESP32-S3
   ┌──────────────────────┐
   │ XiaoZhi Framework    │  ←→  DeepSeek AI (Cloud via Wi-Fi)
   │ OLED Face UI Engine  │  ←→  OLED Display (Expressions)
   └──────────────────────┘
```

---

## 🔧 Components

| # | Component |
|---|-----------|
| 1 | Xiao ESP32-S3 |
| 2 | INMP441 Microphone |
| 3 | MAX98357A I2S Amplifier |
| 4 | 4Ω 3W Square Cavity Speaker |
| 5 | OLED Display |

---

## 🔌 Wiring Summary

| Module | ESP32-S3 Pins |
|--------|--------------|
| INMP441 Mic | SCK → GPIO44(D7), WS → GPIO9(D10), SD → GPIO1(D0), VDD → 3.3V, GND → GND, LRC → GND |
| MAX98357A Amp | BCLK → GPIO7(D8), LRC → GPIO4(D3), DIN → GPIO2(D1), VIN → 5V, GND → GND, SD → 3.3V |
| OLED | SDA → GPIO5(D4), SCL → GPIO6(D5), VCC → 3.3V, GND → GND |

---

## 💻 Software Requirements

| Software | Version | Purpose |
|----------|---------|---------|
| Arduino IDE | 2.x recommended | Programming the ESP32-S3 |
| ESP-IDF | v5.x (via Arduino core) | ESP32-S3 hardware support |
| XiaoZhi ESP32 AI Framework | Open-source, MIT License | Core voice AI chatbot engine |
| DeepSeek API | Cloud-based, requires API key | AI language model backend |
| U8g2 / Adafruit SSD1306 | Arduino library | OLED display control |
| Cirkit Designer IDE | Web-based | Circuit diagram and simulation |

---

## 🚀 Getting Started

1. Clone this repository
   ```bash
   git clone https://github.com/your-username/xiaozhi-ai-chatbox.git
   ```
2. Open the project in **Arduino IDE 2.x**
3. Install the required libraries listed above
4. Add your **DeepSeek API key** in the configuration file
5. Wire up the components as shown in the wiring table
6. Flash the firmware to your **Xiao ESP32-S3**

---

## 📋 PCB Design

The PCB is designed to use **pin sockets** instead of soldering, making it safer and easier to swap components. Footprints are sourced from the lab's own library and supplemented with downloads from **SnapMagic** for components not available locally.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

The XiaoZhi framework is also MIT licensed. DeepSeek API usage is subject to [DeepSeek's Terms of Service](https://platform.deepseek.com).

---

## 🙏 Credits

- [XiaoZhi ESP32 AI Framework](https://xiaozhi.me) — core voice AI engine
- [DeepSeek](https://deepseek.com) — AI language model backend
- **Dasai Mochi by Huykhong** — animated face UI inspiration
