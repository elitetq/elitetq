# 💻 Jonart Bajraktari 🖥️

> **Legend:** 🎥 Video demo · 🖨️ Custom PCB (KiCad) · 📖 Build and usage guide · 🚧 Work in progress · 👥 Team project

Third-year electrical engineering student at the University of Calgary with a computer engineering minor. I like embedded software, hardware, PCBs, graphics libraries and anything low-level.

## Featured: J-Graphics-Library 🎥 📖

**I designed and built this graphics library from scratch for the Embedded in Embedded club (2025-26).**

[J-Graphics-Library](https://github.com/elitetq/J-Graphics-Library) is about 1,600 lines of C for the Zephyr RTOS. It drives a 240x320 ST7789 display over SPI, with capacitive touch, on a Nordic nRF52840 DK.

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

## More projects

### [GameOver_NRF](https://github.com/elitetq/GameOver_NRF) 📖
TOTS, a touchscreen maze game for the nRF52840 DK running on Zephyr. You swipe to move, collect points and avoid enemies, and all rendering goes through my J-Graphics-Library. The repo includes image conversion scripts and full build and flash instructions.

### [jzip](https://github.com/elitetq/jzip) 📖
A file compressor in pure C with no dependencies. It uses static order-0 arithmetic coding with 32-bit bounds and a 15-bit probability model, and writes a self-describing `.jzip` container that restores the original bytes and file extension exactly. Round trips are checked with SHA-256, cutting .txt files by about 46% and .psd files by 24%, and it builds on Linux and Windows.

### [hid-controller](https://github.com/elitetq/hid-controller) 🎥 🖨️ 📖
A custom USB gamepad on an STM32F103 with my own KiCad schematic, PCB, fabrication files and firmware. It has two analog sticks, a D-pad, face buttons, bumpers and digital triggers, and it enumerates on Linux as a custom HID device called J-Controller. Windows only partly enumerates it so far.

### [rotating-disk-uvm](https://github.com/elitetq/rotating-disk-uvm) 🚧 📖
A UVM testbench for a rotating disk position controller, run on Vivado XSim and written by hand to teach myself UVM. The PWM and clamp blocks are verified with constrained-random stimulus, golden-model scoreboards, SVA assertions, functional coverage and a Python regression script. The quadrature decoder and controller are still to do.

### [JAARK](https://github.com/elitetq/JAARK) 🖨️
A Bluetooth remote controlled car and its handheld controller on two STM32F446 boards. I did most of the RC car PCB in KiCad and wrote the C firmware for both sides, including an ST7789 display driver. The link uses DMA with checksums and a watchdog, and the car adds a metal detector and ultrasonic ranging.

### [PathGuard](https://github.com/elitetq/PathGuard) 👥
A pedestrian safety prototype built with Team Sudo Bash Bros at Hack the Change 2025. An ESP32-CAM and YOLOv8 count pedestrians, an Arduino kiosk lets people report hazards like ice, and an AWS backend stores the events. I built the React and Mapbox dashboard that maps congestion and hazards and wired it to the AWS data, while teammates built the camera, AI and kiosk code.

## PCB work at BMERIT

### Gait project
Worked on the upper and lower module PCBs. Implemented buck-boost converters, SD cards, ESP32s, pressure sensors, battery holders and polarity protection, among other circuitry.

### CyberStride
Designed the PCBs and cleaned up the PCB wiring. Fixed issues like floating grounds and messy routing, and standardized SMD component sizes.

### Dementia remote
Helped fix the remote's dimensions and component placement to fit the mechanical design.

## Back-end software at UCalgary Racing

I work on the team's Kotlin server (Ktor REST API, gRPC node protocol and MongoDB), which queues STAR-CCM+ simulation jobs for remote nodes. The repos are private, so here is what I did:

- Replaced a hard-coded login table with SQLite-backed, hashed authentication
- Designed an `AuthService` interface (SQLite plus a legacy adapter) and injected it with Koin into login and 8 REST routes
- Made the job orchestrator concurrency-safe with a coroutine Mutex and ConcurrentHashMaps for job and log state
- Fixed a MongoDB connection race (use before connect) with a double-checked, Mutex-guarded connect
- Built a menu-driven admin CLI, run as a Gradle task, to add, list, search, edit and remove users

## Outside of engineering

I play games, bike and hike with friends, go camping, read, and make motion graphics in After Effects. 🚴🥾🏕️📚🎬
