# Droidtool - Linux Android Management Tool

**Droidtool** is a Bash script designed to simplify the management of Android devices from a Linux system using ADB (Android Debug Bridge) and Fastboot. It provides a user-friendly, menu-driven interface for performing a wide range of tasks, from app management to system tweaks, backups, and developer tools.

## Features

- **Device Connection & Info**:
  - Connect via USB or IP
  - Display device info (model, Android version, serial number)
  - Check battery health, storage usage, CPU/memory usage (root required), and uptime
  - Verify root access and device status (root required)

- **App Management**:
  - Install single or multiple APKs
  - Uninstall or batch-uninstall apps
  - Enable/disable apps
  - Clear cache for all apps (root required)
  - Extract APKs from the device
  - Push APKs as system apps (root required)

- **Backup & Restore**:
  - Backup all apps and data or specific app data
  - Restore from backup files
  - List available backups

- **File Management**:
  - Pull files from the device
  - Push files to the device

- **Reboot & Recovery**:
  - Reboot to system, recovery, bootloader, or fastboot mode
  - Sideload ZIP files in recovery mode

- **Developer Tools**:
  - View and save logcat output
  - Access device shell
  - Take screenshots
  - Change device language (root required)

- **Custom Settings for Android TV/Google TV**:
  - Apply performance improvements
  - Enable processing speed management
  - Clear cache memory (root required)
  - Optimize app performance
  - Close background apps
  - Clear app data and cache
  - Check for system updates
  - Configure private DNS to remove ads

## Requirements

- **Operating System**: Linux (tested on Debian/Ubuntu and Arch Linux)
- **Dependencies**:
  - `android-tools-adb`
  - `android-tools-fastboot`
- **Device**:
  - Android device with USB debugging enabled (for USB connection)
  - Network access and ADB over Wi-Fi enabled (for IP connection)
  - Root access required for some features
- **Permissions**: `sudo` access for installing dependencies

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/handsom3j4ck/Droidtool.git
   cd droidtool
   ```

2. **Make the Script Executable**:
   ```bash
   chmod +x droidtool
   ```

3. **Run the Script**:
   ```bash
   ./droidtool
   ```

The script will automatically check for and install `android-tools-adb` and `android-tools-fastboot` on supported systems (Debian/Ubuntu or Arch Linux). For other distributions, install these tools manually.

## Usage

1. **Launch the Script**:
   ```bash
   ./droidtool
   ```

2. **Select Connection Method**:
   - Choose USB or IP to connect to your Android device.
   - For USB, ensure USB debugging is enabled and accept the ADB prompt on the device.
   - For IP, ensure the device is on the same network and ADB over Wi-Fi is enabled.

3. **Navigate the Menu**:
   - Use the main menu to access categories like Device Connection & Info, App Management, Backup & Restore, etc.
   - Follow on-screen prompts to perform tasks.
   - Some features require root access and will prompt accordingly.

4. **Exit**:
   - Select option 8 from the main menu to exit cleanly, stopping the ADB server.

## Notes

- **Root Access**: Features marked "needs root" require a rooted device with `su` binary installed.
- **Timeouts**: Some operations (e.g., APK installation, sideloading) have timeouts to prevent hangs. Adjust these in the script if needed.
- **Safety**: Be cautious with destructive actions like clearing app data or uninstalling system apps. Always back up important data.
- **Android TV/Google TV**: The custom settings menu is tailored for Android TV devices but may work on other Android systems with similar configurations.

## Contributing

Contributions are welcome!


## Acknowledgments

- Built using ADB and Fastboot from the Android SDK Platform Tools.
- Inspired by the need for a simple, all-in-one Android management tool for Linux users.
