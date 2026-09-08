use this : https://sourceforge.net/projects/recovery-for-xiaomi-devices/files/rothko/

⚠️ WARNING: This TWRP was compiled blindly. Functionality is not guaranteed, and flashing it carries a high risk of bricking.

# TWRP Builder for Xiaomi 14T Pro (rothko)

Use GitHub Actions to automatically compile TWRP Recovery for the Xiaomi 14T Pro (codename: **rothko**).

## Device Specifications

| Item | Details |
|------|---------|
| **Device** | Xiaomi 14T Pro |
| **Codename** | rothko |
| **Chipset** | Mediatek Dimensity 9300+ (mt6989) |
| **Architecture** | arm64 |
| **Android Version** | 14 (shipped) |
| **Recovery Location** | vendor_boot partition |
| **A/B Partition** | Yes (Virtual A/B) |

## Build Parameters

| Parameter | Value |
|-----------|-------|
| **TWRP Manifest** | twrp-14.1 (default) |
| **Device Tree** | [JonesqPacMan/android_device_xiaomi_rothko_twrp](https://github.com/JonesqPacMan/android_device_xiaomi_rothko_twrp) |
| **Device Tree Branch** | twrp-14.1_a16 |
| **Build Target** | vendor_boot |

## How to Build

1. Fork this repository
2. Go to **Actions** tab
3. Click **Build TWRP for Xiaomi 14T Pro (rothko)**
4. Click **Run workflow**
5. Select the manifest branch (default: `14.1`)
6. Select build target (default: `vendor_boot`)
7. Click **Run workflow** to start the build
8. Wait for the build to complete (~1-2 hours)
9. Download the built image from **Releases**

## Flash Instructions

```bash
# Reboot to bootloader
adb reboot bootloader

# Flash TWRP vendor_boot image
fastboot flash vendor_boot vendor_boot.img

# Reboot to recovery
fastboot reboot recovery
```

## Credits

- [TWRP](https://twrp.me/) - Team Win Recovery Project
- [JonesqPacMan](https://github.com/JonesqPacMan) - Device tree maintainer
- [minimal-manifest-twrp](https://github.com/minimal-manifest-twrp) - Minimal TWRP manifest
