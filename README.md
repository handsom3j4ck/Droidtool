## 🛠️ Droidtool – Android Toolkit for Linux Systems

### ✅ Features

#### 🔌 Connection Options

- Connect via **USB**, **IP**, or **ADB Wireless Pair (Android 11+)**

#### 🔌 Device Info

- Comprehensive device report including brand, model, Android version, SDK, serial, build ID, security patch, kernel, mac, rooted status, uptime, battery (level, status, health, temp), storage usage, memory info, arch, screen resolution, network, hardware (CPU, GPU)

#### 📦 App Management

- Install single or multiple apps
- Uninstall single or multiple apps
- Enable/disable apps
- Close apps in the background
- Delete data and cache from apps

#### 📁 File Management

- Pull/push files and folders
- Delete files/folders from device
- Search for files or folders on device

#### 👽 Custom Settings

- TV Tweaks (This could damage your device. Use at your own risk)
- Debloat TV (This could damage your device. Use at your own risk)
- Disable TV Launcher (This could damage your device. Use at your own risk)
- Set private DNS (AdGuard, ControlD, Quad9, NextDNS, Cloudflare)
- Check for updates

#### 🧪 Developer Tools

- View and save and clear `logcat` output
- Open ADB shell
- Custom ADB command
- Take screenshots

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
