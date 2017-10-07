# Lab Exercise 01
Setting up the Raspberry Pi.

- Edit ulnoiot.conf file on the SD card to clone
	- Change username and password (password needs at least 8 characters)
		- username: hainberger_pirklbauer
		- pw: password
	- Change IP-Adress, if not set
- Insert SD card in raspberry PI and connect via WLAN
- Start ssh tunnel via GitBash
	- ssh pi@192.168.12.1 -L 5901:localhost:5901
	- password for ssh: ulnoiot
- choose system 2
- switch to directory of clone script 
	- cd src/rpi-clone
- run clone script
	- sudo ./rpi-clone -v sda
- when prompted for a name, insert "rootfs"
- Insert cloned ssd

- Open VNC viewer (connect via gitbash before that to tunnel)
- Connect via localhost:5901
- type ssh password
- you are now connected

# Blinking

- Start Arduino IDE
- Choose Tool->Board->Wemos D1 R2 & mini
- Choose Tool->Port->usb0
- Choose File->Examples->01Basics->Blinking
- Click Upload Button

File Permission Problem occured here!

- Change permission via ssh with
	- sudo chmod -R 755 /home/pi/apps/arduino
	
# WebServer on Arduino
- Changed WiFi Webserver Example (ssid and password)

Now you can change LED status via Browser:
- to switch on: http://192.168.12.248/gpio/0
- to switch off: http://192.168.12.248/gpio/1

We first tried using the aREST API but it didn't workt out.

- Worked with: Kevin Pirklbauer