## Alp Lab AI

We build **edge AI hardware and the software that runs on it** — from the
[E1M](https://github.com/alplabai/e1m-spec) open-standard System-on-Module
pinout, through the [Alp SDK](https://github.com/alplabai/alp-sdk) firmware
framework that targets it, to [Signex](https://github.com/alplabai/signex),
our open-source AI-first EDA tool.

### The two stacks

#### Edge AI · E1M + Alp SDK

- **[E1M Standard 1.0](https://github.com/alplabai/e1m-spec)** — open
  pinout + mechanical envelope for AI-capable Systems-on-Module
  (35×35 mm and 45×65 mm form factors).  Lets any silicon vendor ship
  pin-compatible modules; lets any product board target one connector
  and accept multiple SoMs.
- **[Alp SDK](https://github.com/alplabai/alp-sdk)** — embedded firmware
  framework for E1M modules.  A single `board.yaml` drives Zephyr,
  Yocto, and bare-metal builds across Alif Ensemble, Renesas RZ/V2N,
  NXP i.MX 93, and DEEPX DX-M1 silicon.  Ships with 20+ chip drivers,
  ML inference dispatch (TFLite Micro → Ethos-U / DRP-AI / DEEPX),
  runtime hardware identification (ADC + on-module EEPROM manifest),
  and a VS Code configurator.

#### Open EDA · Signex

- **[Signex](https://github.com/alplabai/signex)** is a KiCad-compatible
  schematic and PCB editor built in Rust with GPU-accelerated rendering.
  It aims to deliver Altium Designer-quality UX on top of the open KiCad
  file format — engineers get a better editor without leaving the
  ecosystem they trust.
  - **Signex Community** (Apache-2.0) — full schematic editor, PCB editor
    with interactive routing and DRC, 3D viewer, simulation, plugin
    system.  Free forever.
  - **Signex Pro** (subscription) — adds Signal AI (Claude-powered design
    copilot), real-time collaboration, and Signex 365 cloud PLM.

### Current status

- **Alp SDK**: v0.3 candidate — `board.yaml` project config, hardware-
  revision tracking, full peripheral surface, VS Code extension, EEPROM
  manifest + production-test tooling all in.  V0.4 lands Yocto first-
  class for V2N / V2N-M1, secure boot + OTA on AEN-Zephyr.
- **Signex**: v0.6 candidate (full schematic editor).  Schematic viewer,
  editor, and canvas working; next up is ERC validation, PDF/BOM output,
  then PCB.

### Featured repositories

#### Edge AI · E1M + Alp SDK

| Repository | Description |
|---|---|
| [**alp-sdk**](https://github.com/alplabai/alp-sdk) | Embedded SDK for E1M Systems-on-Module — Zephyr / Yocto / bare-metal |
| [**alp-sdk-vscode**](https://github.com/alplabai/alp-sdk-vscode) | VS Code extension — schema-aware `board.yaml` editor, GUI configurator, west wrappers |
| [**e1m-spec**](https://github.com/alplabai/e1m-spec) | E1M open-standard pinout + mechanical envelope (35×35 + 45×65 mm) |
| [**cc3501e-firmware**](https://github.com/alplabai/cc3501e-firmware) | TI CC3501E Wi-Fi 6 + BLE 5.4 coprocessor firmware (companion to alp-sdk on E1M-AEN) |
| [**gd32g5x3-firmware-library**](https://github.com/alplabai/gd32g5x3-firmware-library) | Vendored GD32G5x3 Firmware Library — consumed by alp-sdk's gd32-bridge build |
| [**alp-zephyr-modules**](https://github.com/alplabai/alp-zephyr-modules) | Out-of-tree Zephyr board files for the E1M-* EVKs |

#### Open EDA · Signex

| Repository | Description |
|---|---|
| [**signex**](https://github.com/alplabai/signex) | Signex EDA editor — Rust + Iced + wgpu |
| [ngspice](https://github.com/alplabai/ngspice) | SPICE circuit simulator (fork with Signex integration patches) |
| [openEMS](https://github.com/alplabai/openEMS) | EC-FDTD electromagnetic solver (fork with fixes and CUDA engine) |
| [elmerfem](https://github.com/alplabai/elmerfem) | Elmer FEM solver (fork for thermal and DC IR drop analysis) |

### Tech stack

**Edge AI**: Zephyr RTOS, Yocto, Alif Ensemble, Renesas RZ/V2N, NXP
i.MX 93, DEEPX DX-M1, TFLite Micro, Arm Ethos-U, Renesas DRP-AI, MbedTLS,
LVGL, CMSIS-DSP.

**EDA**: Rust, wgpu, Iced 0.14, KiCad S-expression format, ngspice
(SPICE), OpenEMS (EM/FDTD), Elmer (FEM), Supabase (collaboration + PLM).

### Get involved

- **[Alp SDK](https://github.com/alplabai/alp-sdk)** — embedded firmware
  on the open E1M pinout; check the `docs/getting-started.md` walkthrough
  and the per-peripheral examples for an entry point.
- **[Signex](https://github.com/alplabai/signex)** — open EDA for
  schematic + PCB design; see the
  [contributing guide](https://github.com/alplabai/signex/blob/dev/CONTRIBUTING.md)
  and pick up a [good first issue](https://github.com/alplabai/signex/labels/good%20first%20issue).
- Each repo carries its own `CONTRIBUTING` file + issue templates.
