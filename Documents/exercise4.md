# Exercise 4
 ## node-Red:
 - download node-Red
 - add input node
 - add function node, write toggle function in javascript
 ##### Beispiel:
 ```
	var toggle = context.get('toggle')||0;
	toggle = (toggle + 1)%2;
	context.set('toggle',toggle);

	msg.payload = toggle;

	return msg;
```
(Quelle: ulno)
 - add output node 
 - deploy
 ## MongooseOS
  - connected button to arduino
  - start MongooseOS 
  - select com-port for device
  - select firmware
  - press flash(mos-esp8266-1.18)
  - type in ssid and password
  - start codieng
  - enable MQTT in Device Configuration and add MQTT-Server IP:Port
  - change topic in standard project
  - press save+reboot
  - check with mqtt_all
  
 
