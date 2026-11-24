# AI-Now Inc. — Hardware Designs

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

Open-source PCB hardware repository for **AiNow Voice S3** — a family of ESP32-S3 based dual-microphone AI voice assistant cards.

> **Note:** This hardware is no longer tied to the "XiaoZhi" (小智) firmware. It is a general-purpose ESP32-S3 voice platform compatible with any ESP-SR / ESP-ADF / custom voice pipeline.

---

## 📂 Product Variations

| Variation | MCU | Mic | Display | Amp | Status | Folder |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **AiNow Voice S3 — Standard** | ESP32-S3-WROOM-1-N16R8 | 2× I2S MEMS (INMP441/MSM261S socketed) | ST7789 1.54" TFT | MAX98357A | Released | [`variations/s3-dualmic-standard`](./variations/s3-dualmic-standard) |
| AiNow Voice S3 — Mini | ESP32-S3-WROOM-1-N8R8 | 2× I2S MEMS | None (LED status only) | MAX98357A | Planned | [`variations/s3-dualmic-mini`](./variations/s3-dualmic-mini) |
| AiNow Voice S3 — Pro | ESP32-S3-WROOM-1-N16R8 | ES7210 4-ch ADC + Analog MEMS | ST7789 + OLED | NS4168 + passive filter | In design | [`variations/s3-dualmic-pro`](./variations/s3-dualmic-pro) |

> 各子目錄內含獨立 `README.md`、KiCad 原理圖/PCB 檔、Gerber 與 3D 模型說明。

---

## 🚀 Quick Start

1. 選擇想要建構的變體，進入對應子目錄閱讀其 `README.md`。
2. 使用 **KiCad 10** 開啟 `.kicad_pro` 檔案即可檢視原理圖與 PCB 3D 模型。
3. 依子目錄說明匯出 Gerber 後即可送板廠打樣。

---

## 📄 License

All hardware design files in this repository are released under **CC BY 4.0** unless otherwise noted in a sub-folder.

---

**AI-Now Inc.** — 11/2026
