# Droidtool

**Droidtool** is a powerful, menu-driven Bash script for managing Android devices from a Linux system using ADB (Android Debug Bridge) and Fastboot. It simplifies device diagnostics, app management, file operations, backups, and system-level tweaks — all from the terminal.

---

## 🛠️ Droidtool – Linux Android Management Tool

### ✅ Features

#### 🔌 Connection Options

- Connect via **USB**, **IP**, or **ADB Wireless Pair (Android 11+)**

#### 🔌 Device Info

- Comprehensive device report including brand, model, Android version, SDK, serial, build ID, security patch, kernel, mac, rooted status, uptime, battery (level, status, health, temp), storage usage, memory info, screen resolution, network (IP, Wi-Fi SSID, signal), hardware (CPU, GPU)

#### 📦 App Management

- Install single or multiple APKs
- Uninstall or batch-uninstall apps
- Enable/disable apps
- Extract APKs from device
- Disable bloatware

#### 📁 File Management

- Pull/push files and folders
- Delete files/folders from device
- Search for files or folders on device

#### 📺 Custom Settings (Android TV/Google TV)

- Apply general-purpose performance improvements
- Enable processing speed management system
- Optimize application performance
- Close apps in the background
- AIO cache clean
- Delete data and cache from apps (per app)
- Check for TV device updates
- Remove ads via private DNS (AdGuard, ControlD, Quad9, NextDNS)

#### 🧪 Developer Tools

- View and save `logcat` output
- Open ADB shell
- Take screenshots
- Toggle dark mode (Android 10+)
- Custom ADB command

---

## 📦 Requirements

### Hardware

- Linux system (tested on Arch)
- Android device with USB debugging enabled
- USB cable or network access

### Software

- android-tools (required)

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

### 2. Make Script Executable

```bash
chmod +x droidtool
```

### 3. Run the Script

```bash
./droidtool
```

> 💡 The script will auto-install `android-tools` if missing (Debian/Ubuntu/Arch/Fedora/RedHat).

---

## 🙌 Acknowledgments

- Android Open Source Project (AOSP)
- ADB and Fastboot developers
- Open-source community for tool inspiration

---
