<h1 align="center">Suyash Sunam</h1>

<p align="center">
  Computer vision engineer · B.Tech in AI &amp; Data Science, MIT World Peace University · Pune, India
</p>

<p align="center">
  <a href="https://suyashsunam.me/">Portfolio</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/suyashsunam/">LinkedIn</a> &nbsp;·&nbsp;
  <a href="mailto:2suyash@gmail.com">2suyash@gmail.com</a> &nbsp;·&nbsp;
  <a href="#publications">Publications</a>
</p>

<br/>

I design and ship AI camera surveillance: systems that watch many live video streams at once, recognise whatever
a model has been trained to recognise, and turn what they see into alerts, records and reports a site can act on.
My work covers the whole chain, from dataset and training through GPU inference and a web dashboard to an installer a
client can run on their own machine.

I am in my final year (2023–2027, CGPA 8.56) and looking for machine learning and computer vision engineering roles.

<br/>

## What I am building now

**Industrial Safety Vision** at [Sparkline](https://sparkline.co.in) is a multi-camera AI surveillance platform for
industrial sites. It reads live RTSP streams, runs detection models on the site's own NVIDIA GPU, and records events with
a snapshot, a zone, a severity and a timeline. Client sites have no internet connection, so everything, including the
models, ships inside the installer and runs on-premise.

The part I am proudest of is the architecture. A detection capability is a **pipeline package**: model weights, a manifest,
an optional event handler and an optional dashboard panel, loaded against a versioned contract. A broken package is isolated and
never stops the others. Anything a model can be trained to see becomes a monitored, alertable pipeline without changing the platform.
Five are live today.

| Pipeline | What it does |
|---|---|
| **PPE compliance** | Required equipment is set per camera, on the whole frame or on drawn areas, each with its own zone and severity. People are placed by their foot point and a violation is filed only after it is confirmed over time. A second look re-checks distant, small people on an enlarged crop. |
| **Fire, smoke and sparks** | A custom-retrained detector served as a TensorRT engine, with class-level alerting. |
| **Vehicle dwell time** | Many fine-grained vehicle classes merged into fleet categories, tracked per vehicle to measure how long each one stays. |
| **Intrusion** | Confirmation and departure timers and size limits, so a real visit is told apart from a flicker. |
| **Face recognition** | Worker identification with enrolment, running from a face model packaged for offline sites. |

**Under the pipelines**

- **Inference runtime:** a detection loop shared across all cameras, with GPU-resident models, object tracking, per-pipeline size limits and confidence floors, a decode budget, camera health monitoring and outage recording.
- **Accuracy work:** I traced a stubborn false-alarm problem on small, distant people to helmets missing from the training labels themselves, which a validation set with the same gap could never reveal. The fix was a re-check on enlarged crops, measured on live site footage, plus a relabelling plan.
- **Licensing and model protection:** licences are signed per computer and per pipeline, model weights are encrypted at rest and unlock only with a valid licence, and expiry follows a defined grace and lock behaviour.
- **Delivery:** one codebase ships as a Windows installer and a Linux package, and also runs as a Docker deployment. I built the Installer Studio that produces client-specific installers (which pipelines and which labels each client gets). About 3,000 backend tests and CI on both operating systems guard it.

<sub>Stack: Python, FastAPI, SQLAlchemy and Alembic, React, TypeScript, Vite, Ultralytics YOLO, TensorRT, InsightFace, ONNX Runtime, PyInstaller, Inno Setup, Docker. The product code is private.</sub>

<br/>

## Selected projects

### [Smart Tomato Segregator](https://github.com/Suyashman/tomato-segregator)
**Award-winning hardware and vision project.**
A camera watches each item, a YOLOv8 model decides what it is, and a command goes over Wi-Fi to an Arduino that moves a servo arm to sort it.
Five sorting modes: tomato versus other vegetables, fresh versus rotten, red versus green, small versus large by bounding-box area, and manual. The mode is chosen on the device itself and shown on its OLED.
A solo project, from dataset and model to firmware and hardware.
<sub>YOLOv8 · OpenCV · Arduino UNO R4 WiFi · Roboflow</sub>

### [Super-resolution from scratch (FSRCNN and EDSR)](https://github.com/Suyashman/fsrcnn-dlss)
To understand how DLSS-style upscaling works, I built it from first principles in PyTorch, with mixed-precision training, an ablation runner, and a real-time webcam mode.
At 2× on Set5, FSRCNN reaches about **37.0 dB PSNR against 33.66 dB for bicubic** with only 24 thousand parameters, and runs at about **60 FPS on an RTX 4070**.
<sub>PyTorch · CUDA · AMP · OpenCV</sub>

### Video and image steganography
Hiding messages inside media without visible change. The video version ([Java and OpenCV](https://github.com/Suyashman/video-steganography-java)) embeds data by least-significant-bit substitution, with the carrier frames chosen by a seeded key so only the key holder can recover the message.
The image version ([Python](https://github.com/Suyashman/image-steganography)) is deployed as a [live web demo](https://image-steganography-two.vercel.app).
<sub>Java · OpenCV · Python · LSB encoding</sub>

<details>
<summary>More projects</summary>

<br/>

- **[SAM3 Auto-Annotator](https://github.com/Suyashman/SAM3-Autolabeler):** a labelling assistant on Meta's SAM3 that exports YOLO segmentation datasets, with per-class confidence thresholds and a review queue that shows the most uncertain items first. F1 on PPE: person 0.90, vest 0.87, helmet 0.85, goggles 0.65. Its README documents where it fails.
- **[YOLO Dataset Manager](https://github.com/Suyashman/dataset-manager):** a local app covering dataset merging, in-browser annotation, augmentation, training with live loss and mAP charts, and inference testing on images, video and webcam.
- **[SnakeNGen](https://github.com/Suyashman/SnakeNGen):** a small version of Google's GameNGen idea. A 2M-parameter U-Net replaces the game engine of Snake and predicts each next frame from recent frames and the player's action.
- **[Driver-assistance testbed on RC cars](https://github.com/Suyashman/advance-driver-assistance-system):** overhead-camera tracking, lane-departure and collision warning, automatic emergency braking, and a vehicle-to-vehicle layer over MQTT.
- **[Trading simulator](https://github.com/Suyashman/multi-client-trading-simulator):** a matching engine with partial fills, pushed live to every open tab by PostgreSQL triggers and LISTEN/NOTIFY.
- **[Crop disease prediction](https://github.com/arya20072004/crop-disease-detection):** a team project, a mobile app using a CNN for diagnosis and an LSTM for risk forecasting.
- **[DLSS benchmark](https://github.com/Suyashman/nvidia-dlss-performance-comparison-)** across five RTX GPUs, and **[hand-gesture drawing](https://github.com/Suyashman/hand-gesture-drawing)** with MediaPipe.

</details>

<br/>

## Publications

- **[Paper 1 title]**, *[venue, year]*. [IEEE Xplore](https://ieeexplore.ieee.org/document/11702370)
- **[Paper 2 title]**, *[venue, year]*. [IEEE Xplore](https://ieeexplore.ieee.org/document/11323656)

<br/>

## Tools I work with

<p align="center"><sub><b>LANGUAGES</b></sub></p>

<table align="center">
<tr>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/python/python-original.svg" width="38" height="38" alt="Python"/><br/><sub>Python</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/cplusplus/cplusplus-original.svg" width="38" height="38" alt="C++"/><br/><sub>C++</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/c/c-original.svg" width="38" height="38" alt="C"/><br/><sub>C</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/java/java-original.svg" width="38" height="38" alt="Java"/><br/><sub>Java</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/javascript/javascript-original.svg" width="38" height="38" alt="JavaScript"/><br/><sub>JavaScript</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/typescript/typescript-original.svg" width="38" height="38" alt="TypeScript"/><br/><sub>TypeScript</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/r/r-original.svg" width="38" height="38" alt="R"/><br/><sub>R</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/bash/bash-original.svg" width="38" height="38" alt="Bash"/><br/><sub>Bash</sub></td>
</tr>
</table>

<p align="center"><sub><b>VISION AND MACHINE LEARNING</b></sub></p>

<table align="center">
<tr>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/pytorch/pytorch-original.svg" width="38" height="38" alt="PyTorch"/><br/><sub>PyTorch</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/tensorflow/tensorflow-original.svg" width="38" height="38" alt="TensorFlow"/><br/><sub>TensorFlow</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/opencv/opencv-original.svg" width="38" height="38" alt="OpenCV"/><br/><sub>OpenCV</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/scikitlearn/scikitlearn-original.svg" width="38" height="38" alt="scikit-learn"/><br/><sub>scikit-learn</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/numpy/numpy-original.svg" width="38" height="38" alt="NumPy"/><br/><sub>NumPy</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/pandas/E70488" width="38" height="38" alt="pandas"/><br/><sub>pandas</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/onnx/005CED" width="38" height="38" alt="ONNX"/><br/><sub>ONNX</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/nvidia/76B900" width="38" height="38" alt="CUDA"/><br/><sub>CUDA</sub></td>
</tr>
</table>

<p align="center"><sub><b>BACKEND AND WEB</b></sub></p>

<table align="center">
<tr>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/fastapi/fastapi-original.svg" width="38" height="38" alt="FastAPI"/><br/><sub>FastAPI</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/sqlalchemy/D71F00" width="38" height="38" alt="SQLAlchemy"/><br/><sub>SQLAlchemy</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/nodejs/nodejs-original.svg" width="38" height="38" alt="Node.js"/><br/><sub>Node.js</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/react/react-original.svg" width="38" height="38" alt="React"/><br/><sub>React</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/vitejs/vitejs-original.svg" width="38" height="38" alt="Vite"/><br/><sub>Vite</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/tailwindcss/tailwindcss-original.svg" width="38" height="38" alt="Tailwind"/><br/><sub>Tailwind</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/html5/html5-original.svg" width="38" height="38" alt="HTML5"/><br/><sub>HTML5</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/css3/css3-original.svg" width="38" height="38" alt="CSS3"/><br/><sub>CSS3</sub></td>
</tr>
</table>

<p align="center"><sub><b>DATA AND INFRASTRUCTURE</b></sub></p>

<table align="center">
<tr>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/postgresql/postgresql-original.svg" width="38" height="38" alt="PostgreSQL"/><br/><sub>PostgreSQL</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/mysql/mysql-original.svg" width="38" height="38" alt="MySQL"/><br/><sub>MySQL</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/sqlite/sqlite-original.svg" width="38" height="38" alt="SQLite"/><br/><sub>SQLite</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/docker/docker-original.svg" width="38" height="38" alt="Docker"/><br/><sub>Docker</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/githubactions/githubactions-original.svg" width="38" height="38" alt="Actions"/><br/><sub>Actions</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/linux/FCC624" width="38" height="38" alt="Linux"/><br/><sub>Linux</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/windows8/windows8-original.svg" width="38" height="38" alt="Windows"/><br/><sub>Windows</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/git/git-original.svg" width="38" height="38" alt="Git"/><br/><sub>Git</sub></td>
</tr>
</table>

<p align="center"><sub><b>EMBEDDED AND TOOLING</b></sub></p>

<table align="center">
<tr>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/arduino/arduino-original.svg" width="38" height="38" alt="Arduino"/><br/><sub>Arduino</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/flutter/flutter-original.svg" width="38" height="38" alt="Flutter"/><br/><sub>Flutter</sub></td>
<td align="center" width="92"><img src="https://cdn.simpleicons.org/mqtt/B565D8" width="38" height="38" alt="MQTT"/><br/><sub>MQTT</sub></td>
<td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.16.0/icons/vscode/vscode-original.svg" width="38" height="38" alt="VS Code"/><br/><sub>VS Code</sub></td>
</tr>
</table>


<br/>

<p align="center">
  <sub>Open to conversations about computer vision, edge inference and shipping ML products. Email is the fastest way to reach me.</sub>
</p>
