<h1 align="center"> DEDSEC BLUETOOTH EXPLOIT </h1>

<p align="center">
<img src="/image/logo.png" width="50%" height="50%">
</p>

bt_dedsec is a bluetooth hacking device/tool using (esp32 nodemcu and esp-prog) can perform dos attack on any bluetooth device like 
bluetooth speaker,smartphone,IoT device, etc. using BRAKTOOTH exploit

Braktooth is a collection of flaws affecting commercial  bluetooth stacks on more than 1,400 chipsets
used in billions of devices - including smartphones, PCs, toys, speakers, internet of things(Iot) devices
and industrial equipment - that rely on bluetooth Classic (BT) for communication
    
## requirements:
	
	ESP32-devkit v1 nodeMCU                     
	ESP-prog                               
	Jumper wire female-female (8pcs)                     
	Data usb cable                      
	Ubuntu 18.04
	VMWare
	USB 3.0 port 
	
## installation: 
Open VMWare and USB 3.0 enabled. We recommend Ubuntu 18.04
```
1. git clone https://github.com/0xbitx/DEDSEC-Bluetooth-exploit.git
2. cd DEDSEC-Bluetooth-exploit
3. sudo apt install unzip python3-dev
4. unzip bt_dedsec.zip
5. cd bt_dedsec
6. sudo pip install -r requirements
7. connect esp32 nodeMCU via usb cable to your pc
8. sudo esptool.py erase_flash   (boot button maintained) 	
9. connect the esp32 nodemcu and esp-prog
```

<p align="center">
<img src="/image/image-1.png" width="1000%" height="100%">
</p>

## pinout :
```
----------------------------------------
no.	  Esp-prog          Esp32
----------------------------------------		
1.         GND      -       GND
2.	   3.3v       -     3.3v
  	          JTAG
3.	   TMS      -       gpio14
4.	   TCK      -       gpio13
5.	   TDO      -       gpio15
6.	   TDI      -       gpio12
                 SERIAL
7. 	   TX       -       TX
8.	   RX       -       RX
----------------------------------------
```

```
10.  connect esp-prog via usb cable to your pc
11.  cd firmware 
12.  sudo python3 firmware.py flash /dev/ttyUSB1    (check your esp prog path | command: ls /dev/ttyUSB* )
13.  then hold the BOOT button on (esp32 nodemcu) - dont forget to press RESET button afterwards
```
### usage:
```
sudo python3 bt-dedsec.py
```

### help: 
datasheet for [ESP32 NODEMCU](https://cdn.shopify.com/s/files/1/1509/1638/files/ESP_-_32_NodeMCU_Developmentboard_Datenblatt_AZ-Delivery_Vertriebs_GmbH_10f68f6c-a9bb-49c6-a825-07979441739f.pdf?v=1598356497)

datasheet for [ESP32 PROG](https://docs.espressif.com/projects/espressif-esp-iot-solution/en/latest/hw-reference/ESP-Prog_guide.html)


<h1 align="center"> DISCLAIMER </h1>

<h4 align="center">I'm not responsible for anything you do with this program, so please only use it for good and educational purposes. </h4>

