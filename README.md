```markdown
# Realme C1 Rooting Guide Without Pc

## Prerequisites

- Unlocked Bootloader
- Realme C1 Device
- TWRP Recovery Image
- vbmeta Image
- Magisk ZIP File
- LineageOS ROM (Optional)
- GApps ZIP (if you want Google apps)

## Step-by-Step Process

0. **Backup Your Data:**
   - Backup your important data and create a backup.

1. **Boot into Fastboot Mode:**
   - Power off your phone. Press and hold **Volume Down + Power** to boot into fastboot mode.

2. **Install TWRP Recovery:**
   - Connect your phone to your Bugjagear app. Open a command prompt or terminal and navigate to the directory containing the TWRP image. Flash TWRP with:

   ```bash
   fastboot flash recovery twrp.img
   ```
3. **Flash vbmeta Image:**
   ```bash
   fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
   ```
4. **Boot into TWRP Recovery:**
   - Use the command:

   ```bash
   fastboot reboot recovery
   ```
6. **Wipe Current System:**
   - In TWRP, go to Wipe > Advanced Wipe and select Dalvik/ART Cache, Cache, System, and Data. Do not wipe internal storage.

7. **Flash LineageOS ROM (If You need):**
   - In TWRP, go to Install and select the LineageOS ROM ZIP file. Swipe to confirm the flash.

8. **Flash GApps (if needed):**
   - Go to Install in TWRP and select the GApps ZIP file. Swipe to confirm the flash.

9. **Flash Magisk:**
   - In TWRP, go to Install and select the Magisk ZIP file. Swipe to confirm the flash.

10. **Reboot Your Device:**
    - Go back to the main TWRP screen and select Reboot > System. The first boot might take longer, so be patient.

11. **Additional Setup:**
    - After device opened do all setting, turn on internet and open magisk app (if not installed, install manually. Then allow all permissions and it will reboot your phone.
  ## All done, your phone now rooted
  
## Potential Errors and Solutions

- **Bootloop or Device Stuck in Fastboot Mode:**
  - Reflash the TWRP, vbmeta, and LineageOS following the steps above. Ensure that you flash the correct files for your device.

- **No OS Installed Error:**
  - Reflash LineageOS and make sure it’s the correct version for your device. Check that you’ve wiped the old system and data partitions properly.

- **TWRP Not Booting Properly:**
  - Reinstall TWRP using fastboot and ensure you’ve flashed it correctly.

- **Magisk Not Working:**
  - Reflash Magisk and ensure the Magisk Manager app is correctly installed. Check for the latest version of Magisk.

- **Google Apps Not Functioning:**
  - Reflash GApps and ensure you’re using the correct version compatible with your LineageOS.
```
