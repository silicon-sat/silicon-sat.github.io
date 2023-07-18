---
sort: 1
---

# GROUND STATION 

**USEFUL LINKS**

- [Silicon_OrbitLab_TGS1](https://tinygs.com/station/Silicon_OrbitLab_TGS1@6240637039)
- [TinyGS](https://tinygs.com) 
- [TinyGS GitHub Page](https://github.com/G4lile0/tinyGS)
- [Sooraj Shenoy VU3ZAG](https://soorajshenoys.blogspot.com/2023/01/lora-433mhz-tinygs-satellite-ground.html): Installed our first setup using this site.  


## TINY GS Silicon_OrbitLab_TGS1


**14 JULY 2023**

- Replaced the V-dipole with a better construct by attaching a SMA on the antenna and using low-loss rigid SMA-SMA connector to connect to a SMA-to-U.fl that is attached to the LoRa module. Received packets from Norbi-2!


**7 JULY 2023**

- Replaced the spring antenna with a V-dipole (rabbit year) and received 4 packets within 2 days from Norbi and Norbi-2.

**24 JUNE 2023**

- **HARDWARE**:
  - An old **ESP-WROOM-32** Development board.
  - **AI-Thinker RA-02 LoRa Module** ISM:410-525MHz
  - Spring Antenna with a UFL connector provided with the LoRa module.
  - Connected the ESP32 and LoRa module following [Sooraj Shenoy VU3ZAG's blog](https://soorajshenoys.blogspot.com/2023/01/lora-433mhz-tinygs-satellite-ground.html). [See Circuit Diagram here](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiPLXVwBgXXILY6AirUq9ShTVVTN6xoJR0XoF2F4YatzZkGx725gxbevitd35hwaW-gN5zmFXhxZ16sYMLWMtI3AHicCbGBdiQuepzj7F09rUw8RHgCNEeEBdWACViDJuf4WEvP-KMYnK3eSaRneuvUs43CwqN_q3icXc82oeoE3XxNJLL2y_ylKYjQTg/s2864/circuit.jpg).

- **GROUND STATION CONFIGURATION**
  - Config detailed in this [GitPage](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration)
  - Flash the ESP32 board using the **One-click Uploader**. See the [Quick Start Guide](https://github.com/G4lile0/tinyGS/wiki/Quick-Start).
    - You don't need to have the LoRa module connected when flashing and configuration.
    - You can also use the Platform IO for flashing as detailed in the [TinyGS GitHub Page](https://github.com/G4lile0/tinyGS).
    - Noticed that for flashing the board, needed to hold the BOOT button down while connecting the USB cable but not sure. Also mentioned in VU3ZAG's blog. 
  - After successful flash, boot it up and it will become a hotspot with SSID **My Tiny GS**.
  - Connect to the hotspot and browse to `192.168.4.1` and configure the board.
  - For the **MQTT** credentials, you need to join the [Tiny GS Telegram Community](https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q) and using your TinyGS Personal Bot account request the credentials by typing `/mqtt`
  - For the **Board Type** select `433 MHz TTGO LoRa 32 v2` from the dropdown menu.
  - DO NOT select **TX** unless you are a HAM license holder.
  - Once all info is entered click on the `Apply` button. The ESP32 will reboot and if all went well the ground station should appear on the Tiny GS site.
  - Once the ground station is estabilished, you can get a temporary passwordless link to your station by typing `/weblogin` in your telegram BOT. This link will allow you to modify the groundsation parameters.

- **ANTENNA AND PLACEMENT**
  - The provided tiny spiral antenna was used and the unit was pasted on a south facing window on the fourth floor just to check if we receive any thing. 
  - No telemetry signal was received but some packets were receive with RSSI and SNR as shown in the below picture [FIXME: put the picture]
  - Next step is to build a rabbit ear antenna by following this post on [Telegram](https://t.me/c/1448773154/24354).
