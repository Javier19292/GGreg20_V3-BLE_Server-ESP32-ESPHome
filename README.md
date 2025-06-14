# GGreg20_V3 Geiger counter BLE server using ESP32 with ESPHome firmware 

This repository provides an example of how to leverage ESPHome firmware on the GGreg20_V3 to implement a Bluetooth Low Energy (BLE) server. This setup enables the wireless transmission of Geiger counter measurements from your GGreg20_V3 to any compatible client application that can connect to it. A common example of such a client is a smartphone application.

For this setup, we're using an ESP32 as the MCU. This component choice is quite appealing: an ESP32 flashed with ESPHome firmware is perfectly capable of running its BLE server functions completely autonomously. What's more, if you have a Home Assistant server, the ESP32 will also transmit data to it.
