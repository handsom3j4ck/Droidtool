# Droidtool - Linux Android Management Tool

**Droidtool** is a Bash script designed to simplify the management of Android devices from a Linux system using ADB (Android Debug Bridge) and Fastboot. It provides a user-friendly, menu-driven interface for performing a wide range of tasks, from app management to system tweaks, backups, and developer tools.

## Features

- **Device Connection & Info**:
  - Connect via USB, IP, or ADB Wireless Pair (Android 11+)
  - Display device info (brand, model, Android version, serial number)
  - Show battery health, storage usage, CPU/memory usage (root required), and uptime
  - Verify root access and device status (root required)
  - Show device model, foreground app, and network info (IP, Wi-Fi SSID, signal strength)
  - Disconnect device from ADB

- **App Management**:
  - Install single or multiple APKs
  - Uninstall or batch-uninstall apps
  - Enable/disable apps
  - Clear cache for all apps (root required)
  - Extract APKs from the device
  - Push APKs as system apps (root required)
  - Disable bloatware (hide apps without uninstalling)

- **Backup & Restore**:
  - Backup all apps and data or specific app data (ADB or root methods)
  - Restore from backup files (`.ab`, `.ab.gz`, or `.tar.gz` with root)
  - List available backups
  - Root options for backing up `/data`, `/system`, `/cache` partitions or specific app data via `tar.gz`

- **File Management**:
  - Pull files or folders from the device
  - Push files or folders to the device
  - Delete files or folders from the device
  - Search for files or folders on the device

- **Reboot & Recovery**:
  - Reboot to system, recovery, bootloader, or fastboot mode
  - Sideload ZIP files in recovery mode

- **Developer Tools**:
  - View and save logcat output
  - Access device shell
  - Take screenshots
  - Change device language (root required)
  - Toggle dark mode (Android 10+)

- **Custom Settings for Android TV/Google TV**:
  - Apply general-purpose performance improvements
  - Enable processing speed management
  - Clear cache memory (root required)
  - Optimize app performance
  - Close background apps
  - Clear app data and cache
  - Check for system updates
  - Configure private DNS to remove ads (AdGuard or ControlD)

- **Utilities**:
  - Additional tools for enhanced device management (to be expanded based on contributions)

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
   - Choose USB, IP, or ADB Wireless Pair to connect to your Android device.
   - For USB, ensure USB debugging is enabled and accept the ADB prompt on the device.
   - For IP, ensure the device is on the same network and ADB over Wi-Fi is enabled.
   - For ADB Wireless Pair (Android 11+), enable 'Pair over Wi-Fi' in Developer Options and provide the pairing port and code.

3. **Navigate the Menu**:
   - Use the main menu to access categories like Device Connection & Info, App Management, Backup & Restore, File Management, Reboot & Sideload, Developer Tools, Custom Settings, and Utilities.
   - Follow on-screen prompts to perform tasks.
   - Some features require root access and will prompt accordingly.

4. **Exit**:
   - Select option 9 from the main menu to exit cleanly, stopping the ADB server.

## Notes

- **Root Access**: Features marked "needs root" require a rooted device with `su` binary installed.
- **Timeouts**: Some operations (e.g., APK installation, sideloading) have timeouts to prevent hangs. Adjust these in the script if needed.
- **Safety**: Be cautious with destructive actions like clearing app data, uninstalling system apps, or deleting files/folders. Always back up important data.
- **File Management**: Use `/storage/emulated/0` instead of `/sdcard` for reliable file operations, as `/sdcard` is a symlink.
- **Android TV/Google TV**: The custom settings menu is tailored for Android TV devices but may work on other Android systems with similar configurations.
- **Backup & Restore**: ADB backups may fail for app data on Android 6+ due to system limitations; root-based `tar.gz` backups are recommended for reliability.

## Contributing

Contributions are welcome! Please submit pull requests or issues to the [GitHub repository](https://github.com/handsom3j4ck/Droidtool).

## Acknowledgments

- Built using ADB and Fastboot from the Android SDK Platform Tools.
- Inspired by the need for a simple, all-in-one Android management tool for Linux users.