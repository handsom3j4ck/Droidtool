# Droidtool & FRP Bypass Tool

**Droidtool** is a powerful, menu-driven Bash script for managing Android devices from a Linux system using ADB (Android Debug Bridge) and Fastboot. It simplifies device diagnostics, app management, file operations, backups, and system-level tweaks — all from the terminal.

Alongside it, the **FRP Bypass Tool (`frp-menu`)** is a separate script designed to assist in bypassing Factory Reset Protection (FRP) on locked Android devices during setup, using known exploits and ADB-based methods.

> 🔒 **Both tools are strictly for ethical, authorized use only. Unauthorized access to devices you do not own or have explicit permission to test is illegal.**

---

## ⚠️ Legal and Ethical Warning

These tools are intended **only** for:
- Authorized device recovery
- Penetration testing (with **written consent**)
- Educational demonstrations
- Forensic analysis in legal environments
- Android development and debugging

**Unauthorized use** to bypass security on devices you do not own or control may violate:
- **Computer Fraud and Abuse Act (CFAA)**
- **Local telecommunications and privacy laws**
- **Device manufacturer terms of service**

> 🛑 **The author and contributors are not responsible for any misuse, legal consequences, or damage resulting from unauthorized use.**

### ✅ Always:
- Obtain **explicit, written authorization** before testing.
- Use in **controlled, isolated environments**.
- Comply with **local laws and regulations**.
- Respect **privacy and data ownership**.

---

## 📦 Tools Overview

| Tool | Purpose | Access Level Required |
|------|--------|------------------------|
| **Droidtool** | Full Android device management via ADB | ADB access (root optional) |
| **FRP Bypass Tool (`frp-menu`)** | Bypass Factory Reset Protection during setup | ADB access (varies by method) |

> 🔗 Both tools are **separate scripts** but share the same dependency: `android-tools-adb`.

---

## 🛠️ Droidtool – Linux Android Management Tool

### ✅ Features

#### 🔌 Device Connection & Info
- Connect via **USB**, **IP**, or **ADB Wireless Pair (Android 11+)**
- Auto-install `android-tools` on Debian/Ubuntu and Arch
- Show full device report: brand, model, Android version, serial, battery, storage, network, hardware
- Check root access and uptime
- Show foreground app and network details

#### 📦 App Management
- Install single or multiple APKs
- Uninstall or batch-uninstall apps
- Enable/disable apps (including bloatware)
- Extract APKs from device
- Push APKs as system apps (requires root)
- Clear cache for all apps (root)

#### 💾 Backup & Restore
- ADB backup: full or per-app (`.ab` format)
- Root backup: tar `/data`, `/system`, `/cache` or app data (`.tar.gz`)
- Restore from `.ab`, `.ab.gz`, or `.tar.gz` (root)
- List available backups

#### 📁 File Management
- Pull/push files and folders
- Delete files/folders from device
- Search for files or folders on device
- Supports `/storage/emulated/0` (recommended over `/sdcard`)

#### 🔁 Reboot & Recovery
- Reboot to system, recovery, bootloader, or fastboot
- Sideload ZIP files in recovery mode

#### 🧪 Developer Tools
- View and save `logcat` output
- Open ADB shell
- Take screenshots
- Toggle dark mode (Android 10+)
- Change system language (root)

#### 📺 Custom Settings (Android TV/Google TV)
- Apply performance improvements
- Optimize app performance
- Close background apps
- Clear app data/cache
- Remove ads via private DNS (AdGuard, ControlD)

#### 🧰 Utilities
- Safe path validation
- Input sanitization
- Error handling and retry logic
- Graceful cleanup on exit

---

## 🔓 FRP Bypass Tool (`frp-menu`) – Standalone Script

A separate Bash script to assist in bypassing **Factory Reset Protection (FRP)** on locked Android devices during initial setup.

> ⚠️ This script is **not included in Droidtool** and must be run independently.

### ✅ Supported Methods (by Android Version)

| Method | Android Version | Notes |
|-------|------------------|-------|
| **Dial Menu Exploit** | 5.x–9.x | Uses `*#*#4636#*#*` to access settings |
| **Talkback Exploit** | 10–12 | Enables accessibility to open browser/settings |
| **YouTube/Maps Exploit** | 13–14 | Opens browser via YouTube/Maps to access settings |
| **SIM Card Exploit** | 8–10 | Uses SIM lock screen to trigger Google unlock |
| **Emergency Call Glitch** | 12–14 | Uses emergency dialer to access test menu |
| **Accessibility Menu Exploit** | 12–14 | Enables accessibility to open browser |
| **Quick Shortcut Maker** | 7–11 | Launches hidden activities via shortcut app |
| **Alliance Shield X** | Samsung 11–14 | Disables GMS services on Samsung devices |
| **Motorola Accessibility Bypass** | Android 14 (Moto) | Uses Moto-specific workflow |
| **Direct ADB Bypass** | 10–13 (some 14) | Sets `user_setup_complete=1` via ADB |
| **APK Bypass** | All versions | Requires sideloading bypass APK (e.g., Easy Flashing) |

> 📌 **Note**: Success depends on device model, Android version, and OEM restrictions.

---

## 📦 Requirements

### Hardware
- Linux system (tested on Debian, Ubuntu, Arch)
- Android device with USB debugging enabled (for ADB)
- USB cable or network access (for IP/Wi-Fi ADB)

### Software
- `android-tools-adb` (required)
- `android-tools-fastboot` (optional, for reboot menu)
- Root access (for root-restricted features)

### Permissions
- `sudo` access for:
  - Installing dependencies
  - Running ADB as root
  - Accessing system partitions

---

## 🛠️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/handsom3j4ck/Droidtool.git
cd Droidtool
```

### 2. Make Scripts Executable
```bash
chmod +x droidtool
chmod +x frp-menu  # if available
```

### 3. Run the Scripts

#### For Droidtool:
```bash
./droidtool
```

#### For FRP Bypass Tool:
```bash
./frp-menu
```

> 💡 The scripts will auto-install `android-tools-adb` if missing (Debian/Ubuntu/Arch only).

---

## 🎯 Usage

### Droidtool
1. Launch `./droidtool`
2. Select connection method (USB, IP, or Wireless Pair)
3. Navigate the menu to perform tasks
4. Exit cleanly (option 9) to stop ADB server

### FRP Bypass Tool
1. Launch `./frp-menu`
2. Connect via USB (ADB must be enabled or exploitable)
3. Run **Device Compatibility Check** to see recommended methods
4. Follow on-screen instructions for the chosen exploit
5. Reboot and verify FRP is bypassed

> 📝 **Tip**: Some methods require manual interaction on the device. ADB assists where possible.

---

## 🛑 Troubleshooting

| Issue | Solution |
|------|----------|
| `adb: command not found` | Run script with `sudo` or install `android-tools-adb` manually |
| `unauthorized` device | Accept ADB prompt on the device |
| No device found | Ensure USB debugging is on; try `adb kill-server && adb start-server` |
| FRP bypass fails | Try a different method; some devices block ADB during setup |
| Root commands fail | Device may not be rooted or `su` not installed |
| File paths with spaces | Avoid spaces in paths; use underscores or hyphens |
| `logcat` hangs | Use `Ctrl+C` to interrupt; use `logcat -d` for dump-only mode |

---

## 🙌 Acknowledgments

- Android Open Source Project (AOSP)
- ADB and Fastboot developers
- Security researchers who discovered FRP bypass methods
- Open-source community for tool inspiration

---

## 📬 Contact

For issues, suggestions, or responsible disclosure, please open a GitHub Issue.

> 🔐 **Do not use these tools for malicious purposes. Respect privacy, legality, and ethics.**

---

## 🏁 Disclaimer

**Always act responsibly.**
