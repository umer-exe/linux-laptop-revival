# Installation log — November 13, 2026

**Hardware:** Lenovo G50-45 (80E3), AMD A8-6410, Radeon R5, 8 GB RAM, Lexar NS100 256 GB SSD.

## Completed
- Enabled SVM; confirmed UEFI boot.
- Created Mint 22.3 Xfce USB using Rufus on a separate desktop PC.
- Live boot worked; Wi-Fi initially missing.
- First installer attempt crashed after partitioning. USB port is intermittent; terminal had I/O errors.
- Rebooted live USB, verified drives, then successfully installed Mint on the Lexar SSD.
- Booted from SSD successfully; touchpad tap-to-click worked automatically after installation.
- Installed Broadcom STA DKMS offline for BCM43142 (`14e4:4365`). Wi-Fi connected and still works after reboot.

## Next
- System updates (check Broadcom DKMS rebuild with kernel upgrades).
- Snapshots, browsing/office setup, Git, VS Code, Codex and optional Docker.
- Assess real-world performance.
