<div align="center">
  <img src="./assets/profile-banner.svg" alt="Sobuj Miah — Independent Software & AI Systems Engineer" width="100%" />
</div>

# Sobuj Miah

**Independent Software & AI Systems Engineer**  
On-Device AI · Android · ARM64 Linux · Native Tooling · Software Systems

I build systems close to the hardware: local LLM inference on ARM devices, consent-bound Android automation, native toolchains compiled from AOSP source, and Linux desktops running on phones. Self-taught, and built entirely from an Android phone (Termux / PRoot Debian, no PC) — heavy compilation routes through GitHub Actions, and every hardware-dependent claim is checked against one physical reference device before I call it done.

<div align="center">
  <img src="./assets/profile-stats.svg" alt="Engineering telemetry: featured systems, documented tests, AOSP releases, canonical links and delivery loop" width="100%" />
</div>

## What I Build

- **On-device AI runtimes** — llama.cpp-based local inference on ARM64 Android: GGUF models, streaming, KV-prefix reuse, model-integrity verification, CPU/GPU backend routing
- **Consent-driven Android automation** — Accessibility and Shizuku privileged execution behind explicit user consent, with a hash-chained audit trail
- **Native ARM64 toolchains** — Android SDK build-tools and platform-tools built from AOSP source for Linux ARM64/glibc, shipped as SHA-256-verified offline artifacts
- **Linux on Android** — no-root Debian/Xfce desktops with real GPU routes (Zink/Turnip Vulkan, VirGL) and doctor/repair/benchmark tooling
- **Bangla-first applications** — business ledger and document tools where Bengali is the primary language, not a translation layer

## Featured Work

| Project | What it is | Engineering evidence |
|---|---|---|
| [LAI](https://github.com/soobujmiah/lai) <br> ![LAI CI](https://github.com/soobujmiah/lai/actions/workflows/android_build.yml/badge.svg) | Bangla-first local AI + consent-driven Android automation runtime | Real arm64 llama.cpp CPU inference (GGUF, streaming, KV-prefix reuse) with device-measured throughput and TTFT; Shizuku/Accessibility consent boundaries with a hash-chained audit trail; symbolized root-cause diagnosis of an Adreno Vulkan driver crash (`vkCmdBindPipeline` SIGSEGV) that shaped a fail-closed CPU-default architecture · [v0.9.7](https://github.com/soobujmiah/lai/releases) |
| [GGEN](https://github.com/soobujmiah/ggen) <br> ![GGEN core CI](https://github.com/soobujmiah/ggen/actions/workflows/core.yml/badge.svg) | Android-first creative & document studio (Flutter/Dart) | Pure-Dart core with 143 unit tests and a Flutter shell with 353 widget/controller tests; deterministic text-layout engine with a proven conservation invariant; transactional file persistence with SHA-256 receipts |
| [ADT](https://github.com/soobujmiah/adt) <br> ![ADT CI](https://github.com/soobujmiah/adt/actions/workflows/build.yml/badge.svg) | Native ARM64 Android development toolchain | Builds Android SDK build-tools/platform-tools from AOSP source for Linux ARM64/glibc (not only Android/Bionic); ships SHA-256-verified offline release artifacts; validates the full pipeline on real hardware — native source → APK → sign → install → JNI load → run · [v37.0.0](https://github.com/soobujmiah/adt/releases) |
| [Ternux](https://github.com/soobujmiah/ternux) <br> ![Ternux CI](https://github.com/soobujmiah/ternux/actions/workflows/ci.yml/badge.svg) | No-root Debian/Xfce Linux desktop on an Android phone | Zink/Turnip Vulkan and VirGL GPU routes; modular Bash installer with doctor/repair/benchmark tooling; glmark2 score 140 (OpenGL 4.6 via Zink) measured on device, with device evidence that separates measured results from untested claims |
| [Songjog](https://github.com/soobujmiah/songjog) <br> ![Songjog CI](https://github.com/soobujmiah/songjog/actions/workflows/flutter-ci.yml/badge.svg) | Bangla-first business & institution operations app | Owner Edition: fast daily entry, local SQLite records, auditable corrections instead of destructive deletes; 94 tests green on CI; export/diagnostics validated on the physical reference device |

## Research & Engineering

Each repository documents what is **implemented and device-verified** separately from what is **experimental** or **planned**. The current boundary:

- **Validated on hardware** — arm64 llama.cpp CPU inference with measured throughput/TTFT; AOSP toolchain builds for ARM64 glibc with verified artifacts; Vulkan desktop rendering on Android via Zink/Turnip with a measured glmark2 score; Bangla text shaping and layout invariants under test
- **Diagnosed, deliberately not shipped** — the Adreno Vulkan crash in LAI's GPU inference path: root-caused with symbols, then gated fail-closed to CPU rather than shipped half-working
- **Experimental / in qualification** — GPU LLM acceleration (Vulkan on Adreno) and Qualcomm Hexagon/QNN NPU paths: treated as qualification gates, not shipped capabilities, until device evidence exists

## Tech Stack

<div align="center">

[![Kotlin](https://img.shields.io/badge/Kotlin-07150D?style=flat-square&logo=kotlin&logoColor=4ade80)](https://kotlinlang.org/) [![Dart](https://img.shields.io/badge/Dart-07150D?style=flat-square&logo=dart&logoColor=4ade80)](https://dart.dev/) [![Flutter](https://img.shields.io/badge/Flutter-07150D?style=flat-square&logo=flutter&logoColor=4ade80)](https://flutter.dev/) [![C++](https://img.shields.io/badge/C%2B%2B-07150D?style=flat-square&logo=cplusplus&logoColor=4ade80)](https://isocpp.org/) [![Bash](https://img.shields.io/badge/Bash-07150D?style=flat-square&logo=gnubash&logoColor=4ade80)](https://www.gnu.org/software/bash/)

[![Python](https://img.shields.io/badge/Python-07150D?style=flat-square&logo=python&logoColor=4ade80)](https://www.python.org/) [![CMake](https://img.shields.io/badge/CMake-07150D?style=flat-square&logo=cmake&logoColor=4ade80)](https://cmake.org/) [![SQLite](https://img.shields.io/badge/SQLite-07150D?style=flat-square&logo=sqlite&logoColor=4ade80)](https://sqlite.org/) [![Vulkan](https://img.shields.io/badge/Vulkan-07150D?style=flat-square&logo=vulkan&logoColor=4ade80)](https://www.vulkan.org/) [![Linux](https://img.shields.io/badge/Linux-07150D?style=flat-square&logo=linux&logoColor=4ade80)](https://www.linux.org/) [![Debian](https://img.shields.io/badge/Debian-07150D?style=flat-square&logo=debian&logoColor=4ade80)](https://www.debian.org/)

[![Android](https://img.shields.io/badge/Android-07150D?style=flat-square&logo=android&logoColor=4ade80)](https://developer.android.com/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-07150D?style=flat-square&logo=githubactions&logoColor=4ade80)](https://github.com/features/actions) [![Git](https://img.shields.io/badge/Git-07150D?style=flat-square&logo=git&logoColor=4ade80)](https://git-scm.com/) [![Termux](https://img.shields.io/badge/Termux-07150D?style=flat-square&logo=termux&logoColor=4ade80)](https://termux.dev/)

`Kotlin` · `Dart/Flutter` · `C++ (llama.cpp)` · `Bash` · `Python` · `CMake/Ninja/Clang` · `AOSP source builds` · `SQLite` · `GGUF/llama.cpp` · `Vulkan (Mesa Turnip, Zink)` · `VirGL` · `Shizuku/Accessibility` · `Termux + PRoot Debian` · `GitHub Actions CI/CD`

</div>

## How I Work

Only the heavy build runs remotely, on GitHub Actions. Everything else — writing and editing code, pulling the built artifact back, installing it over ADB, launching it, debugging what goes wrong — happens on the same phone against the same physical reference device. Failures loop straight back into a fix → rebuild → redeploy → retest pass. No separate build machine, test lab, or handoff between roles.

## Currently

Qualifying GPU/NPU acceleration paths (Vulkan on Adreno, Hexagon/QNN) against real hardware, hardening CI/release pipelines across these projects, and building [DocDr](https://github.com/soobujmiah/docdr) — a mobile-first offline document workspace, early development.

## Find Me Online

<div align="center">

**Core**  
[![GitHub](https://img.shields.io/badge/GitHub-050507?style=flat-square&logo=github&logoColor=4ade80&labelColor=050507&color=163D27)](https://github.com/soobujmiah) [![Portfolio](https://img.shields.io/badge/Portfolio-050507?style=flat-square&logo=googlechrome&logoColor=4ade80&labelColor=050507&color=163D27)](https://soobujmiah.github.io)

**Professional**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-050507?style=flat-square&logo=linkedin&logoColor=4ade80&labelColor=050507&color=185C3A)](https://linkedin.com/in/soobujmiah) [![Peerlist](https://img.shields.io/badge/Peerlist-050507?style=flat-square&logo=peerlist&logoColor=4ade80&labelColor=050507&color=185C3A)](https://peerlist.io/soobujmiah) [![Product Hunt](https://img.shields.io/badge/Product_Hunt-050507?style=flat-square&logo=producthunt&logoColor=4ade80&labelColor=050507&color=185C3A)](https://producthunt.com/@soobujmiah)

**AI / Developer**  
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-050507?style=flat-square&logo=huggingface&logoColor=4ade80&labelColor=050507&color=0F5132)](https://huggingface.co/soobujmiah) [![DEV.to](https://img.shields.io/badge/DEV.to-050507?style=flat-square&logo=devdotto&logoColor=4ade80&labelColor=050507&color=0F5132)](https://dev.to/soobujmiah) [![Hashnode](https://img.shields.io/badge/Hashnode-050507?style=flat-square&logo=hashnode&logoColor=4ade80&labelColor=050507&color=0F5132)](https://hashnode.com/@soobujmiah) [![Medium](https://img.shields.io/badge/Medium-050507?style=flat-square&logo=medium&logoColor=4ade80&labelColor=050507&color=0F5132)](https://medium.com/@soobujmiah)

**Social**  
[![X](https://img.shields.io/badge/X-050507?style=flat-square&logo=x&logoColor=4ade80&labelColor=050507&color=14532D)](https://x.com/soobujmiah) [![Instagram](https://img.shields.io/badge/Instagram-050507?style=flat-square&logo=instagram&logoColor=4ade80&labelColor=050507&color=14532D)](https://instagram.com/soobujmiah) [![Threads](https://img.shields.io/badge/Threads-050507?style=flat-square&logo=threads&logoColor=4ade80&labelColor=050507&color=14532D)](https://threads.net/@soobujmiah) [![Facebook](https://img.shields.io/badge/Facebook-050507?style=flat-square&logo=facebook&logoColor=4ade80&labelColor=050507&color=14532D)](https://facebook.com/soobujmiah) [![YouTube](https://img.shields.io/badge/YouTube-050507?style=flat-square&logo=youtube&logoColor=4ade80&labelColor=050507&color=14532D)](https://youtube.com/@soobujmiah)

**Direct**  
[![Telegram](https://img.shields.io/badge/Telegram-050507?style=flat-square&logo=telegram&logoColor=4ade80&labelColor=050507&color=123F2A)](https://t.me/soobujmiah) [![WhatsApp](https://img.shields.io/badge/WhatsApp-050507?style=flat-square&logo=whatsapp&logoColor=4ade80&labelColor=050507&color=123F2A)](https://wa.me/soobujmiah)

**Personal**  
[![About.me](https://img.shields.io/badge/About.me-050507?style=flat-square&logo=aboutdotme&logoColor=4ade80&labelColor=050507&color=103521)](https://about.me/soobujmiah)

</div>

---

More detail — bilingual (বাংলা/English), with an evidence-graded claims model and a per-claim verification log: **[soobujmiah.github.io](https://soobujmiah.github.io)**
