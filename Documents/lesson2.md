# Lesson 2
# Buses
## Onewire: 
(Manuel Leibetseder)

- similiar concept to I2C
- lower data rates and longer range
- Feature: only use two wires: Data and Ground
- 75 devices can be found per second
- Examples: Java Ring (iButton), Apple MacSafe
- Master can be a PC or microcontroller
- Data include power supply model, wattage, serial number, commands to send full power and illuminate the connector
- Used for communication small inexpensive devices (e.g. digital thermometers/wheater instruments)
- also called MicroLAN
- Maximum Cable Length: 750 Meters
- Different forms (linear, stubbed, star topology)
- Master/Slaves[= 1-Wire-Devices]
- Slaves no longer stubs than three meters in linear topology
- In stubbed topology longer than three meters are possible
- Bus-topolgy up to 300 meters
- Star topology - any length (max 750 meter)
- 220Ohm Pullup resistor for the master
- Slaves are connected to the net
- 150Ohm resistor for the slaves which are connected to the net (reduction of reflections on the line)
- 15 microsec and 54 microsec/data package
- Protocol used: CMOS/TTL
- Supply voltage of 2.8V to 6V
- Sequential data flow in either direction
- serial and bidirectional
- ONLY one direction at a TIME! (half duplex)
- Data read and written = least significant bit first
- 16.3kBit/sec
- Home Automation classic use case

## I²C
(Michael Breiteneder)

Type:
- serial computer bus

Used in:
- lower-speed peripherals ICs to processors and microcontrollers in short-distance, intra-board communication

Data signal:
- Open-drain

Protocol:
- Serial, half-duplex

Bitrate:
- 0.1 / 0.4 / 1.0 / 3.4 / 5.0 Mbit/s

Applications:
- Reading configuration data from SPD EEOPROMs on DIMM memory sticks
- Accessing NVRAM chip that keeps user settings
- Accessing low speed DACs and ADCs
- Changing sound volume in intelligent speakers
- Controlling OLED/LCD displays, like in a cellphone
- Reading real-time clocks
- Turning on and off the power supply of system components.

Operation system support:
- AmigaOS
- Arduino (Wire library)
- Maximite
- PICAXE
- eCos
- ChibiOS/RT
- FreeBSD/NetBSD/OpenBSD
- Linux with specific device driver
- Max OS X
- Microsoft Windows
- Unison OS
- Windows CE
- RISC OS

Design:
- 7-bit or 10-bit address space
- 100 kbit/s standard mode speed
- 10 kbit/s low-speed mode
- 400 kbit/s Fast mode
- 1 Mbit/s Fast mode plus
- 3.4 High speed mode

Pair-Communication same group: (Slava)
- Inventor Phillips
- two lines, one for data (USDA) one for clock (USCL)
- Voltage 5V and 3.3V
- Length restricted to few meters
- Always master and slave 

## Research for SPI:

(Gerhard Wührer)

Serial peripheral interface for synchronous serial communication for short distances and mostly used in embedded systems, Standard from Motorola.
Master-Slave architecture, full-duplex communication using four wires.
•	SCLK: Serial Clock (output from master).
•	MOSI: Master Output Slave Input, or Master Out Slave In (data output from master)
•	MISO: Master Input Slave Output, or Master In Slave Out (data output from slave).
•	SS: Slave Select (often active low, output from master).
Master configures the clock which must be supported from the slave device
The master then selects the slave device with a logic level 0 on the select line. If a waiting period is required, such as for an analog-to-digital conversion, the master must wait for at least that period of time before issuing clock cycles.
Frequency up to a few MHz, limiting also the wire length
Connection of more devices possible
SPI is used to talk to a variety of peripherals, such as:
•	Sensors: temperature, pressure, ADC, touchscreens, video game controllers
•	Control devices: audio codecs, digital potentiometers, DAC
•	Camera lenses: Canon EF lens mount
•	Communications: Ethernet, USB, USART, CAN, IEEE 802.15.4, IEEE 802.11, handheld video games
•	Memory: flash and EEPROM
•	Real-time clocks
•	LCD, sometimes even for managing image data
•	Any MMC or SD card 

## RS232

(Luis Hainberger)

- Standard für serielle Schnittstelle
(eine Datenleitung zwei übertragungsrichtungen )
- Vorschnittstelle von USB
- Übertragung geschieht in Wörtern (bis zu 9 bit/Wort)
- Kodierung ASCII
- Datenübertragung geschieht asynchron
- Geschwindigkeit hängt von UART-Hardware ab
- Mindest Geschwindigkeit ist 1,5 Mbps
- Kabellänge standardmäßig auf 15 m begrenzt
- bei der Verwendung von low capacity Kabeln 300m 


### Anwendungen heute:
 - Service- und Konfigurationsanschlüsse(Router,Switches,...)
 - POS-Terminals (online Terminal zum Bargeldlosen bezahlen)
 
# Sensing/Acting
## Group 2
### Participants
- Michael Breiteneder
- Luis Hainberger
- Gabriel Schützeneder
- Gerhard Wührer

## 1. Smoke Sensor MQ-2
### Luis Hainberger

The Grove - Gas Sensor (MQ2) module is useful for gas leakage detection (home and industry).
It is suitable for detecting
- H2
- LPG
- CO
- Alcohol
- Smoke or Propane

Due to its high sensitivity and fast response time, measurement can be taken as soon as possible.
The sensitivity of the sensor can be adjusted by potentiometer.

The sensor value only reflects the approximated trend of gas concentration in a permissible error range, it does not represent the exact gas concentration. 
The detection of certain components in the air usually requires a more precise and costly instrument, which cannot be done with a single gas sensor.

Featues:
- Wide detecting scope
- Stable and long lifetime
- Fast response and high sensitivity

This is an analog output sensor. It needs to be connected to any one analog socket in Grove Base Shield. 
It is possible to connect the Grove module to Arduino directly by using jumper wires. 
The output voltage from the Gas sensor increases when the concentration of gas increases.

## 2. CO Sensor MQ-7
### Gabriel Schützeneder

- High sensitivity to carbon monoxide
- They are used in gas detecting equipment for carbon monoxide(CO) in family and industry or car. 
- The standard measuring circuit of MQ-7 sensitive components consists of 2 parts. One is heating circuit having time control function (the high voltage and the low voltage work circularly). The second is the signal output circuit, it can accurately respond changes of surface resistance of the sensor. 
- The MQ7 has 6 pins. 4 of them are used to fetch signal and the other two are used for heating current.

## 3. Alcohol-Sensor MQ-3
### Gerhard Wührer

- http://www.learningaboutelectronics.com/Articles/MQ-3-alcohol-sensor-circuit-with-arduino.php

Connections:

- +5V
- DOUT Digital OUT
- AOUT Analog OUT
- GND

Sensor lead analog output AOUT and a digital output DOUT. The higher the analog voltage level the higher the
alcohol the sensor detects. If the analog voltage reaches a certain treshold the DOUT is set to HIGH. This HIGH
can be detected by the arduino.

AOUT is connected to an analog pin of the arduino. With analogRead the alcohol value can be read from the
sensor. DOUT is connected to a digital pin of the arduino. If the digital Read detects a HIGH the alcohol level is to
high and a LED could be triggered to show that the limit is reached.

## 4. Digital Light Sensor TSL2561
### Michael Breiteneder

Details:
- advanced digital light sensor, ideal for use in a wide range of light situations
- more precise than low cost CdS cells
- exact Lux calculations
- different gain/timing ranges
- light ranges 0.1 - 40.000+ Lux
- contains infrared and full spectrum diodes
- seperatly measure infrared, full-sprectrum and human-visible light

Interface:
- digital I2C interface
- select one of three addresses -> up to three sensors on one board each with different I2C address
- built in ADC makes compatible with any microcontroller
- low power usage, great for low power data-logging systems
- 0.5mA when active, less than 15 uA when in powerdown mode

Stats:
- Approximates human eye response
- precisely measure illuminance in diverse lighting conditions
- -30 to 80 °C
- 0.1 to 40.000 Lux
- 2.7-3.6V
- I2C interface

Wiring up the sensor:

- Connect the VCC pin to a 3.3V or 5V power source
- Connect GND to the ground pin
- Connect the i2c SCL clock pin to your i2c clock pin (Classic Arduino -> Analog pin #5)
- Connect the i2c SDA data pin to your i2c data pin (Classic Arduino -> Analog pin #4)
- Dont need to connect the ADDR or INT pins
- ADDR can be used if you have a i2c conflict
- INT pin is an output from the sensor used when the sensor is configured to signal when the light level changes (if used -> 10K to 100K pullup from INT to 3.3V vcc)

Using the sensor:
- Math datasheet http://learn.adafruit.com/tsl2561/downloads
- Arduino library repo on github http://adafru.it/aZ9 and guide http://learn.adafruit.com/adafruit-all-about-arduino-libraries-install-use
- Ardafruit V2 library  https://github.com/adafruit/Adafruit_TSL2561/archive/master.zip
- Adafruit standard library https://github.com/adafruit/Adafruit_Sensor
- Adafruit sensor library https://github.com/adafruit/Adafruit_Sensor/archive/master.zip
- Restart IDE
- Run File>Examples>Adafruit_TSL2561>sensorapi
- Open serial monitor at 9600 baud to see measurements
 
 
 
