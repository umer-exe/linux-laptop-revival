# Radeon R5 GPU Ring Hang (`rcs0` Freeze)

## Symptom
Desktop UI and open windows stop responding to clicks or keyboard input (`Ctrl + Alt + F1` unresponsive) while the mouse cursor continues moving smoothly.

## Cause
On kernel `7.0.0-43-generic`, AMD dynamic power management and GPU-accelerated browser or compositor calls trigger a semaphore deadlock on the Radeon R5 render command streamer (`rcs0`), blocking `Xorg`.

## Fix

1. **Disable GPU dynamic power management in GRUB:**
   Edit `/etc/default/grub` and append `amdgpu.runpm=0 radeon.dpm=0` to `GRUB_CMDLINE_LINUX_DEFAULT`:
   ```text
   GRUB_CMDLINE_LINUX_DEFAULT="quiet splash amdgpu.runpm=0 radeon.dpm=0"
   ```
   Apply and reboot:
   ```bash
   sudo update-grub
   ```

2. **Disable Xfce display compositing:**
   ```bash
   xfconf-query -c xfwm4 -p /general/use_compositing -s false
   ```

3. **Disable browser hardware acceleration:**
   Turn off hardware/graphics acceleration in browser performance/system settings.

## Verification
```bash
cat /proc/cmdline && xfconf-query -c xfwm4 -p /general/use_compositing
```
Confirm `amdgpu.runpm=0 radeon.dpm=0` is present in `/proc/cmdline` and compositing returns `false`.
