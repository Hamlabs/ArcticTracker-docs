 
Installing Arctic Tracker firmware
==================================

A quick way to get a tracker up and running is to install a pre-built firmware image. For full control you could build the firmware yourself. It can be useful if you want to modify the code. 

Flashing a pre-built binary
---------------------------
We intend to post pre-compiled binaries with each release and are also available `here <https://arctictracker.no/download/>`_. The complicating factor is that there are more than one way to do it and that the firmware consists of multiple parts: The *bootloader*, the *partition table*, *the webapp*, etc.. 

Download the proper *ArcticTracker.xx.zip* file and unpack it in a directory. Go to that directory and use *esptool* or a similar tool. On Windows, we may use the `flash download tool <https://www.espressif.com/en/support/download/other-tools>`_ from Expressif. The *flash_all.sh* script included in the zip-file shows how to use the *esptool* program. The same parameters can be used in the Windows *flash download tool*. On a Linux system you may just run the *flash_all.sh* script to flash everything. 

You may choose to update only the app (ArcticTracker.bin) or the Webapp (webapp.bin) if you want and if the other parts are in place. Use the the addresses provided. 

OTA Flashing
------------
*OTA flashing* is fully supported from v.4.1 and firmware will be available on arctictracker.no. 

Use the webapp or command shell to set two URLS: One for the firmware and one for the webapp. The OTA install can then be initiated from the tracker (button/display), the webapp or the command shell.

Building the firmware
---------------------
The firmware can be built from source with *esp-idf* (v4.1 is built on version 5.5.x) and the *idf.py* tool. Follow the instructions to install the *esp-idf* and run the necessary scripts there first to set it up. Download the *Arctic Tracker* repository into another directory. cd to this directory and run the following commands to add external components.:: 

  idf.py add-dependency "espressif/mdns^1.2.4" 
  idf.py add-dependency "espressif/led_strip^2.5.3" 

The *led_strip* component is for the LilyGo T-TWR plus (neopixel LED). For this device you will also need to download *XPowersLib* and edit the EXTRA_COMPONENT_DIRS setting in CMakeLists.txt (in the top level directory) to the location where you put it.
  
You may start menuconfig and go to the *Arctic Tracker Config* and check if the right target device is selected. Detailed settings are in *main/defines.h*::
  
  idf.py menuconfig
  
To build the firmware, run::
  
  idf.py build
  
This will build everything. You may flash the firmware directly from idf.py this way. Note that this writes everything to the flash: Including the partition table, a bootloader and the webapp:: 
  
  idf.py flash
  
