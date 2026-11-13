# Linux Laptop Revival 💻

Reviving an aging Lenovo G50 (machine type **80E3**) as a responsive Linux laptop for browsing, writing, lightweight coding, and occasional container-based development.

> **Current stage:** Linux Mint 22.3 Xfce boots from USB. Wi-Fi networks are not appearing in the live session; chipset/driver diagnosis is next. **Linux has not yet been installed to the SSD.**

## Why this project?

Windows felt sluggish despite an SSD and RAM upgrade. The goal is a simple, reliable, lightweight system—not a benchmark machine. Heavy development stays on a separate desktop PC.

## Hardware

| Component | Details |
| --- | --- |
| Laptop | Lenovo G50 family, machine type 80E3 |
| CPU | AMD A8-6410 APU |
| Graphics | Integrated AMD Radeon R5 |
| RAM | 8 GB (no further upgrade planned) |
| SSD | Lexar NS100, 256 GB |
| Wi-Fi | Broadcom 802.11n adapter (exact chipset **not yet confirmed**) |
| Ethernet | Realtek PCIe GBE Family Controller |
| Boot firmware | UEFI |
| Virtualization | SVM enabled in firmware |

## Intended software

- **OS:** Linux Mint 22.3 Xfce (64-bit)
- **Browsing:** Firefox, optionally Chrome for compatibility / profile-based workflows
- **Writing:** LibreOffice, with Microsoft 365 web apps as a fallback
- **Development:** VS Code, Git, Codex CLI
- **Containers:** Docker Engine + Compose, used selectively

## Progress

- [x] Gather laptop hardware specifications
- [x] Enable SVM in firmware
- [x] Download Mint Xfce ISO and Rufus on desktop PC
- [x] Prepare bootable USB
- [x] Boot Linux Mint live session in UEFI mode
- [ ] Identify and fix Broadcom Wi-Fi problem
- [ ] Verify sound, touchpad, brightness, suspend, and graphics
- [ ] Install Mint to internal SSD (clean install)
- [ ] Install updates and recommended drivers
- [ ] Configure browser, editor, Git, Codex CLI, and Docker
- [ ] Measure responsiveness and tune only if necessary

## Documentation

- [Hardware inventory](hardware/specifications.md)
- [Installation log](logs/installation-log.md)
- [Broadcom Wi-Fi troubleshooting](troubleshooting/wifi-broadcom.md)
- [Development environment plan](setup/development-environment.md)

## Scope and cautions

This documents one specific machine. Driver commands should be chosen **after identifying the hardware PCI ID**. Don't blindly install proprietary Broadcom drivers. A clean installation will erase the laptop's existing Windows files; confirm the target disk before doing so.

Avoid committing passwords, tokens, personal documents, MAC addresses, or raw logs that include identifying information.
