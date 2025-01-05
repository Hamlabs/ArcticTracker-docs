 
Basic setup and use
===================

For first-time setup it is recommended to use the *command shell* (console) as described below. Alternatively, it is possible to activate the soft-AP (use the tracker as an access point) and use the web-app to access the most important settings. It is probably easier to use the web-app after the callsign is set since the callsign is part of the identifier for the tracker. 

Using the command shell
-----------------------
The Arctic Tracker offers a serial console (command shell).  This lets you control every setting and has some commands for testing,  debugging, etc. It is recommended  to use it the first time you start the tracker for setting the wifi  access point, access-key, etc. When you plug in a USB-C cable and connect it to your computer a serial interface should appear. On Linux it is typically */dev/ttyACM0*. On Windows, you can see in the device-manager what COM-port it is mapped to. It is usually *COM3*. A good old serial terminal program (VT102 mode is preferable) should work. On Linux, *Minicom* works well. On Windows, *Putty* is recommended. The monitor command of *idf.py* (if you have the esp-idf installed), should also work. You may need to reset the tracker to get up the command prompt (*cmd>*). 

.. image:: img/console.png

The ‘help‘ command gives you a list of available commands. ‘help <command>‘ gives a short explanation of the given command. Be sure to set the callsign (‘mycall‘). The ‘tracker’ command turns on or off the tracking function (it is on by default). ‘radio’ command turns on or off the radio (it is on by default). The ‘wifi on’ command turns on the WIFI. The ‘ap’ command lets you set up a list of WIFI access points. The tracker will try to connect to these in order if they are in range. If the first one fails, it will try the next. Also, before you try to use the webapp, use the ‘api-key’ to set a secret key to be used for the webapp to authenticate. If things are working as expected, you should also be able to get to the most important settings with a web-browser.

﻿﻿The 'digipath' (digipeater path) is by default set to 'WIDE1-1', if you need to use multi-hop digipeating it could be set to '"WIDE1-1,WIDE2-2'. 'timestamp' (timestamped packets) and 'compress' (compressed packets) are also on by default. 'symbol' (aprs symtable/overlay and symbol) is by default set to'/[' which means a running person is to be shown on the map.
 
Connecting to a Wifi access point
---------------------------------
The first time the tracker is used, you could use the 'ap' command to set the access-point to use.::

  ap 1 <ssid> <key>

Up to 6 alternative access-points can be given. First index is 1. The first one will be tried first, if that fails, it will try the next, etc. When you turn on the wifi it should try to connect to the access point. Use the 'wifi-info' to see if it succeeds to connect, what IP-address it gets, etc.. 

The web-app can also be used to edit the list of access points, the keys, etc.. 

Using the Web App
-----------------
The tracker can be configured using a `web-app <https://github.com/Hamlabs/ArcticTracker-Webapp>`_. It can discover and connect to trackers on the same LAN and it can connect to several trackers at the same time. The first time you connect to a tracker, start the webapp from the tracker itself: Point the browser to 'https://arctic-XXXX.local/' where XXXX is the callsign you gave the tracker. If a callsign is not set, the id of the ESP32 chip will be used. You can also see the hostname on the display or when using the 'wifi-info' command. 

The first time you are opening the webpage on the tracker this way, the browser will complain that its certificate cannot be verified. This is because it is a self-signed certificate and not signed by a known CA. If you feel confident that you are really connecting to your tracker you can add an exception to the browser to let it accept the webpage. Later connections to the same tracker will then work, even if the webapp is coming from somewhere else. 

Now, add the tracker. Click on the lock-icon and fill inn the callsign field and click 'add'. Now, the callsign should appear in a little box on the screen. The first time you access the tracker you also need to add the API-key. On the tracker, this key can be set in the command-shell ('api-key' command) or in the web-app itself. By default it is '123456789'. Please change it at your first convenience. If the correct key is set and we have connected sucessfully to the tracker, the box with the callsign will turn green. 

If at least one tracker is connected it will automatically discover other trackers on the LAN (using mDNS). To connect to them, click the callsign-box and (if not added earlier) add the API-key. 

The web-app has a menu with 5 choices: 

* *Status* - show info on tracker
* *Wifi* - configure Wifi access points, Wifi Soft AP and keys. 
* *Aprs* - Configure callsign, radio frequency, APRS confg like symbol, path, etc..
* *Digi/Igate* - Digipeater and igate setup. 
* *TrkLog* - Track logging setup. Automatic uploading of tracks to a Polaric Server instance.

In addition you can select and set up connections to trackers. 




Using the Soft AP
-----------------



