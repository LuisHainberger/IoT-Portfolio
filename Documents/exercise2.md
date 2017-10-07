# Exercise 2
## Set up IFTTT

- Download IFTT Appllication 
- create a IFTT Webhook 
- define a event and its explaination
 (url to call created Webhook in Webhook settings)
## HTTPrequest template:
- change SSID
- change password
- change host String to maker.iftt.com
- change url String to:"/trigger/button_pressed/with/key/mfVYP1moOYQ7FaHecVCjc07785SLkHjn4GIsf9GQG8b";
- delete client.verify 7
- create a button 
## Button setup
- button pin = 14
- set pinMode to input
- digital read to read button state
- low(0) is pressed button 
## LCD setup
- download liquidchrystal i2c library
- vcc = 5V
- define sda = GPIO4, scl = GPIO5
## Teammembers
- Luis Hainberger
- Kevin Pirklbauer