# Broadcom Wi-Fi fix — Lenovo G50-45

**Status:** Fixed; reconnects automatically after reboot.

- Adapter: Broadcom BCM43142 (`14e4:4365`)
- Mint 22.3 Xfce, kernel `6.14.0-37-generic`
- Downloaded `broadcom-sta-dkms_6.30.223.271-23ubuntu1.3_all.deb` on desktop PC; transferred via USB.
- Installed with `sudo apt install ./broadcom-sta-dkms_*.deb`
- Loaded using `sudo modprobe wl` (lowercase **L**, not number **1**).
- Wi-Fi connected and continued working after reboot.
