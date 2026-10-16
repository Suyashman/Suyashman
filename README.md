<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Suyash%20Sunam&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=ML%20%2F%20Computer%20Vision%20Engineer&descAlignY=60&descSize=20" alt="Suyash Sunam" width="100%"/>

<a href="https://github.com/Suyashman">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=21&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=720&lines=Building+real-time+vision+systems+that+ship;YOLO+%C2%B7+SAM3+%C2%B7+PyTorch+%C2%B7+FastAPI+%C2%B7+React;Two+IEEE+publications+%C2%B7+B.Tech+AI+%26+DS+%C2%B72027;Open+to+ML+%2F+Computer+Vision+roles" alt="Typing SVG" />
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-suyashsunam.me-0A66C2?style=for-the-badge&logo=vercel&logoColor=white)](https://suyashsunam.me/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-suyashsunam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/suyashsunam/)
[![Email](https://img.shields.io/badge/Email-2suyash@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:2suyash@gmail.com)
[![IEEE](https://img.shields.io/badge/IEEE_Xplore-2_papers-00629B?style=for-the-badge&logo=ieee&logoColor=white)](#-publications)

</div>

---

## 👋 About

I build **computer-vision systems that run on real cameras, real GPUs and real factory floors**, not just notebooks.
I'm a final-year B.Tech student (AI & Data Science) at **MIT World Peace University, Pune**, and I currently work at
**[Sparkline](https://sparkline.co.in)** on an industrial safety product that detects PPE and recognises workers in live video.

What I care about: the whole loop, from **labelling data → training → measuring honestly → packaging something a non-technical
user can install**. I report real metrics (and the limitations) instead of only the flattering ones.

- 🔭 **Now:** Industrial Safety Vision at Sparkline: PPE detection, face recognition, dashboards and Windows/Linux installers
- 🧪 **Side projects:** SAM3-assisted labelling, dataset tooling, a neural game engine, super-resolution
- 🎓 **Studying:** B.Tech CSE (AI & DS), MIT-WPU · 2023 to 2027 · CGPA **8.56**
- 📍 **Based in:** Pune, India
- 📫 **Open to:** ML / Computer Vision engineering roles (graduating 2027)

---

## 🏢 Currently building: Industrial Safety Vision · [Sparkline](https://sparkline.co.in)

An on-premise safety-compliance product: cameras watch a work area, the system detects **missing PPE** (helmet, vest, goggles…),
**identifies the worker by face**, and raises alerts and reports on a web dashboard. It runs fully on the customer's own GPU
machine, with no cloud dependency.

| | |
|---|---|
| **Vision** | Ultralytics YOLO for PPE · InsightFace + ONNX Runtime for face recognition · multi-camera pipelines on NVIDIA GPUs |
| **Product** | FastAPI backend · React dashboard · per-client model editions |
| **Delivery** | One codebase shipped as a **Windows `.exe` installer** and a **Linux `.deb`** with automated build, smoke tests and CI on both OSes |
| **Data** | Dataset labelling and retraining workflow (see *SAM3 Auto-Annotator* and *Dataset Manager* below) |

> The product code is private. The open-source companions below are the tools I built around it.

---

## 🚀 Featured projects

| Project | What it is | Stack |
|---|---|---|
| **[SAM3 Auto-Annotator](https://github.com/Suyashman/SAM3-Autolabeler)** | A labelling assistant built on Meta's SAM3 that turns image folders into YOLO-seg datasets. Per-class confidence gates calibrated against existing labels, a keyboard-driven review queue that surfaces the most uncertain items first, resumable runs. **Measured F1 on PPE: person 0.90 · vest 0.87 · helmet 0.85 · goggles 0.65.** Its README says plainly where it fails (amorphous classes like smoke). | `Python` `PyTorch` `Transformers` `FastAPI` |
| **[YOLO Dataset Manager](https://github.com/Suyashman/dataset-manager)** | Local-first app for the full detection lifecycle: merge Roboflow exports, annotate in the browser, augment, **train with live loss/mAP charts**, and test on images, video or webcam. Includes dataset validation (duplicates, missing labels, class balance). | `FastAPI` `Ultralytics` `React` `Vite` `Tailwind` |
| **[Worker Monitor](https://github.com/Suyashman/worker-monitor)** | Live webcam view that recognises enrolled workers by face and checks PPE at the same time. Guided multi-angle enrolment, local SQLite storage, GPU with CPU fallback. | `InsightFace` `YOLO` `FastAPI` `SQLAlchemy` `React` |
| **[FSRCNN / EDSR Super-Resolution](https://github.com/Suyashman/fsrcnn-dlss)** | DLSS-style upscaling built from scratch in PyTorch with a real-time webcam mode and an ablation runner. **FSRCNN: ~37.0 dB PSNR vs 33.66 dB bicubic with only 24K parameters, ~60 FPS on an RTX 4070.** | `PyTorch` `CUDA` `AMP` `OpenCV` |
| **[SnakeNGen](https://github.com/Suyashman/SnakeNGen)** | A small take on Google's *GameNGen*: a ~2M-parameter U-Net **replaces the game engine of Snake** and predicts every next frame from past frames and the player's action. Evaluated against a persistence baseline, trained on an 8 GB laptop GPU. | `PyTorch` `U-Net` `Python` |
| **[ADAS on RC cars](https://github.com/Suyashman/advance-driver-assistance-system)** | Scaled physical ADAS testbed: overhead-camera tracking, lane-departure, collision warning, **automatic emergency braking**, lane keeping, and a V2V "hive mind" over MQTT that shares hazards between cars. | `OpenCV` `Arduino R4` `ESP32` `MQTT` |
| **[Smart Tomato Segregator](https://github.com/Suyashman/tomato-segregator)** | Camera → YOLOv8 → Wi-Fi command → servo arm that physically sorts produce by type, ripeness, colour or size, with five modes selectable from the device. | `YOLOv8` `OpenCV` `Arduino UNO R4 WiFi` |

<details>
<summary><b>More projects</b></summary>

<br/>

| Project | What it is | Stack |
|---|---|---|
| **[Trading Simulator](https://github.com/Suyashman/multi-client-trading-simulator)** | Multi-client exchange simulator: matching engine with partial fills, live order book, admin desk. Changes are pushed to every open tab by **Postgres triggers + LISTEN/NOTIFY**, with concurrency-safe matching via `FOR UPDATE SKIP LOCKED`. | `PostgreSQL` `FastAPI` `asyncpg` `WebSockets` |
| **[Video Steganography](https://github.com/Suyashman/video-steganography-java)** | Hides and recovers messages in video with LSB substitution; frames chosen by a seeded key. | `Java` `OpenCV` |
| **[Image Steganography](https://github.com/Suyashman/image-steganography)** · [live demo](https://image-steganography-two.vercel.app) | Web version of the same idea, deployed on Vercel. | `Python` `Vercel` |
| **[Crop Disease Prediction](https://github.com/arya20072004/crop-disease-detection)** (team) | Mobile app that predicts crop disease with a CNN and forecasts risk with an LSTM. | `Python` `Flutter` `CNN` `LSTM` |
| **[DLSS Performance Comparison](https://github.com/Suyashman/nvidia-dlss-performance-comparison-)** | Benchmarks DLSS across RTX 3050 / 4050 / 4070 / 5060 laptop GPUs and an RTX 3080 Ti desktop GPU. | `Benchmarking` `NVIDIA` |
| **[Hand-Gesture Drawing](https://github.com/Suyashman/hand-gesture-drawing)** | Draw in the air with your webcam using MediaPipe hand tracking. | `Python` `MediaPipe` |
| **[Portfolio](https://suyashsunam.me/)** | My site, built with React, Vite, Tailwind and Framer Motion. | `React` `Tailwind` |

</details>

---

## 📄 Publications

- 📘 **[Paper 1 title]**: *[venue / conference, year]* · [IEEE Xplore ↗](https://ieeexplore.ieee.org/document/11702370)
- 📘 **[Paper 2 title]**: *[venue / conference, year]* · [IEEE Xplore ↗](https://ieeexplore.ieee.org/document/11323656)

---

## 🛠️ Tech stack

<div align="center">

**Languages**<br/>
<img src="https://skillicons.dev/icons?i=py,cpp,c,java,js,ts,r,bash&perline=8" alt="Languages"/>

**ML / Computer Vision**<br/>
<img src="https://skillicons.dev/icons?i=pytorch,tensorflow,opencv,sklearn,numpy,pandas&perline=8" alt="ML and CV"/>

**Backend & Web**<br/>
<img src="https://skillicons.dev/icons?i=fastapi,nodejs,express,react,vite,tailwind,html,css&perline=8" alt="Backend and web"/>

**Data & Infra**<br/>
<img src="https://skillicons.dev/icons?i=postgres,mysql,sqlite,docker,githubactions,linux,windows,aws&perline=8" alt="Data and infra"/>

**Tools & Hardware**<br/>
<img src="https://skillicons.dev/icons?i=git,github,vscode,arduino,flutter,vercel&perline=8" alt="Tools"/>

</div>

<sub>Also: Ultralytics YOLO · SAM3 · InsightFace · ONNX Runtime · MediaPipe · MQTT · PyInstaller · Inno Setup · CUDA · Roboflow</sub>

---

## 📊 GitHub stats

<div align="center">

<img height="170" src="https://github-readme-stats.shion.dev/api?username=Suyashman&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false" alt="GitHub stats"/>
<img height="170" src="https://github-readme-stats.shion.dev/api/top-langs/?username=Suyashman&theme=tokyonight&hide_border=true&layout=compact&langs_count=6" alt="Top languages"/>

</div>

---

<div align="center">

*"Measure it, then say what the number actually means."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=100&section=footer" alt="" width="100%"/>

</div>
