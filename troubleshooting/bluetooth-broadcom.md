# Broadcom Bluetooth fix — Lenovo G50-45

**Status:** Fixed; controller initializes and pairs reliably with Bluetooth audio devices.

- **Adapter:** Broadcom BCM43142 (`14e4:4365`), Bluetooth USB subsystem `105b:e065`
- **OS / Kernel:** Linux Mint 22.3 Xfce, kernel `7.0.0-43-generic`

## Background & Prior Windows Issue

Before migrating to Linux Mint, Bluetooth on this laptop suffered from persistent issues and frequently failed to work altogether under Windows. Because the Bluetooth transceiver remained non-functional across Windows installations, it initially looked like a potential hardware failure on the combo card.

**Probable cause of the Windows failure:**
- **Lenovo ACPI / Energy Management radio state bug:** On Lenovo G50-series laptops, Lenovo's Windows ACPI power management driver frequently leaves the Bluetooth software radio switch stuck in a disabled or uninitialized state after Windows updates.
- **Broadcom Windows driver/firmware mismatch:** Windows Update routinely replaces Lenovo's OEM Broadcom Bluetooth package with generic drivers that fail to upload the matching `.hcd` firmware patch to the `105b:e065` subsystem over the internal USB bus (`btusb`), leaving the controller powered down or missing in Device Manager.

Confirming the controller initialized cleanly on Linux proved the underlying BCM43142 Bluetooth silicon and antenna were intact.

## Linux Mint Diagnosis & Fix

1. **Symptom:** Bluetooth hardware (`hci0`) appeared unblocked in `rfkill list bluetooth` (`Soft blocked: no`, `Hard blocked: no`), but `dmesg` reported a missing proprietary firmware patch:
   ```text
   Bluetooth: hci0: BCM: firmware Patch file not found, tried:
   Bluetooth: hci0: BCM: 'brcm/BCM43142A0-105b-e065.hcd'
