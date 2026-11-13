# Installation log

## November 13, 2026 — Preparing the migration

### Goals
- Replace a sluggish Windows installation with a more responsive desktop.
- Prioritize web browsing, documents and lightweight development.
- Keep heavy builds and other demanding tasks on the main desktop PC.

### Completed
1. Recorded Lenovo G50 (80E3) hardware: AMD A8-6410, Radeon R5, 8 GB RAM, Lexar NS100 256 GB SSD.
2. Enabled SVM in firmware (Windows recheck not recorded).
3. Confirmed firmware boot mode was UEFI.
4. Downloaded the Linux Mint 22.3 Xfce ISO and Rufus using the main desktop.
5. Created a bootable USB with Rufus; booted from USB into the normal Mint live session.
6. Reached the Linux Mint Xfce desktop.

### Blocker: Wi-Fi
- No wireless networks appeared in the live session.
- Windows had identified the adapter generically as “Broadcom 802.11n Network Adapter.”
- Exact PCI chipset ID and loaded Linux driver have **not** been collected.
- Driver installation **not attempted**.

### Not yet verified
Audio, brightness keys, touchpad, suspend/resume and graphics stability have not been recorded as passing.

### Next steps
Run Wi-Fi identification and radio-blocking diagnostics. Confirm other hardware works before starting the installer. The internal SSD has **not** been erased yet.
