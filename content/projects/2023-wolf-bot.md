+++
title = "Wolf Bot"
date = 2023-01-01
template = "post.html"
draft = false

[extra]
description = "User-controlled robot with ESP32 controller, tank drive system, and IR laser weapon capabilities for gaming applications"
+++

# Wolf Bot

[repo](https://github.com/dj-ryan/wolf-bot)

# Fall Week 4
## Wolf Bot
### Overview
This is the main user controlled robot that will participate in the game. It will have a reliability simple drive system with two modes of communication. The first mode of communication will be for user input direction control the other for API based post requests given to the BFCM. Both signals will be around 2.4Ghz radio. 

### Micro-controller
The main brains of the Wolf Bot will be a ESP32 controller. We are planning on using the Adafruit HUZZAH32 version. This is a powerful 160 MHz dual-core CPU with  320 KiB RAM, 448 KiB ROM. It also contains a 2.4 GHz WiFi antenna with a speed up to 150 Mbps. This is what we will use to communicate with the BFCM.  Using the Adafruit feather version gives us access to several "wings" like the 128x64 OLED display that would allow us to incorporate a useful information display directly into the robot. 


### Drive system
The drive system will consist of a tank trade base. It will be powered by two brushed 12v DC motors. A future design may include more advanced motors such ESC brush-less motors (These will be more expensive). The base we have chosen to start with is [Project Design](/projects/project-design/) aluminum frame with plastic gears and treads. It does not include any form of suspension. 

The tank design will serve two purposes:
1) In general a tank drive system is more fun to drive giving the user more enjoyment
2) The treads will allow a diverse set of terrains to be conquered (including, possibly, just maybe, astro-turf)

### Power management
The power supply for the bot will consist of a 12V 6000mAh battery pack. The output will feed the L298N motor controller as well as a 5v regulator that will intern power the micro-controller.  Eventually a power supply would be beneficial to regulate the choppy output of the battery pack. 

### IR Laser Weapon
This portion of the Bot has not been flushed out

### Damage Detection Sensor Array
This portion of the Bot has not been flushed out


## User Controller
The controller will be an Arduino Uno R3 with a Nokia 5110  joystick and  button shield attached to it. Also attached to it will be a NFR24l01 radio module that will communicate with a twin modal on the Wolf Bot. It will be powered by a small 5V 1A power pack. The whole device will be a dense handheld device with almost instantaneous boot up and control capabilities. 


### Unknowns
- Nailing down how we make sure that there is no frequency interference between systems.

---

# Fall Week 5
Spent Tuesday gathering data for IR accuracy. This included developing a test workbench with two MCs. One dedicated to gathering and printing IR data and the other responsible for transmitting a known set of IR codes.

Several experiments were conducted with different angles and distances to transmit an IR signal. A pin-point 780nm 3mw laser was used with a generic 3v IR receiver. 

Over the weekend I wrote code to send raw hexadecimal data over IR in the NEC format. This will give us complete control over what data is being sent and not having to rely on the IRremote Library. However writing it in the NEC protocol will allow us to have better accuracy and reliability in transmission as we can have the receiver still rely on the IRremote library. 

---

# Fall Week 6

## TODO
- [x] Regular IR LED
	- [x] Spread angle
	- [x] Distance
- [x] Pin point IR LED
	- [x] Spread angle
	- [x] Distance
- [x] Regular IR LED in cone
	- [x] Spread angle
	- [x] Distance
- [x] Wavelength
	- [x] IR
	- [x] Transmitter
- [x] IR receiver
	- [x] Field of view
- [x] Turning rate of the car
	- [x] How far the car has to move forward to turn 90 & 180 degrees
	- [x] Do an analysis of the turn radius of the RC car. (Maybe look into tank style tracks for RC car)
- [x] Documented NEC protocol
- [x] Make an actual diagram of the IR laser mount in the RC car

## Summary
The main goal for this week was to gather information on how our IR components preformed on in terms of FOV and range. The data is presented below. Also some clarifications needed to be made on technical specifications of components which has also been provided. As well as a detailed explanation with code examples of How the NEC protocol works. 

## IR transmitter testing data
|                                      | FOV (deg) | Max Distance (ft) | Notes               |
| ------------------------------------ | --- | ------------ | ------------------- |
| Filtered IR LED                      | 23*  | 10ft         |                     |
| Filtered IR LED w/ cone              | 5*  | 5ft          |                     |
| Filtered IR LED w/ cone and Diffuser |     |              | No consistent data  |
| Raw IR LED w/ cone                   | 30* | 3ft          | Inconsistent beyond 3ft |
| Pinpoint IR LED                      | 6*  | 3ft          |                     |
| Pinpoint IR LED w/o optics           | 1*    | 2ft             |                     |

## Datasheets
### ESP32 TTGO
![ESP32 PINOU](https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/61U7dm3G3ZL._AC_SX679_.jpg)

#### Hardware Specifications:
Chipset: ESPRESSIF-ESP32 240MHz Xtensa single-/dual-core 32-bit LX6 microprocessor
FLASH: QSPI flash 4MB
SRAM: 520 kB SRAM
Button: Reset
USB to TTL: CH9102
Modular interface: UART, SPI, SDIO, I2C, LED PWM, TV PWM, I2S, IRGPIO, ADC, capacitor touch sensor, DACLNA pre-amplifier
Display: IPS ST7789V 1.14 Inch
Working voltage: 2.7V-4.2V
Working current: About 60MA
Sleep current: About 120uA
Working temperature range: -40°C ~ +85°C