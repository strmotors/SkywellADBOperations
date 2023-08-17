# Skywell ADB Operations Guide
```
███████╗████████╗   ██████╗ 
██╔════╝╚══██╔══╝   ██╔══██╗
███████╗   ██║█████╗██████╔╝
╚════██║   ██║╚════╝██╔══██╗
███████║   ██║      ██║  ██║
╚══════╝   ╚═╝      ╚═╝  ╚═╝
```
Welcome to the Skywell ADB Operations Guide! This guide provides step-by-step instructions on how to manage ADB (Android Debug Bridge) operations on your Skywell ET5 vehicle.

**Note:** (Türkçe) Turkish instructions are available [here](https://github.com/strmotors/SkywellADBOperations/blob/main/README_TR.md).

## Introduction

With ADB, you can efficiently manage application installations and removals on your Skywell ET5 vehicle. The multimedia system in your vehicle is powered by the Android operating system, and every Android device features an ADB interface for debugging purposes. By leveraging this technology, you can connect to your vehicle's system, install new apps, and uninstall existing ones.

### Prerequisites

To get started, ensure you have the following:

- A device capable of creating a personal hotspot (e.g., your smartphone).
- A computer running Windows.

### Downloads

Download the essential files:

- [Skywell Folder](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing)

**Important Note:** Following these steps will not damage your device or void its warranty. All actions taken are reversible. To avoid warranty issues, it's recommended to uninstall any apps you've added before taking your vehicle for authorized service. For assistance, reach out to us at **strmotorstr@gmail.com**.

## Installation Steps

### Step 1: Prepare Necessary Files

1. Download the required files from [here](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing) and extract the "Skywell" folder from the downloaded archive.
2. Move the extracted "Skywell" folder to your desktop.
3. Place the .apk files you wish to install into the "Skywell" folder.

### Step 2: Connect to Car's Wi-Fi Network

1. Create a personal hotspot on your phone and connect both your car and computer to this hotspot.
2. In the car's settings, navigate to the "Bluetooth Calling" section and tap it repeatedly until the "wifi adb opened" message appears.
3. Find the car's IP address by accessing Wi-Fi settings in the car settings menu. Touch to the wifi you have connected and the car's IP address will appear.

### Step 3: Establish ADB Connection

1. Press `Windows Key + R` to open the "Run" window, then type `cmd` and press "OK".
2. In the Command Prompt, enter the following commands:

```
cd Desktop\Skywell
adb connect <Car's IP Address>
adb install ./<APK File Name>.apk
```
Replace `<Car's IP Address>` with the actual IP address obtained from the car's settings.

### Step 4: Verify Installation

1. After the installation process, open the application center on your vehicle.
2. If you can't see the newly installed app, close and reopen the application center from the cross icon on the top left.

## Uninstallation Steps

### Step 1: Prepare for Uninstallation

1. Ensure the "Skywell" folder is still on your desktop.
2. Make sure both the car and the computer are connected to the same Wi-Fi network.

### Step 2: Connect and Access ADB

1. Open the "Run" window again by pressing `Windows Key + R` and entering `cmd`.
2. In the Command Prompt, enter the following commands:

```
cd Desktop\Skywell
adb disconnect
adb connect <Car's IP Address>
adb shell am start -a android.settings.SETTINGS
```
Replace `<Car's IP Address>` with the car's IP address.

3. This will open the hidden "Settings" menu on the tablet. You can uninstall any app you want from this menu, just like any Android device.

## About the Author

This guide is authored by *ST-R Motors*. We hope this guide simplifies your ADB operations on your Skywell ET5 vehicle. Feel free to reach out to us at **strmotorstr@gmail.com** for any assistance.

Happy driving with your Skywell ET5!
