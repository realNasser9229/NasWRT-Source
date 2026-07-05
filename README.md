# NasWRT Open Source Project (NWOSP)

NasWRT is a hyper-lean, barebones, and architecture-neutral network operating system baseline built using pure Buildroot. 

Designed with the "AOSP (Android Open Source Project) for Routers" philosophy, NasWRT does not dictate rigid network applications or heavy web interfaces. Instead, it provides original equipment manufacturers (OEMs) and telecommunications operators with a stable, high-performance, and blank-slate Linux foundation. 

Developers can easily inject their proprietary vendor hardware driver blobs, select their own orchestration daemons, and run `make linux` to build production-grade router firmware.

## Key Features

* **Pure Buildroot Core:** Completely independent of OpenWrt's build architecture, maximizing system freedom and minimizing runtime footprint.
* **Unified Multi-Architecture Support:** Built from the ground up to maintain generic source trees and `defconfigs` across **x86_64**, **MIPS**, and **ARM** targets.
* **OEM Platform:** Designed as a clean canvas. Router manufacturers can seamlessly drop in their proprietary switching/Wi-Fi driver binaries, remote management protocols (TR-069/TR-369), and custom packages without kernel dependency conflicts.
* **Lightweight Ecosystem:** Capable of running securely out of memory (`tmpfs`), dropping idle system overhead dramatically compared to bloatware-heavy stock firmwares.

## How to Get Started

Due to the size of the cross-compilation toolchains and pre-configured source environments, the fully integrated workspace is available as a pre-compressed multi-architecture archive.

1. Download the full source tree archive from the **Releases** section (or our community mirror).
2. Extract the archive into your local or cloud-based compilation workspace.
3. Select your target architecture using `make {text}_defconfig`.
4. Run `make linux` to assemble the monolithic kernel image and file system layers.
