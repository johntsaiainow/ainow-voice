# AiNow Voice S3 — Standard

ESP32-S3 dual-microphone AI voice card — Standard Edition

---

## Overview

Standard Edition is the base model of the AiNow Voice S3 series, suitable for desktop assistants, voice assistant prototypes, and development boards.

## Hardware Specifications

| Item | Specification |
| :--- | :--- |
| **Main MCU** | ESP32-S3-WROOM-1-N16R8 (8 MB Octal PSRAM) |
| **Microphones** | 2× Digital I2S MEMS (INMP441 / MSM261S), socketed via 2.54mm pin headers, 54 mm center spacing |
| **Display** | ST7789 1.54" SPI TFT (240×240), socketed via 1×8 pin header |
| **Audio Output** | MAX98357A I2S Class-D amplifier, JST-PH-2P speaker connector |
| **Power** | USB Type-C (5V), TP4056 single-cell Li-ion charger, AP2112K 3.3V LDO |
| **Battery** | JST-PH-2P 3.7V Li-Po battery connector |
| **Buttons** | RST (ESP_EN) / BOOT (PTT wake) |
| **Status LED** | WS2812B RGB |
| **PCB Size** | 70 × 50 mm, rounded corners, four M3 mounting holes |
| **Layers** | 2 layers (F.Cu / B.Cu) + dual-layer GND pour |

## Folder Structure

```
s3-dualmic-standard/
├── README.md
├── kicad/
│   ├── xiaozhi_s3_dualmic.kicad_pro
│   ├── xiaozhi_s3_dualmic.kicad_sch
│   └── xiaozhi_s3_dualmic.kicad_pcb
├── gerber/           # Gerber output for board house (export and place here)
├── 3d/               # Additional STEP model references
└── docs/
    └── pinout.md     # ESP32-S3 GPIO mapping table
```

## Quick Start

1. Make sure **KiCad 10** is installed.
2. Open `kicad/xiaozhi_s3_dualmic.kicad_pro`.
3. Press `B` to fill copper zones, press `Alt + 3` to view the 3D model.
4. Use KiCad native **Push & Shove** (`X`) to complete routing following the ratsnest.
5. Export Gerber to `gerber/` and send to the manufacturer.

## GPIO Mapping (compatible with xiaozhi-esp32 firmware)

| Function | ESP32-S3 GPIO |
| :--- | :--- |
| I2S0 BCLK (Mic) | 41 |
| I2S0 WS (Mic) | 42 |
| I2S0 DIN (Mic Data) | 2 |
| I2S1 BCLK (Amp) | 15 |
| I2S1 LRCK (Amp) | 16 |
| I2S1 DOUT (Amp Data) | 7 |
| LCD SCL | 12 |
| LCD SDA | 11 |
| LCD RES | 14 |
| LCD DC | 13 |
| LCD CS | 10 |
| LCD BLK | 21 |
| RGB_DATA | 48 |
| BOOT / PTT | 0 |
| RST / ESP_EN | 3 |
| USB D- | 19 |
| USB D+ | 20 |
| VBAT_ADC | 1 |

---

**AI-Now Inc.** — 11/2026 — CC BY 4.0
