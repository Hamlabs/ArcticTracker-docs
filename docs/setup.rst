 
Basic setup
===========

Initial setup - using the command shell
---------------------------------------
The Arctic Tracker offers a serial console (command shell). This lets you control every setting and has some commands for testing, debugging, etc. It is a useful tool when developing. It is recommended to use it the first time you start the tracker for setting the wifi access point and access-key. When you plug in a USB-C cable and connect it to your computer a serial interface should appear (on Linux it is /dev/ttyACM0). A good old serial terminal program will probably work. The monitor command of idf.py (if you have the esp-idf installed), should also work. You may need to reset the tracker to get up the command prompt (cmd>). 

.. image:: img/console.png

The ‘help‘ command gives you a list of available commands. ‘help <command>‘ gives a short explanation of the given command. Be sure to set the callsign (‘mycall‘). The ‘tracker’ command turns on or off the tracking function (it is on by default). ‘radio on’ command turns on the radio. The ‘wifi on’ command turns on the WIFI. The ‘ap’ command lets you set up a list of WIFI access points. The tracker will try to connect to these in order if they are in range. If the first one fails, it will try the next. Also, before you try to use the webapp, use the ‘api-key’ to set a secret key to be used for the webapp to authenticate. If things are working as expected, you should also be able to get to the most important settings with a web-browser.

It is also possible to do the initial configuration by activating the softap (can be done by activating the menu on the display by pushing the button and holdning it one second). Go to the menu-item that says Softap on and push the button to confirm. 

Configuring the Wifi
--------------------

Using the Web App
-----------------

