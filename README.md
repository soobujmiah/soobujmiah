# Sobuj Miah

**Independent Software & AI Systems Engineer** | On-Device AI · Android · Linux · ARM64 · GPU/NPU

I design, build, debug, and validate systems close to the hardware — mostly on Android and ARM64 Linux, with a focus on local LLM inference and native toolchain engineering. I'm self-taught, and I build entirely from an Android phone (Termux/PRoot Debian, no PC): every project here routes compilation and CI through GitHub Actions, and every hardware-dependent claim is checked against one physical reference device before I call it done.

`Android · On-Device AI · Automation · ARM64 · Real-Device Engineering`

## Flagship projects

| Project | What it is | Engineering evidence |
|---|---|---|
| **[LAI](https://github.com/soobujmiah/lai)** | Bangla-first local AI + consent-driven Android automation runtime | Real arm64 llama.cpp CPU inference (GGUF, streaming, KV-prefix reuse), device-measured throughput and TTFT, Shizuku/Accessibility consent boundaries with hash-chained audit trail, and a symbolized root-cause diagnosis of an Adreno Vulkan driver crash (`vkCmdBindPipeline` SIGSEGV) that shaped a fail-closed CPU-default architecture |
| **[GGEN](https://github.com/soobujmiah/ggen)** | Android-first creative & document studio (Flutter/Dart) | Pure-Dart core with 143 unit tests, a Flutter shell with 353 widget/controller tests, deterministic text-layout engine with a proven conservation invariant, transactional file persistence with SHA-256 receipts, and a multi-stage PR history validated on a physical device round after round |

## Systems & real-device engineering

Infrastructure built because the tools these flagship projects needed didn't exist yet on this hardware — not side projects, the substrate the flagship work runs on.

| Project | What it is | Engineering evidence |
|---|---|---|
| **[ADT](https://github.com/soobujmiah/adt)** | Native ARM64 Android development toolchain | Builds Android SDK build-tools/platform-tools from AOSP source for Linux ARM64/glibc (not just Android/Bionic), ships SHA-256-verified offline release artifacts, and validates the full pipeline end-to-end — native source → APK → sign → install → JNI load → run — on real hardware |
| **[Ternux](https://github.com/soobujmiah/ternux)** | No-root Debian/Xfce Linux desktop on an Android phone | Zink/Turnip Vulkan and VirGL GPU routes, a modular Bash installer with doctor/repair/benchmark tooling, and device evidence that explicitly separates measured results from untested claims |

## Technical domains

- **On-device AI / LLM runtime** — llama.cpp, GGUF quantization, KV-cache reuse, model integrity verification, backend routing between CPU/GPU/NPU
- **Android systems** — Kotlin, Flutter, Accessibility services, Shizuku privileged execution, consent-gated automation
- **Linux / ARM64 toolchains** — native aarch64 build systems, AOSP source builds, Clang/CMake/Ninja, Termux + PRoot environments
- **GPU acceleration** — Vulkan (Mesa Turnip, Zink), OpenGL-on-Vulkan translation, native crash diagnosis on vendor drivers
- **NPU (in progress)** — Qualcomm Hexagon/QNN evaluation; treated as a qualification gate, not a shipped capability, until device evidence exists
- **Engineering operations** — GitHub Actions CI/CD, reproducible builds, signed releases, real-device validation as a release gate

## How I work

Every repository above documents what's **implemented and device-verified** separately from what's **experimental** or **planned** — I'd rather show you a real CPU inference number and an honest "GPU crashes here, this is why" than a claim I can't back with a log. Architecture decisions, test counts, CI status, and device evidence live in each repo's own docs, not just in prose here.

Only the heavy build runs remotely, on GitHub Actions. Everything else — writing and editing the code, pulling the built artifact back, installing it over ADB, launching it, and debugging what goes wrong — happens on the same phone against the same physical reference device. Failures loop straight back into a fix → rebuild → redeploy → retest pass. No separate build machine, test lab, or handoff between roles.

## Currently

Qualifying GPU/NPU acceleration paths (Vulkan on Adreno, Hexagon/QNN) against real hardware, and hardening the CI/release pipeline across these projects. Also building **[DocDr](https://github.com/soobujmiah/docdr)**, a mobile-first document workspace — early development, a clean rebuild of a document-generation approach proven in earlier work.

---

More detail, bilingual (বাংলা/English), and an evidence-graded claims model: **[soobujmiah.github.io](https://soobujmiah.github.io)**
