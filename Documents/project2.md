# Project 2

## connect time of light sensor to arduino (5V)
- use library from: https://learn.adafruit.com/adafruit-vl53l0x-micro-lidar-distance-sensor-breakout/wiring-and-test
- run example on arduino and get distance in mm
##  connect HC-SR04 to arduino
- use library from: https://github.com/ErickSimoes/Ultrasonic
- change pins to 4(trig)and 5(echo)
- run example on arduino and get distance in cm

##  connect rain drop sensor to arduino
- use code from: http://henrysbench.capnfatz.com/henrys-bench/arduino-sensors-and-input/arduino-rain-sensor-module-guide-and-tutorial/
- set pins and baudrate
 ## connect scale with usb
 - use library from: https://github.com/bogde/HX711
 - set scale factor 453000 (for kg) or 453 (for g) 
 - set pins to 9,10 with scale.begin()
 - tools-> arduino/genoiono uno
 ## connect reed switch to arduino
 - use code sample from: https://learn.sparkfun.com/tutorials/reed-switch-hookup-guide
 - connect sig to d2 port
 - change baudrate
 - change REED_PIN to 4
 - test it with a magnetic floater 
 
 
<html>
<head>
<style>
table, th, td {
    border: 1px solid black;
}
</style>
</head>
<body>

<table style="width:100%">
  <tr>
  <th></th>
    <th>Laser</th>
    <th>Ultrasonic </th> 
    <th>Raindrop</th>
  </tr>
  <tr>
    <td>Water (7cm)</td>
    <td>7-9</td>
    <td>7-8</td>
	<td>270 - 320</td>
	
  </tr>
  <tr>
    <td>Water(2cm)</td>
    <td>2-4</td>
    <td>2-3</td>
	
  </tr>
  <tr>
    <td>Dirty Water(5cm)</td>
    <td>5-6</td>
    <td>5-6</td>
	<td>230 - 250</td>
  </tr>
  <tr>
    <td>Dirty Water(1cm)</td>
    <td>1-2</td>
    <td>1-2</td>
	
  </tr>
  <tr>
    <td>Oil(7cm)</td>
    <td>7-8</td>
    <td>7-8</td>
	<td>970 - 990</td>
  </tr>
  <tr>
    <td>Oil(3cm)</td>
    <td>3-4</td>
    <td>3-4</td>
  </tr>
  </tr>
  
  
  
  
  # Scale test:
  
 <html>
<head>
<style>
table, th, td {
    border: 1px solid black;
}


</style>
</head>
<body>

<table style="width:100%">
  <tr>
    <th></th>
    <th>Scale</th> 
    
  </tr>
  <tr>
    <td>Water (1l)</td>
    <td>9973g</td>
   
  </tr>
  <tr>
    <td>Dirty Water (1l)</td>
    <td>9971g</td>
    
  </tr>
  <tr>
    <td>Oil (1/4l)</td>
    <td>212g</td>
   
  </tr>
</table>

</body>
</html>
 
  
</table>

</body>
</html>
 
 
 
 


