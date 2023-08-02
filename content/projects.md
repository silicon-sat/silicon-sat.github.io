---
sort: 1
---

# Projects

## TinyGS Ground Station

[TinyGS](https://tinygs.com) is an open network of Ground Stations distributed around the world to receive and operate LoRa satellites, weather probes and other satellites, using low-cost and versatile receiver modules based on ESP32 Wifi chipset and sx126x/sx127x LoRa chipset. 
The goal of this project is to use the tinyGS platform to experiment with the satellite communication technology and eventually come up with a plan for our future tiny/pico satellite format. This will involve trying out different communication protocols like LoRa and FSK. Do experiemnts with current satellites in terms of antennas used and monitor robustness of the commmunication protocol w.r.t. power, environment, geographical location and so on. As part of this project, we will experiment with different antenna technologies.

**Resources**

- [TinyGS GitHub Page](https://github.com/G4lile0/tinyGS)

## Attitude Determination and Control System (ADCS)

Attitude control is the problem of ensuring the orientation of the satellite while in orbit. 
The standard control technique in larger satellites is the use of thrusters but that is mostly prohibitive in small satellite because of cost and minaturization of thrusters. Therefore, attitude control for tinySats remains a fairly open problem. The goal of this project is to investigate passive stabilization technique for a tiny/pico satellite format. The primary goal would be simplicity and robustness in design and being able to simulate and predict it's orbital behaviour with very good accuracy.


## Python-based Orbital Environment Simulator

The objective of the Orbital Environment Simulator is to model the first- and second-order orbital dynamics of the satellite so that electro-mechanical systems sich as ADCS can be simulated to reasonable accuracy. Since the primary goal of this satellite program is to keep everything open-source, Python becomes a suitable choice.
