---
title: "PCB Design with KiCad - Collaboration Guide"
description: "Contributing guide for PCB Design with KiCad course content"
tableOfContents: true
sidebar:
  order: 999
---

# PCB Design with KiCad

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/pcb-design-kicad/](https://siliconwit.com/education/pcb-design-kicad/)

A hands-on course covering PCB design and manufacturing using KiCad 9. Nine lessons produce nine complete boards, from a through-hole ATmega328P breakout to multi-layer STM32 and ESP32 boards with USB-C, WiFi, battery management, motor control, and code-based PCB generation via KiCad Python scripting.

## Lessons

| # | Title |
|---|-------|
| 1 | ATmega328P Breakout Board (Through-Hole) |
| 2 | ATmega328P Sensor Shield (SMD Components) |
| 3 | STM32 USB Development Board |
| 4 | STM32 USB-C Four-Layer Board |
| 5 | ESP32 WiFi/Bluetooth DevKit |
| 6 | ESP32 Battery IoT Sensor Node |
| 7 | RP2040 USB-C Development Board |
| 8 | Motor Driver and Sensor Integration Board |
| 9 | Code-Based PCB Design (KiCad Scripting) |

## File Structure

```
pcb-design-kicad/
├── index.mdx
├── atmega328p-breakout-board-through-hole.mdx
├── atmega328p-sensor-shield-smd-components.mdx
├── stm32-usb-development-board.mdx
├── stm32-usb-c-four-layer-pcb.mdx
├── esp32-wifi-bluetooth-devkit.mdx
├── esp32-battery-iot-sensor-node.mdx
├── rp2040-usb-c-development-board.mdx
├── motor-driver-sensor-integration-board.mdx
├── code-based-pcb-design-kicad-scripting.mdx
└── README.md
```

## How to Contribute

1. Fork the repository: [SiliconWit/pcb-design-kicad](https://github.com/SiliconWit/pcb-design-kicad)
2. Create a feature branch: `git checkout -b feature/your-topic`
3. Make your changes and commit with a clear message
4. Push to your fork and open a Pull Request against `main`
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Do not use `<BionicText>` in this course
- Code blocks should include a title attribute:
  ````mdx
  ```python title="generate_board.py"
  import pcbnew
  board = pcbnew.GetBoard()
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Keep paragraphs concise and focused on practical application
- Include KiCad Python scripting examples where relevant
- All schematics and layouts must target KiCad 9

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).
