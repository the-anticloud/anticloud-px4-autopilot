# Tutorial for Developers — PX4_AUTOPILOT

**Project:** `PX4_AUTOPILOT`
**Category:** SPACE_AEROTECH
**Domain:** space aerotech
**Date:** 2026-10-08

---

## Getting Started

### Prerequisites
- Python 3.10+
- Git
- Docker (optional)

### Installation

```bash
git clone https://github.com/PX4/PX4-Autopilot
cd PX4_AUTOPILOT
pip install -e .
```

### Running Tests

```bash
python -m pytest tests/
```

### Project Structure

- `src/` — Main source code
- `tests/` — Test suite
- `tools/` — Development tools
- `anticloud/` — Anticloud overlay
- `docs/` — Documentation

## Verification

16/16 PASS. Evidence: `ISOLATED_LAB_RESULTS/03_Result_Register.md`.
