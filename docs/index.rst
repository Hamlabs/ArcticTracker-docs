
Welcome to Arctic Tracker documentation!
========================================

Arctic Tracker is an APRS tracker platform based on the ESP32S3 MCU module, a GPS, a display and a VHF/UHF transceiver module. Hardware prototypes were created mainly as experimental prototypes to show how we can build a tracker using affordable modules. The Arctic Tracker is also a IoT device capable of using WIFI and the internet when this is available: For easy configuration, for pushing APRS data, etc. It can also function as a igate. 

Main features
-------------

The firmware is implemented in C and based on the ESP-IDF which again is based on FreeRTOS. 
Many features are fairly complete now. The following features are implemented:

* Command shell running on a serial port (USB). This allows settings of various parameters, using persistent storage (flash).
* FAT filesystem. 
* Internetworking using WIFI. Automatically connect to access points available. User can set up 
  an ordered list of APs to try. It can also function as its own access point.
* Webserver/REST API. Secured using TLS and HMAC based authentication.
* Interface with GPS for position and time. 
* OLED display, status screens and menu. Use button to operate.
* Sending and receiving of APRS packets. Tracking, smart beaconing.
* Encryption of APRS packets.
* Add highly compressed earlier position reports to packets. This can improve trails significantly.
  See `how this is done here <https://github.com/Hamlabs/ArcticTracker-ESP32>`_. 
* Digipeater and igate.
* Automatic management and information on battery and charging.
* Track logging. Store positions in flash memory e.g. every 5 seconds and upload to a REST
  API on a Polaric Server when network is available. 
* LoRa APRS (on supported hardware)
* Firmware upgrades over the air (OTA)


Contents
--------

.. toctree::

   hardware
   gettingstarted
   advanced
   commandref
