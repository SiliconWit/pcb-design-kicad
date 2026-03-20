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
├── schematics/
│   └── (schematic PDFs go here)
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/pcb-design-kicad.git
cd pcb-design-kicad
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**Adding schematic PDFs:**

Place your PDF files in the `schematics/` folder, then:

```bash
git add schematics/
git commit -m "Add schematic for lesson name"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/pcb-design-kicad](https://github.com/SiliconWit/pcb-design-kicad)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/pcb-design-kicad.git
   cd pcb-design-kicad
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
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
- Schematic PDFs go in the `schematics/` folder

## Local Development

To preview the full site locally, clone the main site repository and initialize submodules:

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
