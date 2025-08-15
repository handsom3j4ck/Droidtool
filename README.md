# Droidtool

**Droidtool** is a powerful, menu-driven Bash script for managing Android devices from a Linux system using ADB (Android Debug Bridge) and Fastboot. It simplifies device diagnostics, app management, file operations, backups, and system-level tweaks — all from the terminal.

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

#### 📁 File Management

- Pull/push files and folders
- Delete files/folders from device
- Search for files or folders on device
- Supports `/storage/emulated/0/

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

- Check for device updates

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

### 2. Make Script Executable

```bash
chmod +x droidtool
```

### 3. Run the Script

```bash
./droidtool
```

> 💡 The script will auto-install `android-tools-adb` if missing (Debian/Ubuntu/Arch only).

---

## 🎯 Usage

### Droidtool

1. Launch `./droidtool`
2. Select connection method (USB, IP, or Wireless Pair)
3. Navigate the menu to perform tasks
4. Exit cleanly (option 9) to stop ADB server

---

## 🙌 Acknowledgments

- Android Open Source Project (AOSP)
- ADB and Fastboot developers
- Open-source community for tool inspiration

---
