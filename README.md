# Sobuj Miah

**Independent Software & AI Systems Engineer**
On-Device AI · Android · ARM64 Linux · Native Tooling · Software Systems

I build systems close to the hardware: local LLM inference on ARM devices, consent-bound Android automation, native toolchains compiled from AOSP source, and Linux desktops running on phones. Self-taught, and built entirely from an Android phone (Termux / PRoot Debian, no PC) — heavy compilation routes through GitHub Actions, and every hardware-dependent claim is checked against one physical reference device before I call it done.

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

Only what the repositories above actually build with:

`Kotlin` · `Dart/Flutter` · `C++ (llama.cpp)` · `Bash` · `Python` · `CMake/Ninja/Clang` · `AOSP source builds` · `SQLite` · `GGUF/llama.cpp` · `Vulkan (Mesa Turnip, Zink)` · `VirGL` · `Shizuku/Accessibility` · `Termux + PRoot Debian` · `GitHub Actions CI/CD`

## How I Work

Only the heavy build runs remotely, on GitHub Actions. Everything else — writing and editing code, pulling the built artifact back, installing it over ADB, launching it, debugging what goes wrong — happens on the same phone against the same physical reference device. Failures loop straight back into a fix → rebuild → redeploy → retest pass. No separate build machine, test lab, or handoff between roles.

## Currently

Qualifying GPU/NPU acceleration paths (Vulkan on Adreno, Hexagon/QNN) against real hardware, hardening CI/release pipelines across these projects, and building [DocDr](https://github.com/soobujmiah/docdr) — a mobile-first offline document workspace, early development.

## Find Me Online

- **Core** — [GitHub](https://github.com/soobujmiah) · [Portfolio](https://soobujmiah.github.io)
- **Professional** — [LinkedIn](https://linkedin.com/in/soobujmiah) · [Peerlist](https://peerlist.io/soobujmiah) · [Product Hunt](https://producthunt.com/@soobujmiah)
- **AI / Developer** — [Hugging Face](https://huggingface.co/soobujmiah) · [DEV.to](https://dev.to/soobujmiah) · [Hashnode](https://hashnode.com/@soobujmiah) · [Medium](https://medium.com/@soobujmiah)
- **Social** — [X](https://x.com/soobujmiah) · [Instagram](https://instagram.com/soobujmiah) · [Threads](https://threads.net/@soobujmiah) · [Facebook](https://facebook.com/soobujmiah) · [YouTube](https://youtube.com/@soobujmiah)
- **Direct** — [Telegram](https://t.me/soobujmiah) · [WhatsApp](https://wa.me/soobujmiah)
- **Personal** — [About.me](https://about.me/soobujmiah)

---

More detail — bilingual (বাংলা/English), with an evidence-graded claims model and a per-claim verification log: **[soobujmiah.github.io](https://soobujmiah.github.io)**
