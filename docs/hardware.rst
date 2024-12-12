 
**************** 
Hardware Options
****************

Prior versions
--------------
Based on earlier experiences with the `Polaric Tracker <https://www.la3t.no/polarictracker/>`_ and a `need <http://hamlabs.no/2015/04/01/arctictracker/>`_ for a updated tracker we was thinking of a `possible new design <http://hamlabs.no/2015/04/01/towards-a-next-generation-tracker/>`_ that was based on affordable modules and relatively easy to assemble for radio amateurs. It was also to be able to connect the internet (for config, for uploading tracks, to function as a igate,etc). The first lab-models and the `prototype in the first round <http://hamlabs.no/2019/05/13/first-round-of-tracker-project/>`_ were based on a Teensy-3 microcontroller board, a ESP-8266 and a Nokia display. The role of the ESP was to control the Wifi and provide a simple webserver for configuration of the tracker. It was programmed in LUA (NodeMCU). It had limited memory and barely room for the webserver. The Teensy was more capable and able to encode and decode APRS packets, decode GPS NMEA strings and control the whole thing. 

Arctic Tracker 4 VHF
--------------------

Arctic Tracker 4 UHF/LoRa
-------------------------

LilyGo T-TWR Plus
-----------------
