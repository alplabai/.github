## Alp Lab AI

We're building **Signex** — an open-source, AI-first electronics design automation tool.

### What is Signex?

Signex is a KiCad-compatible schematic and PCB editor built in Rust with GPU-accelerated rendering. It aims to deliver Altium Designer-quality UX on top of the open KiCad file format — so engineers get a better editor without leaving the ecosystem they trust.

**Two editions from one codebase:**

- **Signex Community** (Apache-2.0) — full schematic editor, PCB editor with interactive routing and DRC, 3D viewer, simulation, plugin system. Free forever.
- **Signex Pro** (subscription) — adds Signal AI (Claude-powered design copilot), real-time collaboration, and Signex 365 cloud PLM.

### Current Status

We're currently building **v0.6** (full schematic editor). The schematic viewer, editor, and canvas are working. Next up: ERC validation, PDF/BOM output, then PCB.

### Featured Repositories

| Repository | Description |
|---|---|
| [**signex**](https://github.com/alplabai/signex) | Signex EDA editor — Rust + Iced + wgpu |
| [ngspice](https://github.com/alplabai/ngspice) | SPICE circuit simulator (fork with Signex integration patches) |
| [openEMS](https://github.com/alplabai/openEMS) | EC-FDTD electromagnetic solver (fork with fixes and CUDA engine) |
| [elmerfem](https://github.com/alplabai/elmerfem) | Elmer FEM solver (fork for thermal and DC IR drop analysis) |

### Tech Stack

Rust, wgpu, Iced 0.14, KiCad S-expression format, ngspice (SPICE), OpenEMS (EM/FDTD), Elmer (FEM), Supabase (collaboration + PLM)

### Get Involved

- Check out [Signex](https://github.com/alplabai/signex) and the [contributing guide](https://github.com/alplabai/signex/blob/dev/CONTRIBUTING.md)
- Report bugs, add KiCad test fixtures, or pick up a [good first issue](https://github.com/alplabai/signex/labels/good%20first%20issue)
- See the [roadmap](https://github.com/alplabai/signex/blob/dev/docs/ROADMAP.md) for what's coming next
