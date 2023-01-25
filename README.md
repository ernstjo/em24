# Reworked service to have dynamic mqtt topics (multiple em24 via ports) and added 3 phase functionality.

## MQTT topics

Voltage L1:   #prefix#/voltage1
Voltage L2:   #prefix#/voltage2
Voltage L3:   #prefix#/voltage3

Current L1:   #prefix#/current1
Current L2:   #prefix#/current2
Current L3:   #prefix#/current3

Total Power:  #prefix#/power
Power L1:     #prefix#/power1
Power L2:     #prefix#/power2
Power L3:     #prefix#/power3

Import kwh:   #prefix#/import
Export kwh:   #prefix#/export

HZ:           #prefix#/hz

## Description

Works with Victron Energy ESS<br>

Subscribe to a local MQTT broker and make energy data available on a Modbus server

sml_smartmeter  -->  MQTT broker  -->  em24  <--  Victron


Thanks to 
https://github.com/stephane/libmodbus

## Installation


apt install libmodbus5 libmodbus-dev


cp em24.service /etc/systemd/system/<br>
systemctl enable em24.service<br>
systemctl start em24.service

