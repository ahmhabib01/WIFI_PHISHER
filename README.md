# WIFI_PHISHER
<p align="center">
<a href="https://github.com/ahmhabib01/WIFI_PHISHER/"><img title="Tool" src="https://img.shields.io/badgeWIFI_PHISHER"></a>
<img title="Version" src="https://img.shields.io/badge/Version-1.0-green">
<img title="Support" src="https://img.shields.io/badge/Support-No-red">
</p>

## A franken baby of [M1z23R/ESP8266-EvilTwin](https://github.com/M1z23R/ESP8266-EvilTwin) and [adamff1/ESP8266-Captive-Portal](https://github.com/adamff1/ESP8266-Captive-Portal).

<img src="https://user-images.githubusercontent.com/32341044/202444452-3e7c9ab0-1643-4996-8319-18b8c25544fa.jpg"></img><br>

It uses an ESP8266 to attack a WiFi network using Deauther && || Evil-Twin AP method.

## FEATURES :
* Deauthentication of a target WiFi access point
* Evil-Twin AP to capture passwords with password verification against the og access point
* It can do both attacks at the same time, no toggling of the deauther is required. 

## DISCLAIMER
The source code given in this public repo is for educational use only and should only be used against your own networks and devices!<br>
Please check the legal regulations in your country before using it.

## Install using Arduino IDE
1. Install Arduino IDE
2. In Arduino go to `File` -> `Preferences` add this URL to `Additional Boards Manager URLs` ->
   `https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json`  
3. In Arduino go to `Tools` -> `Board` -> `Boards Manager` search for and install the `deauther` package  
4. Download and open [WIFI_PHISHER](https://github.com/ahmhabib01/WIFI_PHISHER/blob/main/ESP8266_WIFI_PHISHER.ino) with Arduino IDE
6. Select an `ESP8266 Deauther` board in Arduino under `tools` -> `board`
7. Connect your device and select the serial port in Arduino under `tools` -> `port`
8. Click Upload button

# How to use:
- Connect to the AP named `Bangladesh_cyber_2_0` with password `ahmhabib01` from your phone/PC.
- Select the target AP you want to attack (list of available APs refreshes every 30secs - page reload is required).
- Click the Start Deauthing button to start kicking devices off the selected network.
- Click the Start Evil-Twin button and optionally reconnect to the newly created AP named same as your target (will be open).
- You can stop any of the attacks by visiting `192.168.4.1/admin` while conected to Evil-Twin AP or by resetting the ESP8266.
- Once a correct password is found, AP will be restarted with default ssid `Bangladesh_cyber_2_0` / `ahmhabib01` and at the bottom of a table you should be able to see something like "Successfully got password for - `TARGET_SSID` - `PASSWORD`
   - If you power down / hard reset the gathered info will be lost
 


## Credits:
* https://github.com/SpacehuhnTech/esp8266_deauther
* https://github.com/M1z23R/ESP8266-EvilTwin
* https://github.com/adamff1/ESP8266-Captive-Portal

## License 
This software is licensed under the [MIT License](https://opensource.org/licenses/MIT).