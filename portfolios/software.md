# Software portfolio

[Back to profile](https://github.com/elitetq) · Other portfolios: [Hardware design](hardware-design.md), [Firmware](firmware.md), [PCB design](pcb-design.md)

> **Legend:** 🎥 Video demo · 🖨️ Custom PCB (KiCad) · 📖 Build and usage guide · 🚧 Work in progress · 👥 Team project

Systems, back-end and tooling work, from a dependency-free compressor in C to a Kotlin server.

## jzip 📖

A file compressor in pure C with no dependencies. It uses static order-0 arithmetic coding with 32-bit bounds and a 15-bit probability model, and writes a self-describing `.jzip` container that restores the original bytes and file extension exactly. Round trips are checked with SHA-256, cutting .txt files by about 46% and .psd files by 24%, and it builds on Linux and Windows. [View the repo](https://github.com/elitetq/jzip).

## J-Graphics-Library 🎥 📖

A graphics library I designed and built from scratch for the Embedded in Embedded club (2025-26). About 1,600 lines of C for the Zephyr RTOS.

- A layered component system with buttons, shapes, text, images, decals, progress bars and full-screen fills, plus runtime layer reordering
- A Python pipeline that converts PNG and JPG images into 1-bit or RGB666 pixel arrays for the driver
- Reused across 3 later projects, replacing per-project display code with a shared graphics layer
- Ships with SojournOS, a themed demo OS built on Zephyr state machines, with a playable snake game, theme switching, a lock screen and an about page

[View the repo and demo video](https://github.com/elitetq/J-Graphics-Library).

## Back-end software at UCalgary Racing

I work on the team's Kotlin server (Ktor REST API, gRPC node protocol and MongoDB), which queues STAR-CCM+ simulation jobs for remote nodes. The repos are private, so here is what I did:

- Replaced a hard-coded login table with SQLite-backed, hashed authentication
- Designed an `AuthService` interface (SQLite plus a legacy adapter) and injected it with Koin into login and 8 REST routes
- Made the job orchestrator concurrency-safe with a coroutine Mutex and ConcurrentHashMaps for job and log state
- Fixed a MongoDB connection race (use before connect) with a double-checked, Mutex-guarded connect
- Built a menu-driven admin CLI, run as a Gradle task, to add, list, search, edit and remove users

## PathGuard 👥

A pedestrian safety prototype built with Team Sudo Bash Bros at Hack the Change 2025. An ESP32-CAM and YOLOv8 count pedestrians, an Arduino kiosk lets people report hazards like ice, and an AWS backend stores the events. I built the React and Mapbox dashboard that maps congestion and hazards and wired it to the AWS data, while teammates built the camera, AI and kiosk code. [View the repo](https://github.com/elitetq/PathGuard).
