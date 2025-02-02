Command Reference
=================

System commands
---------------

**trk-reset** 
    Reset track storage

**ls**
    List files in filesystem

**mkdir** <path>
     Create a new directory

**rm** <file>
    Remove file

**cd** <directory>
    Change working directory

**format** 
    Reformat file system. 

**write** <file>
    Write content to file

**read** <file>
    Read content from file

**free**
    Show amount of free memory (in bytes)

**sysinfo**
    Show system information. 

**restart** 
    Restart the system

**tasks**
    Show list of tasks running in system (threads/processes)

**log** <tag> | * [<level>]
    Set loglevel (for debugging/testing)

**time**
    Show time (UTC and local-time if timezone is set)

**timezone** <tz-string>
    Set timezone. Use tz-string format to specify timezone information. 

**nmea** [raw]
    Show NMEA data stream from GNSS. Use 'raw' switch to indicate that all data is to be shown. Otherwise only 
    fixed data will be shown. 

**vbatt**
    Show battery status and voltage

**ioconfig** <gpio-num>
    Show info on GPIO configuration (for developing/debugging)

**fw-uprade**
    OTA Firmware upgrade

**rssi**
    Show signal strength. 

**tone**
    Tone generator test. 

**ptt**
    Transmitter on

Networking commands
-------------------
**mdns**  <type>
    Scan for MDNS services

**wifi-scan**
    Scan for access points

**wifi-info**
    Info about Wifi connection

**wifi** [on|off]
    Wifi on/off setting

**softap** [on|off]
    Wifi softap on/off setting

**ap** [<index> <ssid> [<password>]]
    List or change AP alternatives. Up to 6 alternatives can be specified (index 1-6). 

**ap-ssid** [<ssid>]
    WIFI SoftAP SSID setting

**ap-auth** [<password>]
    WIFI SoftAP password

**ap-ip** [<ip>]
    WIFI SoftAP IP address

**ap-sta**
    Show WIFI SoftAP connected stations

**api-key** [<key>]
    REST API secret key

**api-origins** [<regex>]
    Allowed origins for REST API webclients. Default is to allow all.

**fw-url** [<url>]
    URL for OTA firmware update

**fw-cert**
    Certificate for firmware update. Use only if you use a self-signed certificate

**connect** <host> <port>
    Connect to internet server (like telnet). Use for testing/debugging.

