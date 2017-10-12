# Exercise 3
## COAP
- download simple COAP library at: https://github.com/automote/ESP-CoAP
- add library to libraries folder of arduino studio
- change password, ssid
- change pins in callback_light method to pin 2
- install copper plugin
- chose discovery on copper to show methods of ESP-CoAP
- chose light method
- chose a payload in outgoing tab to turn off(1) and turn on(0) the arduino led(pin is 2)  
- press post
## MQTT
 - download MQTT.fx(mqtt browser)
 - create a mqtt java client or use https://github.com/eclipse/paho.mqtt.java
 - create Mqtt client
 - connect client to Server
 - client has to publish data
 - mqtt.fx has to subscribe the clients message
 - create a sensor class, which simulates temperature values in seperate thread, publish these values to broker
 - create a switch class, which subscribes the integrator in a seperate thread
 - create a integrator class which publishes a message(on/off) when a specific temperature is reached
 
 ### Problems:
  - We had to install Firefox version FF55 because the copper plugin is not compatible with a newer version of Firefox
 








