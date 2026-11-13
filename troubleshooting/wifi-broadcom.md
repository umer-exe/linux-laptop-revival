# Broadcom Wi-Fi fix — Lenovo G50-45

**Status:** Connected successfully; persistence after reboot not yet tested.

- **Adapter:** Broadcom BCM43142 (`14e4:4365`)
- **OS:** Linux Mint 22.3 Xfce; kernel `6.14.0-37-generic`
- **Problem:** Wi-Fi networks missing after installation.
- **Fix:** Downloaded `broadcom-sta-dkms_6.30.223.271-23ubuntu1.3_all.deb` on another PC and transferred it by USB.

Installed with:

```bash
sudo apt install ./broadcom-sta-dkms_*.deb
sudo modprobe wl
```

**Gotcha:** `wl` ends in lowercase letter **L**, not number **1**. Using `w1` caused “module not found”.

Wi-Fi then connected successfully. **Next:** Restart and confirm the driver loads automatically.
