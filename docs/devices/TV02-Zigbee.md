---
title: "TuYa TV02-Zigbee control via MQTT"
description: "Integrate your TuYa TV02-Zigbee via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendors bridge or gateway."
addedAt: 2021-11-30T20:10:17
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa TV02-Zigbee

|     |     |
|-----|-----|
| Model | TV02-Zigbee  |
| Vendor  | TuYa  |
| Description | Thermostat radiator valve |
| Exposes | battery_low, lock (state), open_window, open_window_temperature, holiday_temperature, comfort_temperature, eco_temperature, climate (preset, local_temperature_calibration, local_temperature, current_heating_setpoint), boost_timeset_countdown, frost_protection, heating_stop, online, holiday_mode_date, programming, error_status, linkquality |
| Picture | ![TuYa TV02-Zigbee](https://www.zigbee2mqtt.io/images/devices/TV02-Zigbee.jpg) |
| White-label | Moes TV01-ZB, Tesla Smart TSL-TRV-TV01ZG, Unknown/id3.pl GTZ08 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->

## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).



## Exposes

### Battery_low (binary)
Indicates if the battery of this device is almost empty.
Value can be found in the published state on the `battery_low` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` battery_low is ON, if `false` OFF.

### Lock 
The current state of this lock is in the published state under the `child_lock` property (value is `LOCK` or `UNLOCK`).
To control this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"child_lock": "LOCK"}` or `{"child_lock": "UNLOCK"}`.
It's not possible to read (`/get`) this value.

### Open_window (binary)
Enables/disables the status on the device.
Value can be found in the published state on the `open_window` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"open_window": NEW_VALUE}`.
If value equals `ON` open_window is ON, if `OFF` OFF.

### Open_window_temperature (numeric)
Open window temperature.
Value can be found in the published state on the `open_window_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"open_window_temperature": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `30`.
The unit of this value is `°C`.

### Holiday_temperature (numeric)
Holiday temperature.
Value can be found in the published state on the `holiday_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"holiday_temperature": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `30`.
The unit of this value is `°C`.

### Comfort_temperature (numeric)
Comfort temperature.
Value can be found in the published state on the `comfort_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"comfort_temperature": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `30`.
The unit of this value is `°C`.

### Eco_temperature (numeric)
Eco temperature.
Value can be found in the published state on the `eco_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"eco_temperature": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `30`.
The unit of this value is `°C`.

### Climate 
This climate device supports the following features: `preset`, `local_temperature_calibration`, `local_temperature`, `current_heating_setpoint`.
- `current_heating_setpoint`: Temperature setpoint. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"current_heating_setpoint": VALUE}` where `VALUE` is the °C between `0` and `30`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"current_heating_setpoint": ""}`.
- `local_temperature`: Current temperature measured on the device (in °C). Reading (`/get`) this attribute is not possible.
- `preset`: Mode of this device (similar to system_mode). To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"preset": VALUE}` where `VALUE` is one of: `auto`, `manual`, `holiday`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"preset": ""}`.
- `local_temperature_calibration`: Offset to be used in the local_temperature. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"local_temperature_calibration": VALUE}.`

### Boost_timeset_countdown (numeric)
Setting minimum 0 - maximum 465 seconds boost time. The boost (♨) function is activated. The remaining time for the function will be counted down in seconds ( 465 to 0 )..
Value can be found in the published state on the `boost_timeset_countdown` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"boost_timeset_countdown": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `465`.
The unit of this value is `second`.

### Frost_protection (binary)
When Anti-Freezing function is activated, the temperature in the house is kept at 8 °C ‚the device display "AF".press the pair button to cancel..
Value can be found in the published state on the `frost_protection` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"frost_protection": NEW_VALUE}`.
If value equals `ON` frost_protection is ON, if `OFF` OFF.

### Heating_stop (binary)
Battery life can be prolonged by switching the heating off. To achieve this, the valve is closed fully. To activate the heating stop, the device display "HS" ‚press the pair button to cancel..
Value can be found in the published state on the `heating_stop` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"heating_stop": NEW_VALUE}`.
If value equals `ON` heating_stop is ON, if `OFF` OFF.

### Online (binary)
Is the device online.
Value can be found in the published state on the `online` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"online": NEW_VALUE}`.
If value equals `ON` online is ON, if `OFF` OFF.

### Holiday_mode_date (text)
The holiday mode( ⛱ ) will automatically start at the set time starting point and run the holiday temperature..
Value can be found in the published state on the `holiday_mode_date` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"holiday_mode_date": NEW_VALUE}`.

### Programming (composite)
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"undefined": {"schedule_monday": VALUE, "schedule_tuesday": VALUE, "schedule_wednesday": VALUE, "schedule_thursday": VALUE, "schedule_friday": VALUE, "schedule_saturday": VALUE, "schedule_sunday": VALUE}}`
- `schedule_monday` (text): undefined. 
- `schedule_tuesday` (text): undefined. 
- `schedule_wednesday` (text): undefined. 
- `schedule_thursday` (text): undefined. 
- `schedule_friday` (text): undefined. 
- `schedule_saturday` (text): undefined. 
- `schedule_sunday` (text): undefined. 

### Error_status (numeric)
Error status.
Value can be found in the published state on the `error_status` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

