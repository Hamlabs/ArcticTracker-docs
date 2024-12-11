
Welcome to Arctic Tracker documentation!
========================================

Arctic Tracker is an APRS tracker platform based on the ESP32S3 MCU module, a GPS, a display and a VHF/UHF transceiver module. Hardware prototypes were created mainly as experimental prototypes to show how we can build a tracker using affordable modules. The Arctic Tracker is also a IoT device capable of using WIFI and the internet when this is available: For easy configuration, for pushing APRS data, etc. It can also function as a igate. 

See http://www.hamlabs.no for some blogging about this project.

Main features
-------------

The firmware is implemented in C and based on the ESP-IDF which again is based on FreeRTOS. 
It is fairly complete now. The following features are implemented:

* Command shell running on a serial port (USB). 
* FAT filesystem. 
* Internetworking using WIFI. Automatically connect to access points available. User can set up 
  an ordered list of APs to try. It can also function as its own access point.
* Webserver/REST API.
* OLED display, status screens and menu. Use button to operate.
* Sending and receiving of APRS packets. Tracking, smart beaconing.
* Digipeater and igate. 
* Add highly compressed earlier position reports to packets. This can improve trails significantly.
  See `how this is done here <http://hamlabs.no/2020/11/02/improving-trails-with-arctic-tracker/>`_. 
* Firmware upgrades over the air (OTA).
* Basic information on battery and charging.
* Track logging. Store positions in flash memory e.g. every 5 seconds and upload to a REST
  API on a Polaric Server when network is available. 


Contents
--------

.. toctree::
   
   concepts
   gettingstarted
   config
   interface
