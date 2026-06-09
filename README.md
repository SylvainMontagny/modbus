# LoRaWAN to Mobbus Interface
This Node-RED flows is a example of a LoRaWAN to Modbus interface. It reads data from a LoRaWAN server (LNS) and write them in a Modbus TCP server.

# Requirements
- Node-RED
- node-red-contrib-modbus palette
- A Chirpstack or TTN (The Things Stack) LNS
- A LoRaWAN device (STM32WL) with simulated Thermostatic valve firwmware (see https://univ-lorawan.fr/compiler)
- A Modbus Server

# Getting started
1. Configure the MQTT subscriber to get the decoded data from your End-Device
2. Open the "configuration node" and uncomment the code according to the LNS used.
3. Configure the Modbus server Ip address and port in the Modbus Client Write node.
4. deploy the flow

valveTemperature and valveSetpoint LoRaWAN payload will be writte in Holding Register 40001 and 40002.


