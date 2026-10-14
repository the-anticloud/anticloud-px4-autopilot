# PX4 AUTOPILOT

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-space_aerotech-lightgrey)

> Anticloud-hardened packaging of the upstream project `PX4_AUTOPILOT` in category **SPACE AEROTECH**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SPACE AEROTECH · **Upstream:** https://github.com/PX4/PX4-Autopilot · **Upstream pin:** `b798249a61af32c355d95decd2805a6ab4e9d9f1` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<p align="center">
  <a href="https://px4.io">
    <img src="docs/assets/site/px4_logo.svg" alt="PX4 Autopilot" width="240">
  </a>
</p>

<p align="center">
  <em>The autopilot stack the industry builds on.</em>
</p>

<p align="center">
  <a href="https://github.com/PX4/PX4-Autopilot/releases"><img src="https://img.shields.io/github/release/PX4/PX4-Autopilot.svg" alt="Release"></a>
  <a href="https://zenodo.org/badge/latestdoi/22634/PX4/PX4-Autopilot"><img src="https://zenodo.org/badge/22634/PX4/PX4-Autopilot.svg" alt="DOI"></a>
  <a href="https://discord.gg/dronecode"><img src="https://img.shields.io/discord/1022170275984457759?label=discord&logo=discord&logoColor=white&color=5865F2" alt="Discord"></a>
</p>

<p align="center">
  <a href="https://www.bestpractices.dev/projects/6520"><img src="https://www.bestpractices.dev/projects/6520/badge" alt="OpenSSF Best Practices"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/health-score?project=px4" alt="LFX Health Score"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/contributors?project=px4" alt="LFX Contributors"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/active-contributors?project=px4" alt="LFX Active Contributors"></a>
</p>

---

## About

PX4 is an open-source autopilot stack for drones and unmanned vehicles. It supports multirotors, fixed-wing, VTOL, rovers, and many more experimental platforms from racing quads to industrial survey aircraft. It runs on [NuttX](https://nuttx.apache.org/), Linux, and macOS. Licensed under [BSD 3-Clause](LICENSE).

## Why PX4

**Modular architecture.** PX4 is built around [uORB](https://docs.px4.io/main/en/middleware/uorb.html), a [DDS](https://docs.px4.io/main/en/middleware/uxrce_dds.html)-compatible publish/subscribe middleware. Modules are fully parallelized and thread safe. You can build custom configurations and trim what you don't need.

**Wide hardware support.** PX4 runs on a wide range of [autopilot boards](https://docs.px4.io/main/en/flight_controller/) and supports an extensive set of sensors, telemetry radios, and actuators through the [Pixhawk](https://pixhawk.org/) ecosystem.

**Developer friendly.** First-class support for [MAVLink](https://mavlink.io/) and [DDS / ROS 2](https://docs.px4.io/main/en/ros2/) integration. Comprehensive [SITL simulation](https://docs.px4.io/main/en/simulation/), hardware-in-the-loop testing, and [log analysis](https://docs.px4.io/main/en/log/flight_log_analysis.html) tools. An active developer community on [Discord](https://discord.gg/dronecode) and the [weekly dev call](https://docs.px4.io/main/en/contribute/).

**Vendor neutral governance.** PX4 is hosted under the [Dronecode Foundation](https://www.dronecode.org/), part of the Linux Foundation. Business-friendly BSD-3 license. No single vendor controls the roadmap.

## Supported Vehicles

<table>
  <tr>
    <td align="center">
      <a href="https://docs.px4.io/main/en/frames_multicopter/">
        <img src="docs/assets/airframes/types/QuadRotorX.svg" width="50" alt="Multicopter"><br>
        <sub>Multicopter</sub>
      </a>
    </td>
    <td align="center">
      <a href="https://docs.px4.io/main/en/frames_plane/">
        <img src="docs/assets/airframes/types/Plane.svg" width="50" alt="Fixed Wing"><br>
        <sub>Fixed Wing</sub>
      </a>
    </td>
    <td align="center">
      <a href="https://docs.px4.io/main/en/frames_vtol/">
        <img src="docs/assets/airframes/types/VTOLPlane.svg" width="50" alt="VTOL"><br>
        <sub>VTOL</sub>
      </a>
    </td>
    <td align="center">
      <a href="https://docs.px4.io/main/en/frames_rover/">
        <img src="docs/assets/airframes/types/Rover.svg" width="50" alt="Rover"><br>
        <sub>Rover</sub>
      </a>
    </td>
  </tr>
</table>

<sub>…and many more: helicopters, autogyros, airships, submarines, boats, and other experimental platforms. These frames have basic support but are not part of the regular flight-test program. See the <a href="https://docs.px4.io/main/en/airframes/airframe_reference.html">full airframe reference</a>.</sub>

## Try PX4

Run PX4 in simulation with a single command. No build tools, no dependencies beyond Docker:

```bash
docker run --rm -it -p 14550:14550/udp px4io/px4-sitl:latest
```

Open [QGroundControl](https://qgroundcontrol.com) and fly. See [PX4 Simulation Quickstart](https://docs.px4.io/main/en/simulation/px4_simulation_quickstart) for more options.

## Build from Source

```bash
git source https://github.com/PX4/PX4-Autopilot.git --recursive
cd PX4-Autopilot
make px4_sitl
```

> [!NOTE]
> See the [Development Guide](https://docs.px4.io/main/en/development/development.html) for toolchain setup and build options.

## Documentation & Resources

| Resource | Description |
| --- | --- |
| [User Guide](https://docs.px4.io/main/en/) | Build, configure, and fly with PX4 |
| [Developer Guide](https://docs.px4.io/main/en/development/development.html) | Modify the flight stack, add peripherals, port to new hardware |
| [Airframe Reference](https://docs.px4.io/main/en/airframes/airframe_reference.html) | Full list of supported frames |
| [Autopilot Hardware](https://docs.px4.io/main/en/flight_controller/) | Compatible flight controllers |
| [Release Notes](https://docs.px4.io/main/en/releases/) | What's new in each release |
| [Contribution Guide](https://docs.px4.io/main/en/contribute/) | How to contribute to PX4 |

## Community

- **Weekly Dev Call** — open to all developers ([Dronecode calendar](https://www.dronecode.org/calendar/))
- **Discord** — [Join the Dronecode server](https://discord.gg/dronecode)
- **Discussion Forum** — [PX4 Discuss](https://discuss.px4.io/)
- **Maintainers** — see [`MAINTAINERS.md`](MAINTAINERS.md)
- **Contributor Stats** — [LFX Insights](https://insights.lfx.linuxfoun

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / CMake** (manifests: CMakeLists.txt, Makefile; scanned in UPSTREAM_CLONE)
- Top-level source layout: `ROMFS/`, `Tools/`, `boards/`, `cmake/`, `launch/`, `msg/`, `platforms/`, `posix-configs/`, `src/`, `srv/`, `test/`, `test_data/`
- Snapshot size: **14633 files**, **1104882 lines of code** (measured; see Benchmarks)
- Primary languages: `.md` (4332), `.cpp` (1945), `.h` (1257), `.hpp` (963), `.txt` (867), `(none)` (847)
- Upstream commit pinned for this packaging: `b798249a61af32c355d95decd2805a6ab4e9d9f1`

---

## Installation

</p>

<p align="center">
  <a href="https://github.com/PX4/PX4-Autopilot/releases"><img src="https://img.shields.io/github/release/PX4/PX4-Autopilot.svg" alt="Release"></a>
  <a href="https://zenodo.org/badge/latestdoi/22634/PX4/PX4-Autopilot"><img src="https://zenodo.org/badge/22634/PX4/PX4-Autopilot.svg" alt="DOI"></a>
  <a href="https://discord.gg/dronecode"><img src="https://img.shields.io/discord/1022170275984457759?label=discord&logo=discord&logoColor=white&color=5865F2" alt="Discord"></a>
</p>

<p align="center">
  <a href="https://www.bestpractices.dev/projects/6520"><img src="https://www.bestpractices.dev/projects/6520/badge" alt="OpenSSF Best Practices"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/health-score?project=px4" alt="LFX Health Score"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/contributors?project=px4" alt="LFX Contributors"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/active-contributors?project=px4" alt="LFX Active Contributors"></a>
</p>

---

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

```bibtex
@software{px4_autopilot,
  author    = {Meier, Lorenz and {The PX4 Contributors}},
  title     = {{PX4 Autopilot}},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.595432},
  url       = {https://px4.io}
}
```

The DOI above is a Zenodo concept DOI that always resolves to the latest release. For a version-pinned citation, see the [Zenodo record](https://doi.org/10.5281/zenodo.595432) or our [`CITATION.cff`](CITATION.cff).

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/contributors?project=px4" alt="LFX Contributors"></a>
  <a href="https://insights.linuxfoundation.org/project/px4"><img src="https://insights.linuxfoundation.org/api/badge/active-contributors?project=px4" alt="LFX Active Contributors"></a>
</p>

---

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / CMake |
| Manifests detected | CMakeLists.txt, Makefile |
| Files in snapshot | 14633 |
| Lines of code | 1104882 |
| Dependency references | 49 |
| Dependencies by ecosystem | native: 37, npm: 10, pypi: 2 |
| Upstream license | BSD-3-Clause |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| native | Python3 | - | CMakeLists.txt |
| native | Python3 | - | CMakeLists.txt |
| native | Python3 | - | CMakeLists.txt |
| pypi | pymavlink | >=2.4.42 | Tools/bench_test/pyproject.toml |
| pypi | pyserial | - | Tools/bench_test/pyproject.toml |
| native | MAVSDK | - | test/mavsdk_tests/CMakeLists.txt |
| native | Threads | - | test/mavsdk_tests/CMakeLists.txt |
| native | gz-transport | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-sim | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-sensors | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-plugin | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-transport | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-sim | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-sensors | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| native | gz-plugin | - | src/modules/simulation/gz_plugins/CMakeLists.txt |
| ... | (34 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

**Wide hardware support.** PX4 runs on a wide range of [autopilot boards](https://docs.px4.io/main/en/flight_controller/) and supports an extensive set of sensors, telemetry radios, and actuators through the [Pixhawk](https://pixhawk.org/) ecosystem.

**Developer friendly.** First-class support for [MAVLink](https://mavlink.io/) and [DDS / ROS 2](https://docs.px4.io/main/en/ros2/) integration. Comprehensive [SITL simulation](https://docs.px4.io/main/en/simulation/), hardware-in-the-loop testing, and [log analysis](https://docs.px4.io/main/en/log/flight_log_analysis.html) tools. An active developer community on [Discord](https://discord.gg/dronecode) and the [weekly dev call](https://docs.px4.io/main/en/contribute/).

**Vendor neutral governance.** PX4 is hosted under the [Dronecode Foundation](https://www.dronecode.org/), part of the Linux Foundation. Business-friendly BSD-3 license. No single vendor controls the roadmap.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing to PX4-Autopilot

We follow the [GitHub flow](https://guides.github.com/introduction/flow/) development model.

## Fork the project, then source your project

First [fork and source](https://help.github.com/articles/fork-a-project) the project.

## Create a feature branch

Always branch off `main` for new features.

```
git checkout -b mydescriptivebranchname
```

## Edit and build the code

The [developer guide](https://docs.px4.io/main/en/development/development.html) explains how to set up the development environment on Mac OS, Linux or Windows.

### Coding standards

All C/C++ code must follow the [PX4 coding style](https://docs.px4.io/main/en/contribute/code.html). Formatting is enforced by [astyle](http://astyle.sourceforge.net/) in CI (`make check_format`, ``make format`, `make format_changed`). Code quality checks run via [clang-tidy](https://clang.llvm.org/extra/clang-tidy/). Pull requests that fail either check will not be merged.

Python code is checked with [mypy](https://mypy-lang.org/) and [flake8](https://flake8.pycqa.org/).

## Commit message convention

PX4 uses [conventional commits](https://www.conventionalcommits.org/) for all commit messages and PR titles.

### Format

```
type(scope): short description of the change
```

| Part | Rule |
|------|------|
| **type** | Category of change (see types table below) |
| **scope** | The module, driver, board, or area of PX4 affected |
| **`!`** (optional) | Append before `:` to mark a breaking change |
| **description** | What the change does, at least 5 characters, written in imperative form |

### Types

| Type | Description |
|------|-------------|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only changes |
| `style` | Formatting, whitespace, no code change |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `perf` | Performance improvement |
| `test` | Adding or correcting tests |
| `build` | Build system or external dependencies |
| `ci` | CI configuration files and scripts |
| `chore` | Other changes that don't modify src or test files |
| `revert` | Reverts a previous commit |

### Scopes

The scope identifies which part of PX4 is affected. Common scopes:

| Scope | Area |
|-------|------|
| `ekf2` | Extended Kalman Filter (state estimation) |
| `mavlink` | MAVLink messaging protocol |
| `commander` | Commander and mode management |
| `navigator` | Mission, Return, Land, and other navigation modes |
| `sensors` | Sensor drivers

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: BSD-3-Clause** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
BSD 3-Clause License

Copyright (c) 2012 - 2025, PX4 Development Team
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original BSD-3-Clause terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `BSD-3-Clause` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `PX4_AUTOPILOT` (category: SPACE AEROTECH)
- **Upstream URL:** https://github.com/PX4/PX4-Autopilot
- **Pinned commit (SHA):** `b798249a61af32c355d95decd2805a6ab4e9d9f1`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`ea81ec6764f9175667b8465701d6edbafa9a240ee0ff6144a67b7373509d68f9`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

