# Reworked service to have dynamic mqtt topics (multiple em24 via ports) and added 3 phase functionality.

## MQTT topics

Voltage L1:   #prefix#/voltage1<br>
Voltage L2:   #prefix#/voltage2<br>
Voltage L3:   #prefix#/voltage3<br>
<br>
Current L1:   #prefix#/current1<br>
Current L2:   #prefix#/current2<br>
Current L3:   #prefix#/current3<br>
<br>
Total Power:  #prefix#/power<br>
Power L1:     #prefix#/power1<br>
Power L2:     #prefix#/power2<br>
Power L3:     #prefix#/power3<br>
<br>
Import kwh:   #prefix#/import<br>
Export kwh:   #prefix#/export<br>
<br>
HZ:           #prefix#/hz<br>

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

