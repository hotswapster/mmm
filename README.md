iBBQ be a Pro
===

# About

This is a way to trend and track your grill/smoker cooks. It reads the temperatures from an Inkbird bluetooth temp probe and displays it on a chart. There is a text field where you can enter a comment like "Bumped top vent open 0.5", and it gets a timestmap and saves in a file.

# How it works
## Hardware
Inkbird IBT-2X is a bluetooth temperature module with two thermocouples. The thermocouples are placed inside the meat and the Inkbird module displays the temperature.

This setup uses a raspberry pi to communicate with the Inkbird module over Bluetooth Low Energy (BLE).

The Raspberry Pi has software running which makes it available over MQTT and via a Node Red web interface.

## Software

### Data Aquisition and Publishing

https://github.com/lukeryannetnz/go-ibbq
This software written in GO makes the BLE connection, reads the temperatures and battery level, and publishs the values to console and MQTT.
Battery level is not accurate.

### Display and Charting

Node-red is used to display this informaiton and provide the charts. It is the Node-Red configuratino that this repo is for.

