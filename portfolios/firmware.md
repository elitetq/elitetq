# Firmware portfolio

[Back to profile](https://github.com/elitetq) · Other portfolios: [Hardware design](hardware-design.md), [Software](software.md), [PCB design](pcb-design.md)

> **Legend:** 🎥 Video demo · 🖨️ Custom PCB (KiCad) · 📖 Build and usage guide · 🚧 Work in progress · 👥 Team project

Embedded C on Nordic and STM32 parts, from drivers and RTOS applications to USB devices and wireless links.

## J-Graphics-Library 🎥 📖

**Designed and built from scratch for the Embedded in Embedded club (2025-26).** About 1,600 lines of C for the Zephyr RTOS. It drives a 240x320 ILI9341 display over SPI, with capacitive touch, on a Nordic nRF52840 DK.

- Asynchronous SPI transfers through Zephyr's callback API, and capacitive touch polling over I2C
- A double-buffered RAM scheme that cut image load time by almost 50%
- A layered component system with animations for shape resizing and image fade-in and fade-out
- Reused across 3 later projects, replacing per-project display code with a shared graphics layer
- Ships with SojournOS, a themed demo OS built on Zephyr state machines

[View the repo and demo video](https://github.com/elitetq/J-Graphics-Library).

## GameOver_NRF 📖

TOTS, a touchscreen maze game for the nRF52840 DK running on Zephyr. You swipe to move, collect points and avoid enemies, and all rendering goes through my J-Graphics-Library. The repo includes image conversion scripts and full build and flash instructions. [View the repo](https://github.com/elitetq/GameOver_NRF).

## hid-controller 🎥 🖨️ 📖

Firmware for a custom USB gamepad on an STM32F103. It samples the analog sticks and buttons and sends custom HID gamepad reports. The controller enumerates on Linux as a custom HID device called J-Controller. Windows only partly enumerates it so far. [View the repo](https://github.com/elitetq/hid-controller).

## JAARK 🖨️

C firmware for both sides of a Bluetooth remote controlled car, on two STM32F446 boards. The link uses DMA with checksums and a watchdog, and the project includes an ILI9341 display driver. The car adds a metal detector and ultrasonic ranging. [View the repo](https://github.com/elitetq/JAARK).
