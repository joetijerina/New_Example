# STM32-Hotspot/Menu System Firmware Package, based on STM32CubeWL Release v1.2.0

![latest tag](https://img.shields.io/github/v/tag/STMicroelectronics/STM32CubeWL.svg?color=brightgreen)

## Example

This Hotspot FW package includes:
* Application example under "Projects\NUCLEO-WL55JC\Applications\SubGHz_Phy" called MenuSystem.     
   * This example introduces a Menu Interface for transmitter (and/or receiver) application between two STM32WL55xx devices (note, two NUCLEO-WL55JC1 are needed; for the Tx and Rx, respectively). The Tx device transmits a short 10 byte packet every 2s if in TX_Multiple Radio Mode, and the Rx device receives these packets and displays the payload on the OLED display. 
   * Development tools, toolchains/compilers: STM32CubeIDE v1.8.0
   * Supported Devices and hardware boards: NUCLEO-WL55JC1
   * Known limitations: None

## Hardware and Software Requirements
  * HARDWARE:
	* Two NUCLEO-WL55JC1
      * [NUCLEO-WL55JC](https://www.st.com/en/evaluation-tools/nucleo-wl55jc.html)	  
	* Two Micro-USB cables
	* Two SSD1306 OLED displays
  * SOFTWARE:
	* STM32Cube IDE v1.8 and higher
	* STM32Cube_FW_WL_V1.2.0 Firmware Package
![UG1](Utilities/Media/Images/User_Guide/UG1.jpg)

## Set Up
* Install STM32 CubeEcosystem tools (STM32Cube IDE)
* Download the Menu-System Firmware binary file from STMicroelectronics MFT
* Attach the OLED Displays on the Nucleo-STM32WL55 Boards
* Drag the .bin file onto the Nucleo-STM32WL55 board.
* Do the same for both Nucleo-STM32WL55 Boards with the Firmware
![UG2](Utilities/Media/Images/User_Guide/UG2.jpg)
![UG3](Utilities/Media/Images/User_Guide/UG3.jpg)


## Parameter Summary
* MenuSystem-LoRa
	* We have two boards, one as a transmitter and one as a receiver.
	* We can switch different parameters of LoRa Modulation and start transmitting Custom packet configurations.
		Parameters include:
		* Transmit Power: Values include -9, -4, 0, 4, 9, 14, 22 (dBm)
		* Bandwidth: Values include 125, 250, 500 (kHz)
		* Coding Rate: Values include  1: 4/5, 2: 4/6, 3: 4/7, 4: 4/8
		* Spreading Factor: Values include 5, 6, 7, 8, 9, 10, 11, 12
		* Carrier Frequency: Values include 902.3, 903.9, 905.5, 907.1, 908.7, 910.3, 911.9, 913.5, 914.9 (MHz)
		* Radio Mode: Modes include:
									* TX-Single: Sends one packet every time user presses Switch 1
									* TX-Multiple: Sends multiple packets every 2 seconds, once user presses Switch 1.



* MenuSystem-FSK
	* We have two boards, one as a transmitter and one as a receiver.
	* We can switch different parameters of FSK Modulation and start transmitting Custom packet configurations.
		Parameters include:
		* Deviation Rate: Values include 25k, 50k, 100k
		* Data Rate: Values include 25k, 50k, 100k
		* Bandwidth: Values include 125, 250, 500 (kHz)
		* Preamble Length: Values include  5, 6, 7, 8, 9 
		* Fixed Length: Values include Yes, No 
		* Carrier Frequency: Values include 902.3, 903.9, 905.5, 907.1, 908.7, 910.3, 911.9, 913.5, 914.9 (MHz)
		* Radio Mode: Modes include:
									* TX-Single: Sends one packet every time user presses Switch 1
									* TX-Multiple: Sends multiple packets every 2 seconds, once user presses Switch 1.





## Operation Manual

![UG4](Utilities/Media/Images/User_Guide/UG4.jpg)

## Troubleshooting

**Caution** : Issues and the pull-requests are **not supported** to submit problems or suggestions related to the software delivered in this repository. The STM32WL_SubGHz_Phy_Basic_Tx_Rx example is being delivered as-is, and not necessarily supported by ST.

**For any other question** related to the product, the hardware performance or characteristics, the tools, the environment, you can submit it to the **ST Community** on the STM32 MCUs related [page](https://community.st.com/s/topic/0TO0X000000BSqSWAW/stm32-mcus).

