# GGreg20 V3 Geiger Counter BLE Server

![Geiger Counter](https://example.com/path/to/geiger-counter-image.png)  
![ESP32](https://example.com/path/to/esp32-image.png)  
![ESPHome](https://example.com/path/to/esphome-image.png)  

Welcome to the **GGreg20 V3 Geiger Counter BLE Server** repository! This project turns an ESP32 microcontroller into a Bluetooth Low Energy (BLE) server for a Geiger counter. Using ESPHome firmware, it provides a simple way to monitor radiation levels.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)
- [Contact](#contact)

## Overview

The GGreg20 V3 is designed to measure radiation levels and transmit this data via BLE. This project uses the ESP32 microcontroller for its capabilities and ESPHome for easy configuration. You can connect to the server using a BLE-enabled device to view real-time radiation data.

## Features

- **Real-time Radiation Monitoring**: Get instant updates on radiation levels.
- **BLE Connectivity**: Connect to your devices easily using Bluetooth Low Energy.
- **User-friendly Configuration**: Configure settings through ESPHome.
- **Compact Design**: Designed for portability and ease of use.
- **Open Source**: Contribute and modify the code as you see fit.

## Installation

To set up the GGreg20 V3 Geiger Counter BLE Server, follow these steps:

1. **Hardware Requirements**:
   - ESP32 Development Board
   - Geiger Counter Module (compatible with GGreg20 V3)
   - USB Cable for power and programming
   - Breadboard and jumper wires (optional)

2. **Software Requirements**:
   - Install [ESPHome](https://esphome.io/guides/getting_started_hassio.html) on your system.
   - Ensure you have Python and pip installed for running ESPHome commands.

3. **Clone the Repository**:
   Clone this repository to your local machine using the following command:
   ```bash
   git clone https://github.com/Javier19292/GGreg20_V3-BLE_Server-ESP32-ESPHome.git
   ```

4. **Install Dependencies**:
   Navigate to the project directory and install required dependencies:
   ```bash
   cd GGreg20_V3-BLE_Server-ESP32-ESPHome
   pip install -r requirements.txt
   ```

5. **Upload Firmware**:
   Use the ESPHome command to upload the firmware to your ESP32:
   ```bash
   esphome run ggreg20_v3.yaml
   ```

## Usage

Once the firmware is uploaded, follow these steps to use the GGreg20 V3 Geiger Counter:

1. **Power the Device**: Connect the ESP32 to a power source.
2. **Connect via BLE**: Use a BLE scanner app on your smartphone or computer to find the GGreg20 V3 device.
3. **Monitor Radiation Levels**: Open the app and connect to the GGreg20 V3. You will see real-time radiation data.

## Configuration

You can customize the configuration by editing the `ggreg20_v3.yaml` file. Here are some key sections you can modify:

- **Sensor Configuration**: Adjust the settings for the Geiger counter.
- **BLE Settings**: Change the name and advertising interval of the BLE server.
- **Logging**: Enable or disable logging for debugging purposes.

Here is an example configuration snippet:

```yaml
sensor:
  - platform: geiger_counter
    id: ggreg20
    name: "GGreg20 V3 Radiation Level"
    update_interval: 5s
```

## Contributing

We welcome contributions! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your branch and create a pull request.

Please ensure that your code follows the project's style guidelines and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

To download the latest firmware and updates, visit the [Releases](https://github.com/Javier19292/GGreg20_V3-BLE_Server-ESP32-ESPHome/releases) section. Here you can find the necessary files to download and execute.

## Contact

For any questions or support, please reach out via the Issues section on GitHub or contact me directly at [your_email@example.com](mailto:your_email@example.com).

![BLE Icon](https://img.shields.io/badge/BLE-Enabled-brightgreen)  
![ESP32](https://img.shields.io/badge/ESP32-Board-blue)  
![ESPHome](https://img.shields.io/badge/ESPHome-Config-orange)  

Thank you for your interest in the GGreg20 V3 Geiger Counter BLE Server! We hope you find it useful for your radiation monitoring needs.