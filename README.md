# AI-Now Inc. — Hardware Designs

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

Open-source PCB hardware repository for **AiNow Voice S3** — a family of ESP32-S3 based dual-microphone AI voice assistant cards.

> **Note:** This hardware is no longer tied to the "XiaoZhi" firmware. It is a general-purpose ESP32-S3 voice platform compatible with any ESP-SR / ESP-ADF / custom voice pipeline.

---

## 📂 Product Variations (directly under root)

| Variation | MCU | Mic | Display | Amp | Status | Folder |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **AiNow Voice S3 — Standard** | ESP32-S3-WROOM-1-N16R8 | 2× I2S MEMS (INMP441/MSM261S socketed) | ST7789 1.54" TFT | MAX98357A | Released | [`s3-dualmic-standard`](./s3-dualmic-standard) |
| AiNow Voice S3 — Mini | ESP32-S3-WROOM-1-N8R8 | 2× I2S MEMS | None (LED status only) | MAX98357A | Planned | [`s3-dualmic-mini`](./s3-dualmic-mini) |
| AiNow Voice S3 — Pro | ESP32-S3-WROOM-1-N16R8 | ES7210 4-ch ADC + Analog MEMS | ST7789 + OLED | NS4168 + passive filter | In design | [`s3-dualmic-pro`](./s3-dualmic-pro) |

> Each sub-folder contains its own `README.md`, KiCad schematic/PCB files, Gerber output, and 3D model notes.

---

## 🚀 Quick Start

1. Enter the variation folder you want to build (e.g. `s3-dualmic-standard/`) and read its `README.md`.
2. Open the `.kicad_pro` file with **KiCad 10** to view the schematic and PCB 3D model.
3. Export Gerber per the sub-folder instructions and send to the board house.

---

## 📄 License

All hardware design files in this repository are released under **CC BY 4.0** unless otherwise noted in a sub-folder.

---

**AI-Now Inc.** — 11/2026
