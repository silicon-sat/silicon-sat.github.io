---
sort: 5
---

# ANTENNAS

**RESOURCES**

- [TinyGS Antenna Wiki Page](https://github.com/G4lile0/tinyGS/wiki/Antenna)

## Quarter Wave Ground Plane

- [1/4 wave ground plane calculator](https://m0ukd.com/calculators/quarter-wave-ground-plane-antenna-calculator/) 
- [Simple Ground Plane Antennas for 2/1.25/0.7meter band](http://www.n1gy.com/simple-ground-plane-antennas.html): Blog from HAM N1GY using SO-239 UHF Conn (not recommended for >100MHz). 
- [LoRa/LoRaWAN tutorial 44](https://www.youtube.com/watch?v=bWpjDM2CJXI): Very nice YuTube tutorial on 1/4-Wave Ground Plane Antenna.
- [Andrea Spiess Video #368](https://www.youtube.com/watch?v=6cVYsHCLKq8): How to build performing antennas for LoRa, WiFi, 433MHz, Airplanes etc.(NanoVNA, MMANA-GAL)`

**Two Antenna Specs Built at Orbit Lab on 26 Sep 2023**

The antennas were constructed following the above resources. The measurements were done using a **Keysight N9918A VNA** during a demo day.

- **Antenna-1**: 
  - Radiating Element: 16.2cm
  - Radials: La=3.2cm, Lb=17.5cm
  - VSWR@434.18 MHz: 1.2
  - Smith: 46.5 ohm + j9.2 ohm
- **Antenna-2**:
  - Radiating Element: 16cm
  - Radials: La=3.2cm, Lb=18cm
  - VSWR@432.2 MHz: 1.181
  - Smith: 50 ohm + j8.6 ohm

## Simulation

**4NEC2**
- [Official Site](https://www.qsl.net/4nec2/)

## Tuning 

- [LiteVNA](https://www.aliexpress.com/item/1005003551867442.html?srcSns=sns_Copy&spreadType=socialShare&bizType=ProductDetail&social_params=60367037557&aff_fcid=76c9a8868cce4ddab20cdf6d610738b4-1692354904870-06492-_EQ2ZMAP&tt=MG&aff_fsk=_EQ2ZMAP&aff_platform=default&sk=_EQ2ZMAP&aff_trace_key=76c9a8868cce4ddab20cdf6d610738b4-1692354904870-06492-_EQ2ZMAP&shareId=60367037557&businessType=ProductDetail&platform=AE&terminal_id=b7f9ed03597c45148e1069eb4123f838&afSmartRedirect=y): Original Hugen 50kHz ~ 6.3GHz tinyVNA LiteVNA 64 4" Display Vector Network Analyzer HF VHF UHF Antenna.
  - Got reference from [tinyGS Telegram](https://t.me/c/1448773154/78473/88123)
  - [YouTube on Tuning a 1/4 wave using a LiteVNA from above guy](https://www.youtube.com/watch?v=OJy-XjGYlGw)
- [LoRa/LoRaWAN tutorial 40: N1201SA Vector Impedance Analyzer](https://youtu.be/d3WSn_MaYiA)

