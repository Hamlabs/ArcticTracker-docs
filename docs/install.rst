 
Installing Arctic Tracker firmware
==================================

A quick way to get a tracker up and running is to install a pre-built firmware image. For full control you could build the firmware yourself. It can be useful if you want to modify the code or if you for maximum security want to generate a SSL-certificate specifically for your firmware and keep the private key secret. 

Building the firmware
---------------------
The firmware can be built from source with *esp-idf* (version 5.0.x) and the *idf.py* tool. Follow the instructions to install the *esp-idf* and run the necessary scripts there first to set it up. Download the *Arctic Tracker* repository into another directory. cd to this directory and run the following commands to add external components.:: 

  idf.py add-dependency "espressif/mdns^1.2.4" 
  idf.py add-dependency "espressif/led_strip^2.5.3" 

The *led_strip* component is for the LilyGo T-TWR plus (neopixel LED). For this device you will also need to download *XPowersLib* and edit the EXTRA_COMPONENT_DIRS setting in CMakeLists.txt (in the top level directory) to the location where you put it.

A self-signed certificate is included to support encrypted connections to the the web-app. It is a good idea to generate a new key-pair and SSL certificate now and then. You could also just cd to the directory and run the command inside the *gencert.sh* script. You should have *openssl* installed on your computer to do this:: 
  
  cd components/networking/cert; sh gencert.sh
  
You may start menuconfig and go to the *Arctic Tracker Config* and check if the right target device is selected. Detailed settings are in *main/defines.h*::
  
  idf.py menuconfig
  
To build the firmware, run::
  
  idf.py build
  
This will build everything. You may flash the firmware directly from idf.py this way. Note that this writes everything to the flash: Including the partition table, a bootloader and the webapp:: 
  
  idf.py flash
  
