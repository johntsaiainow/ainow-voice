# AiNow Voice S3 — Standard

ESP32-S3 雙麥克風 AI 語音卡片（標準版）

---

## 概述

標準版是 AiNow Voice S3 系列的基礎型號，適合桌面擺件、語音助手原型與開發板使用。

## 硬體規格

| 項目 | 規格 |
| :--- | :--- |
| **主控 MCU** | ESP32-S3-WROOM-1-N16R8 (8 MB Octal PSRAM) |
| **麥克風** | 2× 數位 I2S MEMS (INMP441 / MSM261S)，透過 2.54mm 排母插座式安裝，中心間距 54 mm |
| **顯示螢幕** | ST7789 1.54" SPI TFT (240×240)，1×8 排母插座 |
| **音訊輸出** | MAX98357A I2S D 類功放，JST-PH-2P 揚聲器插座 |
| **電源** | USB Type-C (5V)，TP4056 單節鋰電池充電，AP2112K 3.3V LDO |
| **電池** | JST-PH-2P 3.7V 鋰聚合物電池插座 |
| **按鍵** | RST (ESP_EN) / BOOT (PTT 喚醒) |
| **狀態燈** | WS2812B RGB |
| **PCB 尺寸** | 70 × 50 mm，圓角，四角 M3 固定孔 |
| **層數** | 2 層 (F.Cu / B.Cu) + 雙層 GND 鋪銅 |

## 目錄結構

```
s3-dualmic-standard/
├── README.md
├── kicad/
│   ├── xiaozhi_s3_dualmic.kicad_pro
│   ├── xiaozhi_s3_dualmic.kicad_sch
│   └── xiaozhi_s3_dualmic.kicad_pcb
├── gerber/           # 送板廠用 Gerber (匯出後放入)
├── 3d/               # 額外 STEP 模型參考
└── docs/
    └── pinout.md     # ESP32-S3 GPIO 對照表
```

## 快速開始

1. 確認已安裝 **KiCad 10**。
2. 開啟 `kicad/xiaozhi_s3_dualmic.kicad_pro`。
3. 按下 `B` 重算鋪銅，按下 `Alt + 3` 檢視 3D 模型。
4. 使用 KiCad 原生 **Push & Shove** (`X`) 依據飛線網表完成佈線。
5. 匯出 Gerber 至 `gerber/` 後送製造。

## GPIO 對照 (xiaozhi-esp32 相容)

| 功能 | ESP32-S3 GPIO |
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
