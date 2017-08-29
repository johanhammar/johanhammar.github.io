---
layout: post
title:  "How to configure a switch in Domoticz"
date:   2017-08-28 20:55:00 +0100
categories: raspberry pi automation domoticz 433mhz
---
This is a note to self on how to configure an ac outlet using RFXtrx433 in Domoticz.

1. Browse to your Domotics instance and go to the "Switches" tab
2. Click on Manual Light/Switch
3. Now configure the new device:
    1. First give the new device a new name
    2. Switch Type should be ```On/Off```
    3. Change Type to ```AC```
    4. Give the device a unique random id
    5. Set the outlet in "learn mode" and click "Test"
4. Done!
