# ex8
- activate spi with: sudo raspi-config
- check legacy...
- pi@raspberrypi:~$ wget https://github.com/tftelkamp/single_chan_pkt_fwd/archive/master.zip
- pi@raspberrypi:~$ unzip master.zip
- pi@raspberrypi:~$ cd single_chan_pkt_fwd-master/
- open main.cpp
- change #define SERVER1 "54.72.145.119" to "52.169.76.203"
- pi@raspberrypi:~$ make
- pi@raspberrypi:~/single_chan_pkt_fwd-master$ sudo ./single_chan_pkt_fwd 
- Create TTN account
- Choose Console to enter the TTN console page
- define Gateway ID: iot_hagenberg1
- define router 


