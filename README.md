# Hi, I'm Jonart 👋

Third-year electrical engineering student at the University of Calgary with a computer engineering minor. I like embedded software, hardware, PCBs, graphics libraries and anything low-level.

## Featured: J-Graphics-Library

**I designed and built this graphics library from scratch for the Embedded in Embedded club (2025-26).**

[J-Graphics-Library](https://github.com/elitetq/J-Graphics-Library) is about 1,600 lines of C for the Zephyr RTOS. It drives a 240x320 SPI touchscreen (the Adafruit 2.8" capacitive touch panel) on a Nordic nRF52840 DK.

- A layered component system with buttons, shapes, text, images, decals, progress bars and full-screen fills, plus runtime layer reordering
- Animations for shape resizing and image fade-in and fade-out
- Asynchronous SPI transfers through Zephyr's callback API, and capacitive touch polling over I2C
- Python tools that convert images into the library's formats
- Ships with SojournOS, a demo OS with a playable snake game, theme switching, a lock screen and an about page

## What I'm involved in

- Electrical lead on **BMERIT**, a club focused on biomedical design
- Software member on the **UCalgary Racing** formula car team
- Starting **Schulich Press Start**, a club building gaming handhelds from the ground up

## More projects

### [GameOver_NRF](https://github.com/elitetq/GameOver_NRF)
TOTS, a touchscreen maze game for the nRF52840 DK. Swipe to move, collect points and avoid enemies. Runs on Zephyr and uses J-Graphics-Library for all rendering.

### [jzip](https://github.com/elitetq/jzip)
A file compressor in pure C with no dependencies. It uses static order-0 arithmetic coding and writes a self-describing `.jzip` container that restores the original bytes and file extension exactly. Builds on Linux and Windows.

### [hid-controller](https://github.com/elitetq/hid-controller)
A custom USB gamepad built on an STM32F103. Includes the KiCad schematic and PCB, the fabrication files, and the firmware. Two analog sticks, a D-pad, face buttons, bumpers and triggers. It enumerates as a HID gamepad on Linux, and Windows support is still in progress.

### [rotating-disk-uvm](https://github.com/elitetq/rotating-disk-uvm)
A UVM testbench for a rotating disk position controller, run on Vivado XSim. It uses constrained-random stimulus, scoreboards against golden models, SVA assertions and functional coverage. A learning project, with the PWM and clamp blocks done so far and the quadrature decoder and controller still to do.

### [JAARK](https://github.com/elitetq/JAARK)
STM32F446 firmware with a custom ST7789 display driver, alongside a KiCad PCB design for a motor board.

### [PathGuard](https://github.com/elitetq/PathGuard)
A pedestrian safety prototype built with my team at Hack the Change 2025. An ESP32-CAM feeds a YOLOv8 people counter, an Arduino UNO R4 WiFi kiosk lets pedestrians report hazards like ice, an AWS backend stores the events, and a React dashboard maps it all.

## Club work

### [Schulich-Press-Start/console](https://github.com/Schulich-Press-Start/console)
The embedded software home for the Schulich Press Start Gen 1 handheld. A Zephyr workspace with the console firmware, board definitions, drivers and tests, built around a fork of the 32blit SDK.

### [Schulich-Press-Start/website](https://github.com/Schulich-Press-Start/website)
The Astro-based website for Schulich Press Start, with several console concept designs for feedback.

### [BMERIT-UCalgary/bmerit-cyberstride-website](https://github.com/BMERIT-UCalgary/bmerit-cyberstride-website)
Website repository for BMERIT's CyberStride. Early stage so far.

## Outside of engineering

I play games, bike and hike with friends, go camping, read, and make motion graphics in After Effects. 👋
