# Waveshare 13.3" e-Paper HAT+ (E) Demo (Modified)

This repository contains demo code originally provided by Waveshare for the **13.3" e-Paper HAT+ (E)** module. It has been adapted for experimentation, file conversion, and selective integration with other hardware platforms — especially the ESP32 Universal e-Paper Driver Board.

🎯 **Goal**: Extract and adapt essential files (e.g., LUTs, image processing logic) for cross-compatibility with Waveshare's ESP32 board-based setup using the same Spectra 6 display.

## ⚙️ Features

- Original display code for Raspberry Pi (Python-based)
- Floyd-Steinberg image conversion with palette tables (`.act` files)
- Direct framebuffer access for testing
- File structure reference for display controller variants (13.3" Spectra 6)
- Source for LUTs and waveform generation logic

## 🧰 Requirements

- Raspberry Pi (any model with GPIO)
- 13.3" Spectra 6 e-Paper HAT+ (E) display
- Python 3.x
- Libraries: `spidev`, `RPi.GPIO`, `PIL` (Pillow), `numpy`

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/jakubkarafa/E-Paper_13.3inch_HAT_E.git
   cd E-Paper_13.3inch_HAT_E
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the demo:
   ```bash
   sudo python3 epd_demo.py
   ```

> Note: You must run with `sudo` due to GPIO access.

## 📄 Image Preparation (Optional)

- Use the included `.act` color tables for dithering (e.g., 3-color or 7-color Spectra).
- You can convert your own images using Affinity Photo, GIMP, or Photoshop.
- Place processed `.bmp` files into the `/pic` directory and reference them in the script.

## 📌 Credits

- Original source: [Waveshare Wiki](https://www.waveshare.com/wiki/13.3inch_e-Paper_HAT%2B_(E)_Manual)
- Adapted and maintained by: [Jakub Karafa](https://github.com/jakubkarafa)

## 📷 Screenshots / Photos

<!-- Add any photos of the HAT+ (E) display in action -->

---

This repo is used alongside [`E-Paper_ESP32_Driver_Board_Code`](https://github.com/jakubkarafa/E-Paper_ESP32_Driver_Board_Code.git) to enable broader Spectra 6 compatibility.

Pull requests welcome!