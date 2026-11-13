# Linux Laptop Revival 🐧

Reviving a **Lenovo G50-45 (80E3)** with **Linux Mint 22.3 Xfce** for browsing, writing, and lightweight coding.

**Current status:** Mint boots from the SSD; Wi-Fi works after reboot; system updates, drivers, multimedia codecs, Timeshift and firewall setup are done. Firefox is configured. No additional apps installed from Software Manager yet.

## Hardware

| Component | Details |
| --- | --- |
| CPU / graphics | AMD A8-6410 APU / Radeon R5 |
| RAM | 8 GB nominal (~6.7 GiB usable in Mint) |
| SSD | Lexar NS100 256 GB |
| Wi-Fi | Broadcom BCM43142 (`14e4:4365`) |
| Ethernet | Realtek PCIe GBE |
| Boot | UEFI; SVM enabled |

## Progress

- [x] Install Linux Mint 22.3 Xfce on SSD and boot without USB
- [x] Check sound, keyboard, display, brightness and touchpad tap-to-click
- [x] Install Broadcom STA Wi-Fi driver; verify reconnection after reboot
- [x] Install ~208 system updates; verify kernel `7.0.0-43-generic`
- [x] Create Timeshift snapshot
- [x] Check Driver Manager; Broadcom alternative driver selected
- [x] Install multimedia codecs
- [x] Configure Firefox Sync (phone, desktop, laptop), uBlock Origin and Multi-Account Containers
- [x] Review Xfce autostart applications; disable selected optional entries
- [x] Enable firewall (GUFW)
- [x] Check memory and uptime: ~1.2 GiB used, ~5.5 GiB available at measurement
- [x] Explore Software Manager (no new apps installed yet)
- [ ] Review Power Manager settings and test suspend/resume
- [ ] Install and configure Git and VS Code
- [ ] Consider LibreOffice and optional Docker Engine later

## Notes

The first installer attempt crashed. USB connectivity and SSD detection were intermittently unreliable during setup; the exact cause was not established. The system now boots normally.

WhatsApp and Discord can be used in Firefox; no separate messaging applications have been installed. **Codex CLI is not planned for this laptop.**

## Documentation

- [Hardware](hardware/specifications.md)
- [Installation log](logs/installation-log.md)
- [Broadcom Wi-Fi fix](troubleshooting/wifi-broadcom.md)
- [Development setup plan](setup/development-environment.md)

Avoid committing credentials, tokens, sensitive logs or other private identifiers.
