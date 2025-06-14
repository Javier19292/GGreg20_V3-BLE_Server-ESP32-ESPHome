[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner-direct-team.svg)](https://stand-with-ukraine.pp.ua)

# GGreg20_V3 Geiger counter BLE server using ESP32 with ESPHome firmware 

This repository provides an example of how to leverage ESPHome firmware on the GGreg20_V3 to implement a Bluetooth Low Energy (BLE) server. This setup enables the wireless transmission of Geiger counter measurements from your GGreg20_V3 to any compatible client application that can connect to it. A common example of such a client is a smartphone application.

For this setup, we're using an ESP32 as the MCU. This component choice is quite appealing: an ESP32 flashed with ESPHome firmware is perfectly capable of running its BLE server functions completely autonomously. What's more, if you have a Home Assistant server, the ESP32 will also transmit data to it.

![image](https://github.com/user-attachments/assets/175fc242-507c-4678-b0d4-040ed92edbd4)

Please do not modify the UUIDs specified in this example. It's crucial to keep them as-is, as changing these BLE GATT UUID services or UUID characteristics could lead to incompatibility with other services we may develop in the future.
```YAML
  services:
    # Radiation Monitoring Service
    - uuid: "decccc6a-5126-5d0f-9951-cbe8fcf57724"

      characteristics:
        # CPM as a string
        - id: cpm_characteristic
          uuid: "2257ebe9-664d-5623-b78b-1d462ea39bea"
            
        # CPM Moving Average as a string
        - id: cpm_ma5_characteristic
          uuid: "0cf388bb-d350-58b5-9bfa-c6e33000b8e5"
```
