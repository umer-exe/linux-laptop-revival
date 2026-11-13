# Linux Laptop Revival 🐧

Reviving a **Lenovo G50-45 (80E3)** with Linux Mint 22.3 Xfce for responsive browsing, writing, and occasional lightweight coding.

**Current status:** Mint installed on the internal SSD, booting normally; Broadcom Wi-Fi fixed and working after reboot; first Timeshift snapshot created. **208 updates available, not yet installed.** Further setup paused for now.

## Hardware

| Component | Details |
| --- | --- |
| CPU / graphics | AMD A8-6410 APU / Radeon R5 |
| RAM | 8 GB (no further upgrade planned) |
| SSD | Lexar NS100 256 GB |
| Wi-Fi | Broadcom BCM43142 (`14e4:4365`) |
| Ethernet | Realtek PCIe GBE |
| Boot | UEFI; SVM enabled |

## Progress

- [x] Create installation USB; boot Mint live session
- [x] Install Linux Mint 22.3 Xfce to SSD
- [x] Boot successfully from SSD
- [x] Verify sound, keyboard, display, brightness and touchpad
- [x] Confirm tap-to-click works after installation
- [x] Install Broadcom STA driver offline; verify Wi-Fi persists after reboot
- [x] Create first Timeshift snapshot
- [ ] Apply 208 available updates and verify Wi-Fi afterward
- [ ] Set up preferred browser and writing applications
- [ ] Configure Git, VS Code, Codex CLI, optional Docker Engine
- [ ] Test suspend/resume and evaluate performance

## Notes

First installation attempt crashed, possibly due to an unreliable laptop USB port; a subsequent attempt completed successfully. No storage hardware failure was established.

The laptop is intended for browsing, typing and modest development; heavy workloads run on a separate desktop.

## Documentation

- [Hardware](hardware/specifications.md)
- [Installation log](logs/installation-log.md)
- [Broadcom Wi-Fi fix](troubleshooting/wifi-broadcom.md)
- [Development setup plan](setup/development-environment.md)

Avoid sharing credentials, tokens, sensitive logs or other private identifiers.
