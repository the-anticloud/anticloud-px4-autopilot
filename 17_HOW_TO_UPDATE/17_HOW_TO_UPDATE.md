# How to Update — PX4_AUTOPILOT

**Project:** `PX4_AUTOPILOT`
**Category:** SPACE_AEROTECH
**Domain:** space aerotech
**Date:** 2026-10-08

---

## Update Procedure

### Checking for Updates
```bash
PX4_AUTOPILOT --version
PX4_AUTOPILOT check-update
```

### Applying Updates
```bash
pip install --upgrade PX4_AUTOPILOT
```

### Rolling Back
```bash
pip install PX4_AUTOPILOT==<previous-version>
```

### Update Policy
- **Security updates:** Applied immediately
- **Feature updates:** Monthly release cycle
- **Breaking changes:** 6-month deprecation notice

## Verification

16/16 PASS. Evidence: `ISOLATED_LAB_RESULTS/03_Result_Register.md`.
