# 💻 Jonart Bajraktari 🖥️

> **Legend:** 🎥 Video demo · 🖨️ Custom PCB (KiCad) · 📖 Build and usage guide · 🚧 Work in progress · 👥 Team project

Third-year electrical engineering student at the University of Calgary with a computer engineering minor. I like embedded software, hardware, PCBs, graphics libraries and anything low-level.

## Portfolios

Pick the portfolio that matches the role. Some projects appear in more than one.

| Portfolio | Projects |
| --- | --- |
| [Hardware design](portfolios/hardware-design.md) | Gait power supply, hid-controller, JAARK, rotating-disk-uvm |
| [Firmware](portfolios/firmware.md) | J-Graphics-Library, GameOver_NRF, hid-controller, JAARK |
| [Software](portfolios/software.md) | jzip, J-Graphics-Library, PathGuard, UCalgary Racing back end |
| [PCB design](portfolios/pcb-design.md) | Gait boards, hid-controller, JAARK, CyberStride, Dementia remote |

## Featured: J-Graphics-Library 🎥 📖

**I designed and built this graphics library from scratch for the Embedded in Embedded club (2025-26).**

[J-Graphics-Library](https://github.com/elitetq/J-Graphics-Library) is about 1,600 lines of C for the Zephyr RTOS. It drives a 240x320 ILI9341 display over SPI, with capacitive touch, on a Nordic nRF52840 DK.

- A layered component system with buttons, shapes, text, images, decals, progress bars and full-screen fills, plus runtime layer reordering
- A double-buffered RAM scheme that cut image load time by almost 50%
- Animations for shape resizing and image fade-in and fade-out
- Asynchronous SPI transfers through Zephyr's callback API, and capacitive touch polling over I2C
- A Python pipeline that converts PNG and JPG images into 1-bit or RGB666 pixel arrays for the driver
- Reused across 3 later projects, replacing per-project display code with a shared graphics layer
- Ships with SojournOS, a themed demo OS built on Zephyr state machines, with a playable snake game, theme switching, a lock screen and an about page

## What I'm involved in

- Electrical lead on **BMERIT**, a club focused on biomedical design, leading a 10-person electrical team
- Software member on the **UCalgary Racing** formula car team, working on the back end
- Founder of **Schulich Press Start**, a club designing a Game Boy-style handheld from the ground up, with a custom OS and game library. I'm building the PCB devkit from scratch in KiCad, working from reference designs

## Outside of engineering

I play games, bike and hike with friends, go camping, read, and make motion graphics in After Effects. 🚴🥾🏕️📚🎬
