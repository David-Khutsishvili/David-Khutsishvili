<h1 align="center">David Khutsishvili</h1>

<p align="center">
  <b>Software Engineer · Robotics · Embedded Systems</b><br>
  B.Sc. Computer Science, Holon Institute of Technology
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/davidkhuts/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDQuNDU1djYuMjg2ek01LjMzNyA3LjQzM2EyLjA2MiAyLjA2MiAwIDEgMSAwLTQuMTI1IDIuMDYyIDIuMDYyIDAgMCAxIDAgNC4xMjV6TTcuMTE5IDIwLjQ1MkgzLjU1NVY5aDMuNTY0djExLjQ1MnpNMjIuMjI1IDBIMS43NzFDLjc5MiAwIDAgLjc3NCAwIDEuNzI5djIwLjU0MkMwIDIzLjIyNy43OTIgMjQgMS43NzEgMjRoMjAuNDUxQzIzLjIgMjQgMjQgMjMuMjI3IDI0IDIyLjI3MVYxLjcyOUMyNCAuNzc0IDIzLjIgMCAyMi4yMjIgMGguMDAzeiIvPjwvc3ZnPg==&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:davidhuzt@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## About me

I build software end to end, from backend services and web apps down to firmware, sensors and motors.
I'm most at home where code meets the physical world: robots that see and listen, devices that measure,
and systems that have to work reliably in real time.

- **Software engineering**: backend services and full-stack apps. REST and WebSocket APIs with FastAPI, React + TypeScript frontends, SQL, tested with Pytest.
- **Robotics**: perception, control and autonomy. ROS 2, NVIDIA Isaac Sim, Webots, PID control, humanoid robots (NAO).
- **Embedded systems**: C/C++ firmware on Arduino, ARM and Raspberry Pi. I2C, UART, FreeRTOS, custom serial protocols.
- **Applied AI**: putting models into live systems. Computer vision, speaker verification and on-device inference with PyTorch, OpenCV and YOLO.

> *Solve known problems, and find new problems to solve.*

---

## Featured projects

### [3D Embedded Scanner](https://github.com/David-Khutsishvili/3D-embedded-scanner)
*Embedded · Full-stack · 3D reconstruction*

An Arduino-based 3D scanner built from scratch: hardware, firmware and a live control app.

- C++ firmware on an Arduino Uno R4 WiFi drives 3 servos and two VL53L1X time-of-flight sensors over I2C, with a custom serial protocol and a hardware watchdog.
- Full-stack control app: a FastAPI backend (REST, WebSocket, SQLite) and a React + TypeScript + three.js frontend with live 3D streaming and a scanner state machine.
- Turns raw `(θ, height, distance)` samples into point clouds and closed, smoothed surface meshes.

![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![three.js](https://img.shields.io/badge/three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)

### [Secure Gateway](https://github.com/David-Khutsishvili/Secure-Gateway-DLProject)
*AI · Security · Computer vision*

Real-time multi-modal biometric access control: face, voice and a spoken password, fused into a single decision.

- Three independent gates (spoken password, biometric capture, fusion model), plus liveness detection (blink and head pose) that blocks photo and replay attacks.
- Late-fusion MLP over 512-dim FaceNet and 192-dim ECAPA-TDNN embeddings, with a confidence-based fallback policy.
- **99.5%** test accuracy and **98%** impostor detection on the team's dataset.
- In progress: a desktop app that locks selected PC applications behind biometric verification.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=mediapipe&logoColor=white)
![SpeechBrain](https://img.shields.io/badge/SpeechBrain-555555?style=flat-square)

### [ElderGuard: Humanoid Assistant Robot](https://github.com/David-Khutsishvili/ElderGuard-Humanoid_Assistant_Robot)
*Robotics · Edge AI · Distributed systems*

A fully offline personal-assistant robot. A Raspberry Pi 4 "brain" runs all perception and decision-making, and commands a NAO V5 humanoid "body" over TCP.

- Wake word and grammar-based speech recognition (Vosk), plus speaker verification (ECAPA-TDNN on ONNX) so the robot only answers its owner.
- PID visual servoing for face tracking and "follow me", and on-demand YOLOv8n object search ("find my keys") that loads and unloads to fit the Pi's memory.
- A state-machine orchestrator, with the Python 3 brain and the Python 2.7 NAOqi body kept fully decoupled behind a JSON-over-TCP protocol.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![NAO](https://img.shields.io/badge/NAO%20V5-555555?style=flat-square)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLOv8-111F68?style=flat-square)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=mediapipe&logoColor=white)

### [Async Chat App](https://github.com/David-Khutsishvili/Networking-Chat-Project)
*Networking · Backend · Concurrency*

An asynchronous multi-client chat server and terminal client over raw TCP/IP.

- `asyncio` server handling many concurrent clients: registration and login (salted SHA-256), direct messages, group chats with owner permissions, and real-time notifications.
- A custom line-based application protocol over TCP.
- Traffic captured and analyzed in Wireshark to document TCP/IP encapsulation layer by layer.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![asyncio](https://img.shields.io/badge/asyncio-555555?style=flat-square)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)

<!--
  ADD A NEW PROJECT: copy this block above the "More on the way" line and fill it in.

### [Project Name](https://github.com/David-Khutsishvili/REPO-NAME)
*Area · Area · Area*

One-sentence description of what it is and why it matters.

- What you built (the main technical piece).
- An interesting engineering decision or challenge.
- A result or number, if there is one.

![Tech](https://img.shields.io/badge/Tech-555555?style=flat-square&logo=LOGO&logoColor=white)
-->

*More projects on the way.*

---

## Tech stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Backend & web**<br>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![SQL](https://img.shields.io/badge/SQL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

**Robotics & embedded**<br>
![ROS 2](https://img.shields.io/badge/ROS%202-22314E?style=flat-square&logo=ros&logoColor=white)
![Isaac Sim](https://img.shields.io/badge/Isaac%20Sim-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Webots](https://img.shields.io/badge/Webots-555555?style=flat-square)
![Arduino](https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![ARM](https://img.shields.io/badge/ARM-0091BD?style=flat-square&logo=arm&logoColor=white)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-555555?style=flat-square)
![PID control](https://img.shields.io/badge/PID%20control-555555?style=flat-square)
![I2C / UART](https://img.shields.io/badge/I2C%20%2F%20UART-555555?style=flat-square)

**AI & ML**<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-111F68?style=flat-square)
![LLM integration](https://img.shields.io/badge/LLM%20integration-555555?style=flat-square)

**Tools**<br>
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=claude&logoColor=white)

---

## Experience

**Technical Consultant**, Freelance · *2025 – present*<br>
System and product architecture, and feature development for companies and start-ups.

**CS & Math Teaching Assistant**, Hashmonaim High School · *2025 – present*<br>
Teaching OOP, data structures, algorithms and optimization in C++, C# and Python; supervising final projects and running code reviews.

**Robotics Team Mentor & Engineer**, Darca Bat-Yam High School · *2014 – 2023*<br>
Co-founded Bat Yam's first FIRST Robotics Competition team; developed C++ control software with sensor integration.

## Education

**B.Sc. Computer Science**, Holon Institute of Technology · *2022 – 2026*<br>
Highlights: Embedded Systems (100), Networking (93), Deep Learning (90)

---

## GitHub stats

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=David-Khutsishvili&show_icons=true&hide_rank=true&include_all_commits=true&hide_border=true&theme=github_dark">
    <img height="165" src="https://github-readme-stats.vercel.app/api?username=David-Khutsishvili&show_icons=true&hide_rank=true&include_all_commits=true&hide_border=true" alt="GitHub stats">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=David-Khutsishvili&layout=compact&hide=jupyter%20notebook,html&size_weight=0.5&count_weight=0.5&hide_border=true&theme=github_dark">
    <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=David-Khutsishvili&layout=compact&hide=jupyter%20notebook,html&size_weight=0.5&count_weight=0.5&hide_border=true" alt="Top languages">
  </picture>
</p>
