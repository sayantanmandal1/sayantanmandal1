<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=30&pause=1000&color=FF6A2B&center=true&vCenter=true&width=820&lines=Hi%2C+I'm+Sayantan;Software+Engineer+%C2%B7+Systems+%26+Backend;I+build+things+from+scratch+and+measure+them" alt="typing" />

**[Portfolio](https://portfolio-red-tau-coral.vercel.app/)** · **[LinkedIn](https://www.linkedin.com/in/sayantan-mandal-8a14b7202/)** · **[LeetCode](https://leetcode.com/u/sayonara1337/)** · **[Email](mailto:msayantan05@gmail.com)**

</div>

---

### About

Software engineer at **Honeywell** (.NET / C# / React), working end to end across systems programming, backend services and applied AI.

I build the hard version on purpose — a search engine rather than a search wrapper, a VPN rather than a VPN client — and then **measure it**, because an unmeasured claim is just an opinion.

- 🔭 **Now:** Software Engineer @ Honeywell — .NET (C#), React, Kubernetes
- 🌱 **Into:** distributed systems, developer tooling, information retrieval
- 🧩 **825+** LeetCode solved (130+ Hard)
- 🎓 B.Tech CSE, VIT-AP — CGPA 9.03/10
- 📫 msayantan05@gmail.com

---

### Selected work

Each of these is measured, not described. The numbers below are reproduced by a command in the repo.

| project | what it is | measured result |
|---|---|---|
| **[argus](https://github.com/sayantanmandal1/argus)** <br/> `Java 17 · zero deps` | A full-text **search engine** *and* a **browser rendering engine**, from scratch — inverted index, BM25, query DSL, WAL, plus HTML/CSS/layout/paint and a JavaScript interpreter | **98.9%** of scoring work eliminated by Block-Max WAND with provably identical rankings · **218 tests** · durability proven by killing a real JVM with `halt(9)` |
| **[MyVPN](https://github.com/sayantanmandal1/MyVPN)** <br/> `Rust · QUIC · Wintun` | Serverless **peer-to-peer VPN** with NAT hole-punching, full-tunnel routing, kill-switch and DNS-leak hardening | Security controls **unit-tested, not asserted** — injection guard rejects 8 payloads, constant-time proof compare, domain-separated key derivation |
| **[chromaforge](https://github.com/sayantanmandal1/chromaforge)** <br/> `C++17 · multithreaded` | **Colour-grading engine** — 3D LUT trilinear, separable convolution, ACES/Reinhard tone mapping, custom thread pool | **13.4×** separable vs naive 4K blur · white balance **306 → 473 Mpix/s** via lookup tables, bit-identical output |
| **[GameManager](https://github.com/sayantanmandal1/GameManager)** <br/> `NestJS · Socket.IO · Expo` | **Server-authoritative multiplayer framework** validated across 45 distinct rulesets, with per-player hidden-state projection and WebRTC voice | Crossplay web + Android, per-commit APK from CI |
| **[VoiceRep](https://github.com/sayantanmandal1/VoiceRep)** <br/> `Python · PyTorch` | Consent-aware, watermarked **zero-shot voice cloning** with an independent verification pipeline | Held-out LibriSpeech benchmark with acceptance gates independent of the engine's own score |
| **[BitDown](https://github.com/sayantanmandal1/BitDown)** <br/> `Rust · Tauri · axum` | **BitTorrent client** with DHT/PEX/UPnP and a byte-range HTTP server that streams a file while it downloads | Shipped Windows installer, auto-released from CI |

---

### Engineering notes

Three things these repos taught me that are worth more than the features:

- **A randomised differential test found a bug no example test could.** Argus scored the same document as `6.278620742691458` on one path and `...457` on another — both scorers summed over a `PriorityQueue`, whose iteration order is unspecified, and floating-point addition is not associative. Rankings were non-deterministic *across runs*. Fixed by scoring in fixed clause order.
- **Work skipped ≠ time saved.** Block-Max WAND eliminates 94.5% of scoring at top-10 but only runs 1.6× faster, because the postings are already in RAM so nothing is saved on I/O. Reporting both numbers is the honest version.
- **A single timing is not a benchmark.** On a hybrid P-core/E-core laptop, identical chromaforge runs disagreed by 30–50%. The harness now reports medians across five bursts and prints the spread.

---

### Tech

![Java](https://img.shields.io/badge/Java-007396?logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?logo=dotnet&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)

![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![Spring](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)

---

### Open source

Fixes sent upstream to libraries I use:

- **[bytesize](https://github.com/bytesize-rs/bytesize/pull/171)** (Rust) — fixed `f64` precision loss when parsing large byte counts
- **[go-humanize](https://github.com/dustin/go-humanize/pull/151)** (Go) — exact integer parsing in `ParseBytes`
- **[luxon](https://github.com/moment/luxon/pull/1787)** (JS) — reject out-of-range 12-hour values in `fromFormat`

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=sayantanmandal1&show_icons=true&hide_border=true&theme=transparent&icon_color=FF6A2B&title_color=FF6A2B" height="150" alt="stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sayantanmandal1&layout=compact&hide_border=true&theme=transparent&title_color=FF6A2B" height="150" alt="langs" />

<br/><br/>

**Open to SDE / new-grad roles · 2026**

</div>
