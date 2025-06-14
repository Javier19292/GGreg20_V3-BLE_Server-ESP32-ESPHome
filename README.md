[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner-direct-team.svg)](https://stand-with-ukraine.pp.ua)

# GGreg20_V3 Geiger counter BLE server using ESP32 with ESPHome firmware 

This repository provides an example of how to leverage ESPHome firmware on the [GGreg20_V3](https://iot-devices.com.ua/en/product/ggreg20_v3-ionizing-radiation-detector-with-geiger-tube-sbm-20/) to implement a Bluetooth Low Energy (BLE) server. This setup enables the wireless transmission of Geiger counter measurements from your GGreg20_V3 to any compatible client application that can connect to it. A common example of such a client is a smartphone application.

For this setup, we're using an ESP32 as the MCU. This component choice is quite appealing: an ESP32 flashed with ESPHome firmware is perfectly capable of running its BLE server functions completely autonomously. What's more, if you have a Home Assistant server, the ESP32 will also transmit data to it.

On the ESP32 BLE Server side of the ESPHome firmware for ESP32, we create only two sensors - one for the instant CPM value and the other for the 5 minute moving average CPM value. Accordingly, for BLE, we create one service with two characteristics. Since GATT (See Bluetooth SIG Assigned Numbers) does not have an assigned UUID number for the geiger counter service, we use custom UUIDs that we generated for our project ourselves.
In this example, we believe that the rest of the calculations should be done on the BLE client side, i.e. in the application. 


![image](https://github.com/user-attachments/assets/175fc242-507c-4678-b0d4-040ed92edbd4)

⚠️ Please do not modify the UUIDs specified in this example. It's crucial to keep them as-is, as changing these BLE/GATT service-UUID or characteristic-UUIDs could lead to incompatibility with other services we may develop in the future.
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
> For Connection Diagrams please visit: [GGreg20_V3 with generic ESP32 under Home Assistant with ESPHome setup example -> The three options are shown in the following figures](https://github.com/iotdevicesdev/GGreg20_V3-ESP32-HomeAssistant-ESPHome/tree/main#the-three-options-are-shown-in-the-following-figures)
