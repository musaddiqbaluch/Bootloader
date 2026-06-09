# 🔒 Bootloader

A lightweight Android utility that inspects your device's bootloader status using low-level system properties — no root, no ADB, fully offline.

<img src="https://raw.githubusercontent.com/musaddiqbaluch/Bootloader/main/ic_launcher.png" width="80"/>

---

## 📸 Screenshots

<p>
<img src="https://raw.githubusercontent.com/musaddiqbaluch/Bootloader/main/Bootloader-screenshot1.png" width="200"/>
<img src="https://raw.githubusercontent.com/musaddiqbaluch/Bootloader/main/Bootloader-screenshot2.png" width="200"/>
<img src="https://raw.githubusercontent.com/musaddiqbaluch/Bootloader/main/Bootloader-screenshot3.png" width="200"/>
</p>

---

## 🔍 What It Checks

| Property | Description |
|---|---|
| `ro.boot.verifiedbootstate` | The most reliable signal — set directly by the bootloader at boot |
| `ro.boot.flash.locked` | Raw lock flag: `1` = locked, `0` = unlocked |
| `ro.oem_unlock_supported` | Whether the device supports OEM unlocking at all |
| `ro.secureboot.lockstate` | Secure boot state reported by some OEMs |

---

## 📊 Status Values

- 🔒 **LOCKED** — Bootloader is locked, verified boot chain is intact
- 🔓 **UNLOCKED** — Bootloader has been unlocked
- ❓ **UNCERTAIN** — Device OEM does not expose standard bootloader properties
- ⚠️ **ERROR** — System properties could not be read

---

## ⚙️ How It Works

Bootloader reads Android system properties via reflection using `android.os.SystemProperties`. No special permissions, no root access, and no network connection required. Results are displayed instantly on launch.

---

## 📱 Compatibility

- Android 9 (API 29) and above
- Works on most Android OEMs following AOSP standards
- Results may vary on Samsung (Knox) and some Xiaomi (HyperOS) devices

---

## 🎨 Credits

App icon made by [Freepik](https://www.freepik.com) from [Flaticon](https://www.flaticon.com).

---

## 📄 License

Proprietary. All rights reserved © 2026 musaddiqbaluch.

---

## 🏷️ Version

`v1.0.0`
