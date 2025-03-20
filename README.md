# Home Automation IoT with ESP32 and Arduino Cloud

This project demonstrates a **Home Automation IoT** system based on the **ESP32**. The system is integrated with **Arduino Cloud**, enabling remote control, real-time feedback, and the ability to operate in both **online** and **offline modes**. It also includes a **manual switch** for controlling devices locally, a **Wi-Fi Manager** for easy Wi-Fi setup, and **Google Home** integration for voice control.

## Features

- **ESP32 & Arduino Cloud Integration**: Remotely control and monitor your devices using the Arduino Cloud platform.
- **Online & Offline Modes**: The system works both when connected to the internet and offline, ensuring continuous operation.
- **Manual Switch**: Devices can be toggled via a manual switch, with real-time feedback to show the current state of devices.
- **Wi-Fi Manager**: The **BOOT** button triggers a Wi-Fi manager portal, allowing users to enter new Wi-Fi credentials.
- **Google Home Integration**: Control your devices using voice commands with **Google Home**, linked via **Arduino IoT Cloud** smart variables.
- **Boot Mode**: Press and hold the **BOOT** button to launch the Wi-Fi configuration portal.

## Requirements

### Hardware

- **ESP32 Development Board**
- **Manual Switch** (e.g., a button or relay to control devices)
- **Google Home** or a compatible voice assistant device

### Software

- **Arduino IDE** (with ESP32 board support)
- **Arduino Cloud** account (for device management and integration)
- **Google Home app** (for voice control setup)

## Installation

### 1. Set up Arduino IDE for ESP32

1. Download and install the [Arduino IDE](https://www.arduino.cc/en/software).
2. Open Arduino IDE and go to `File` > `Preferences`.
3. In the "Additional Boards Manager URLs" section, add the following URL:
    ```
    https://dl.espressif.com/dl/package_esp32_index.json
    ```
4. Go to `Tools` > `Boards` > `Boards Manager`, search for **ESP32**, and install the package.

### 2. Set up Arduino Cloud

1. Sign up or log in to [Arduino Cloud](https://create.arduino.cc/).
2. Create a new device using your **ESP32** board and follow the prompts to link it to the cloud.
3. Create **smart variables** for controlling devices (e.g., switches, relays) in Arduino IoT Cloud, and enable **Google Home integration**.

### 3. Wi-Fi Configuration

To set up Wi-Fi credentials on the ESP32:

1. Press and hold the **BOOT** button on the ESP32 to enter Wi-Fi manager mode.
2. The ESP32 will create a Wi-Fi Access Point (AP) where you can connect and enter the new Wi-Fi credentials.
3. Once credentials are saved, the ESP32 will automatically reconnect to the Wi-Fi network.

Alternatively, you can hardcode Wi-Fi credentials directly into the sketch (less recommended for dynamic environments).

### 4. Upload the Code

1. Clone or download this repository to your local machine.
2. Open the **Arduino IDE**, go to `File` > `Open`, and select the project file (`.ino`).
3. Connect your **ESP32** to your computer via USB.
4. In the IDE, go to `Tools` > `Board` > `ESP32 Dev Module` and select the correct port.
5. Click **Upload** to transfer the code to the ESP32.

## Usage

### Boot Mode for Wi-Fi Configuration

1. To change Wi-Fi settings, press and hold the **BOOT** button on the ESP32.
2. The ESP32 will create a local Wi-Fi network. Connect to it with your phone or laptop.
3. Enter your new Wi-Fi credentials via the portal that appears.
4. Once saved, the ESP32 will reconnect to the specified Wi-Fi network.

### Google Home Integration

1. Link your **ESP32 device** to **Google Home** via the Arduino Cloud IoT integration.
2. Once linked, you can control devices using voice commands like:
   - "Hey Google, turn on the lights."
   - "Hey Google, set the fan to 50%."

## Acknowledgments

- **Arduino IoT Cloud**: For simplifying cloud integration and device management.
- **ESP32**: A powerful and versatile platform for IoT development.
- **Google Home**: For adding voice control to the automation system.
- **Wi-Fi Manager Library**: For easily managing Wi-Fi credentials without the need for hardcoding.



