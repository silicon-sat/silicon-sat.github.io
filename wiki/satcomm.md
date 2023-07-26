---
sort: 4
---

# SAT-COMM

Satellite Communication 

## LoRa

LoRa is Low-Power Wide-Area Network (LPWAN) technology from Semtech. It started as a protocol for builliding long-range (hence LoRa) low-power network for Internet of Things (IoT). It has now become popular for satellite communication for tinySats since low-bandwidth data can be transferred with very little energy which is attractive for tinySats with tiny batteries. Also, it uses a **non-licensed** band ISM (eg. 434 MHz) that is suitable for global use in the amateur band. In India **434-438MHz** is an amatuer band. So you are free to receive in this band but need an amateur license to transmit. 

**REFERENCES**

- **Papers**:
  - Hwang et.al., _A survey on LPWA technology: LoRa and NB-IoT_ , ICT Express, 2017 Elsevier [Link](https://www.sciencedirect.com/science/article/pii/S2405959517300061)
  - Roedig et.al. _LoRa for the Internet of Things_ , 2016, [Link](https://eprints.lancs.ac.uk/id/eprint/77615/1/MadCom2016_LoRa_MAC.pdf) --  _Good comprehensive info on LoRa technology_ * Resources: [LoRaBlink Kit](https://mcbor.github.io/lorablink-kit/) -- devleopment platform., [LoRaSim](https://www.lancaster.ac.uk/scc/sites/lora/lorasim.html) -- SimPy-based LoRa simulator.
  - Karthikeyan A, et.al., _LoRa technology-an overview_ , IEEE 2018 [Link](https://ieeexplore.ieee.org/iel7/8466240/8474542/08474715.pdf)

- **Application Notes**:
  - [LoRa Basics, SemTech](https://www.dropbox.com/s/rmyebqd4j0fbfy9/AN1200_22_Semtech_LoRa_Basics_v2_STD.pdf)
- **Datasheets**:
  - [SX1261](https://www.dropbox.com/s/ct5q16a4aohzl1a/Datasheet-SX1261-2_V2_1.pdf)
    - [AppNotes, etc](https://www.semtech.com/products/wireless-rf/lora-connect/sx1261#documentation)
  - [SX127X](https://www.dropbox.com/s/9ohuuyscbmycjts/Datasheet-SX1276-7-8-9_W_APP_V7.pdf)
    - [Appnotes, etc](https://www.semtech.com/products/wireless-rf/lora-connect/sx1278#documentation)


**TECHNOLOGY**

**LoRa**

LoRa (Long Range) is a proprietary spread spectrum modulation technique by Semtech. It is a derivative of Chirp Spread Spectrum (CSS). The LoRa physical layer may be used with any MAC layer; however, LoRaWAN is the currently proposed MAC which operates a network in a simple star topology.

**LoRaWAN**

As LoRa is capable of transmiting over very long distances LoRaWAN naturally selects star topology. Nodes transmit directly to a gateway which is powered and connected to a backbone infrastructure. Gateways are powerful transceivers capable of connecting to multiple devices concurrently (up to 50).  Three classes of node devices are defined.

**LoRa Physical Layer**

LoRa is a physical layer specification based on CSS with integrated Forward Error Correction (FEC). Transmissions use a wide band to counter interference and to handle frequency offsets due to low cost crystals. A LoRa receiver can decode transmissions 19.5 dB below the noise floor. Thus, very long communication distances can be bridged. LoRa key properties are: long range, high robustness, multipath resistance, Doppler resistance, low power. LoRa operates in the lower ISM bands (EU: 868 MHz and 433 MHz, USA: 915 MHz and 433 MHz).  A LoRa radio has four configuration parameters: _carrier frequency, spreading factor, bandwidth_ and _coding rate_. The selection of these parameters determines energy consumption, transmission range and resilience to noise. 

_Carrier Frequency (CF)_ is the centre frequency used for the transmission band. For the SX1272 it is in the range of 860 MHz to 1020 MHz, programmable in steps of 61 Hz. The alternative radio chip Semtech SX1276 allows adjustment from 137 MHz to 1020 MHz. 

_Spreading Factor (SF)_ is the ratio between the symbol rate and chip rate.  A higher spreading factor increases the Signal to Noise Ratio (SNR), and thus sensitivity and range, but also increases the air time of the packet. The number of chips per symbol is calculated as 2^SF. For example, with an SF of 12 (SF12) 4096 chips/symbol are used. Each increase in SF halves the transmission rate and, hence, doubles transmission duration and ultimately energy consumption. Spreading factor can be selected from 6 to 12. SF6, with the highest rate transmission, is a special case and requires special operations. For example, implicit headers are required. Radio communications with different SF are orthogonal to each other and network separation using different SF is possible.

_Bandwidth (BW)_ is the range of frequencies in the transmission band. Higher BW gives a higher data rate (thus shorter time on air), but a lower sensitivity (due to integration of additional noise). A lower BW gives a higher sensitivity, but a lower data rate. Lower BW also requires more accurate crystals (less ppm). Data is send out at a chip rate equal to the bandwidth. So, a bandwidth of 125 kHz corresponds to a chip rate of 125 kcps. The SX1272 has three programmable bandwidth settings: 500 kHz, 250 kHz and 125 kHz. The Semtech SX1272 can be programmed in the range of 7.8 kHz to 500 kHz, though bandwidths lower than 62.5 kHz requires a temperature compensated crystal oscillator (TCXO).

_Coding Rate (CR)_ is the FEC rate used by the LoRa modem and offers protection against bursts of interference. A higher CR offers more protection, but increases time on air.  Radios with different CR (and same CF/SF/BW), can still communicate with each other. CR of the payload is stored in the header of the packet, which is always encoded at 4/8.


