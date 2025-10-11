## Droidtool – Android Toolkit for Linux

### Features

#### Connection Options

- Connect via **USB**, **IP**, or **ADB Wireless Pair (Android 11+)**

####  Device Info

- Detailed device report including brand, model, Android version, SDK, serial number, build ID, security patch level, kernel version, rooted status, system uptime, battery status (level, health, temperature), storage usage, memory info, architecture, screen resolution, network details, and hardware specs (CPU, GPU)

####  App Management

- Install or uninstall applications
- Enable or disable applications
- Clear app data and cache
- Clear only cache

####  File Management

- Transfer files and folders (upload/download)
- Remove files and folders from the device
- Search for files and folders on the device

####  Custom Settings

- TV Tweaks: Optimize system performance and speed on Android TV devices, including TV sticks and boxes.
- Set Private DNS: Configure DNS options such as AdGuard, ControlD, Quad9, Cloudflare, or a custom DNS.
- Check for Device Updates: Verify if software updates are available for the device.

####  Developer Tools

- View, Save, and Clear logcat Output: Access, store, and clear logcat logs for system debugging.
- Open ADB Shell: Launch the ADB shell for direct interaction with the device.
- Custom ADB Command: Execute custom ADB commands for advanced device control.
- Take Screenshots: Capture screenshots of the device screen.

---

##  Requirements

### Hardware

- Linux system
- Android device with USB debugging enabled
- USB cable or network access

### Software

- android-tools or adb and fastboot (required)

### Permissions

- `sudo` access for:
  - Installing dependencies

---

##  Installation

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

>  The script will auto-install `android-tools` if missing (Arch/Debian).

---

## Android Device Setup

### Enabling Developer Options and USB Debugging
1. Open the **Settings** app on your Android device.
2. Scroll down and select **About phone** (or **About device** on some devices).
3. Find the **Build number** entry and tap it **7 times** in quick succession.
4. You will see a toast message: "You are now a developer!" (or similar).
5. Go back to the main Settings menu; **Developer options** should now appear (usually under **System**).
6. Open **Developer options**.
7. Scroll to the **Debugging** section.
8. Toggle **USB debugging** to **On**.
9. When you first connect your device to your computer via adb, a prompt will appear on the device screen. Check "Always allow from this computer" and tap **OK** to authorize.

### ADB Wireless Pairing (Android 11+)
1. In **Developer options**, toggle **Wireless debugging** to **On**.
2. Tap **Wireless debugging** > **Pair device with pairing code**.
3. Your device will display a pairing code, IP address, and port (e.g., `192.168.1.100:37521`).
4. In Droidtool's connection menu, select option 3 and enter the IP:port and code as prompted.

**Notes:**
- Revoke USB debugging authorizations in Developer options if switching computers.

---

##  Acknowledgments

- Android Open Source Project (AOSP)
- ADB and Fastboot developers
- Open-source community for tool inspiration

---
