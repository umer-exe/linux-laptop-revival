# Broadcom Bluetooth fix — Lenovo G50-45

**Status:** Fixed; controller initializes and pairs with Bluetooth audio devices.

- **Adapter:** Broadcom BCM43142 (`14e4:4365`), Bluetooth subsystem `105b:e065`
- **OS / Kernel:** Linux Mint 22.3 Xfce, kernel `7.0.0-43-generic`

## Background

Bluetooth previously failed to work on Windows due to common Lenovo G50-series ACPI radio-state bugs and Windows Update replacing OEM Broadcom firmware patches. On Mint, `rfkill` showed Bluetooth unblocked, but `dmesg` reported a missing patch file (`brcm/BCM43142A0-105b-e065.hcd`), proving the hardware was intact.

## Fix

1. **Download the firmware patch** into `/lib/firmware/brcm/`:
   ```bash
   sudo mkdir -p /lib/firmware/brcm
   sudo wget -O /lib/firmware/brcm/BCM43142A0-105b-e065.hcd https://raw.githubusercontent.com/winterheart/broadcom-bt-firmware/master/brcm/BCM43142A0-105b-e065.hcd
   ```
2. **Reload the Bluetooth USB driver:**
   ```bash
   sudo modprobe -r btusb && sudo modprobe btusb
   ```
3. **Verify initialization and scanning:**
   ```bash
   bluetoothctl show
   bluetoothctl --timeout 10 scan on
   ```
   Confirmed `Powered: yes` (`Manufacturer: 0x000f`), and wireless earbuds paired and played audio normally.
