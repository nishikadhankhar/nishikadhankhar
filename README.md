<h1 align="center">Hi, I'm Nishika 👋</h1>

<p align="center">
  <b>Embedded systems&nbsp; ·&nbsp; Computer vision&nbsp; ·&nbsp; Full-stack</b><br>
  <sub>B.Tech student · Gurugram, India</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Sensors_%E2%86%92_Signals_%E2%86%92_Software-1A1B27?style=for-the-badge&labelColor=1A1B27" alt="Sensors to signals to software" />
</p>

---

I build systems that **sense the physical world and act on it** — an ESP32 that catches
onions rotting before anyone can smell them, a Raspberry Pi that impersonates a USB
keyboard, a vision pipeline that predicts where a crowd will jam up fifteen minutes
from now.

Most of my work sits at the seam between hardware and the web: firmware on one end,
a live dashboard on the other, and something interesting happening in between.

<br>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nishikadhankhar/nishikadhankhar/output/github-snake-tokyonight.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/nishikadhankhar/nishikadhankhar/output/github-snake.svg" />
    <img alt="A snake eating my GitHub contribution graph" src="https://raw.githubusercontent.com/nishikadhankhar/nishikadhankhar/output/github-snake.svg" />
  </picture>
</div>

<br>

## What I'm building

### 🧅 &nbsp;[Cold Storage Monitor](https://github.com/nishikadhankhar/cold-storage-monitor)

Catches onion decay in a 24 × 18 ft cold storage room *before it's visible*. Rotting onions
release ammonia and H₂S, which show up as a measurable **drop in gas resistance** on a BME688 —
so the alert fires on chemistry rather than guesswork. Four DS18B20 probes cover temperature,
and readings land in three places at once: a cloud dashboard, a dashboard the ESP32 serves
itself, and an on-device TFT with LEDs and a buzzer.

The nice bit: the `/ingest` response echoes current thresholds back to the ESP32, so a change
made in the browser reaches the hardware in about two seconds without any polling.

<sub>

`ESP32` `BME688` `DS18B20` `ST7735 TFT` `FastAPI` `WebSockets` `React` `TypeScript` `Supabase`

</sub>

### 🏟️ &nbsp;[Crowd Flow Optimiser](https://github.com/nishikadhankhar/GrandPrixGeekRoom)

A predictive digital twin for venue crowd management. YOLOv8 and MiDaS turn ordinary camera
feeds into a 3D occupancy grid, a Social Force Model simulates the crowd forward in time, and
the engine **forecasts bottlenecks 15 minutes out** and reroutes around them. A local SmolVLM2
(2.2B, GGUF) reads each scene and describes safety hazards in plain language. Density is
classified by Fruin Level-of-Service.

<sub>

`Python` `PyTorch` `YOLOv8` `MiDaS` `SmolVLM2` `llama.cpp` `FastAPI` `WebSockets` `Canvas API`

</sub>

### 📷 &nbsp;[Pi Barcode Scanner](https://github.com/nishikadhankhar/pi-barcode-scanner)

A Raspberry Pi 4 that **pretends to be a USB keyboard**. Camera Module 3 captures frames,
`pyzbar` decodes any barcode or QR in view, and the result is typed straight into whatever app
has focus on the host machine through `/dev/hidg0`. No driver, no client software, no pairing —
plug in the USB-C cable and it just types.

<sub>

`Raspberry Pi 4` `Picamera2` `pyzbar` `USB HID gadget` `systemd` `Python`

</sub>

<br>

**Also worth a look —**
[`pacer`](https://github.com/nishikadhankhar/pacer) (AI productivity companion with proactive
task prioritisation, built on Gemini) ·
[`gesture_draw`](https://github.com/nishikadhankhar/gesture_draw) (drawing on screen with
webcam-tracked hand gestures) ·
[`ecoroot`](https://github.com/nishikadhankhar/ecoroot) (an eco-friendly initiative platform) ·
[`learning-tracker`](https://github.com/nishikadhankhar/learning-tracker) (my daily learning log,
kept in the open)

<br>

## Toolbox

**Hardware & embedded**

<p>
  <img src="https://img.shields.io/badge/ESP32-1A1B27?style=for-the-badge&logo=espressif&logoColor=BF91F3" alt="ESP32" />
  <img src="https://img.shields.io/badge/Raspberry_Pi-1A1B27?style=for-the-badge&logo=raspberrypi&logoColor=BF91F3" alt="Raspberry Pi" />
  <img src="https://img.shields.io/badge/Arduino-1A1B27?style=for-the-badge&logo=arduino&logoColor=BF91F3" alt="Arduino" />
  <img src="https://img.shields.io/badge/C++-1A1B27?style=for-the-badge&logo=cplusplus&logoColor=BF91F3" alt="C++" />
  <img src="https://img.shields.io/badge/Linux-1A1B27?style=for-the-badge&logo=linux&logoColor=BF91F3" alt="Linux" />
</p>

**AI & computer vision**

<p>
  <img src="https://img.shields.io/badge/Python-1A1B27?style=for-the-badge&logo=python&logoColor=70A5FD" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-1A1B27?style=for-the-badge&logo=pytorch&logoColor=70A5FD" alt="PyTorch" />
  <img src="https://img.shields.io/badge/OpenCV-1A1B27?style=for-the-badge&logo=opencv&logoColor=70A5FD" alt="OpenCV" />
  <img src="https://img.shields.io/badge/YOLOv8-1A1B27?style=for-the-badge&logoColor=70A5FD" alt="YOLOv8" />
  <img src="https://img.shields.io/badge/NumPy-1A1B27?style=for-the-badge&logo=numpy&logoColor=70A5FD" alt="NumPy" />
</p>

**Backend & data**

<p>
  <img src="https://img.shields.io/badge/FastAPI-1A1B27?style=for-the-badge&logo=fastapi&logoColor=38BDAE" alt="FastAPI" />
  <img src="https://img.shields.io/badge/WebSockets-1A1B27?style=for-the-badge&logo=socketdotio&logoColor=38BDAE" alt="WebSockets" />
  <img src="https://img.shields.io/badge/Supabase-1A1B27?style=for-the-badge&logo=supabase&logoColor=38BDAE" alt="Supabase" />
  <img src="https://img.shields.io/badge/PostgreSQL-1A1B27?style=for-the-badge&logo=postgresql&logoColor=38BDAE" alt="PostgreSQL" />
</p>

**Frontend & deploy**

<p>
  <img src="https://img.shields.io/badge/React-1A1B27?style=for-the-badge&logo=react&logoColor=70A5FD" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-1A1B27?style=for-the-badge&logo=typescript&logoColor=70A5FD" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-1A1B27?style=for-the-badge&logo=vite&logoColor=70A5FD" alt="Vite" />
  <img src="https://img.shields.io/badge/GitHub_Actions-1A1B27?style=for-the-badge&logo=githubactions&logoColor=70A5FD" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Vercel-1A1B27?style=for-the-badge&logo=vercel&logoColor=70A5FD" alt="Vercel" />
</p>

<br>

## Currently

- 🔭 Extending the cold storage system — persisting history to Postgres, and a custom KiCad carrier board to get it off the breadboard
- 🌱 Working through DSA, Python and ML fundamentals daily, logged in the open at [`learning-tracker`](https://github.com/nishikadhankhar/learning-tracker)
- 🎯 Building toward **GSoC 2027** — looking for an org where embedded, vision, or sensor data is the point
- 💬 Happy to talk about ESP32 gotchas, USB HID gadgets, or getting YOLO to run fast on modest hardware

<br>

## Say hi

<p>
  <a href="mailto:nishidhnkhr@gmail.com">
    <img src="https://img.shields.io/badge/Email-1A1B27?style=for-the-badge&logo=gmail&logoColor=70A5FD" alt="Email" />
  </a>
  <!-- TODO: replace YOUR-HANDLE with your real LinkedIn handle, or delete this whole <a> block.
       The logo is inlined as a data URI because shields.io no longer ships a "linkedin" icon slug. -->
  <a href="https://www.linkedin.com/in/YOUR-HANDLE">
    <img src="https://img.shields.io/badge/LinkedIn-1A1B27?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0iIzcwYTVmZCI+PHBhdGggZD0iTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOSAxLjYzNy0xLjg1IDMuMzctMS44NSAzLjYwMSAwIDQuMjY3IDIuMzcgNC4yNjcgNS40NTV2Ni4yODZ6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjQuOTI1IDIuMDY0IDIuMDYzIDAgMS4xMzktLjkyNSAyLjA2NS0yLjA2NCAyLjA2NXptMS43ODIgMTMuMDE5SDMuNTU1VjloMy41NjR2MTEuNDUyek0yMi4yMjUgMEgxLjc3MUMuNzkyIDAgMCAuNzc0IDAgMS43Mjl2MjAuNTQyQzAgMjMuMjI3Ljc5MiAyNCAxLjc3MSAyNGgyMC40NTFDMjMuMiAyNCAyNCAyMy4yMjcgMjQgMjIuMjcxVjEuNzI5QzI0IC43NzQgMjMuMiAwIDIyLjIyNSAweiIvPjwvc3ZnPgo=" alt="LinkedIn" />
  </a>
</p>

<sub align="center">Sensors → signals → software.</sub>
