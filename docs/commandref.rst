Command Reference
=================

System commands
---------------
**cd** <directory>
    Change working directory
**format** 
    Reformat file system. 
**free**
    Show amount of free memory (in bytes)
**fw-uprade**
    OTA Firmware upgrade
**ioconfig** <gpio-num>
    Show info on GPIO configuration (for developing/debugging)
**trk-reset** 
    Reset track storage
**ls**
    List files in filesystem
**log** <tag> | * [<level>]
    Set loglevel (for debugging/testing)
**mkdir** <path>
     Create a new directory
**nmea** [raw]
    Show NMEA data stream from GNSS. Use 'raw' switch to indicate that all data is to be shown. Otherwise only 
    fixed data will be shown. 
**rm** <file>
    Remove file
**read** <file>
    Read content from file
**sysinfo**.
    Show system information. 
**restart** 
    Restart the system
**tasks**
    Show list of tasks running in system (threads/processes)
**time**
    Show time (UTC and local-time if timezone is set)
**timezone** <tz-string>
    Set timezone. Use tz-string format to specify timezone information. 
**vbatt**
    Show battery status and voltage.
**write** <file>
    Write content to file
**rssi**
    Show signal strength on radio receiver. 



Networking commands
-------------------

**ap** [<index> <ssid> [<password>]]
    List or change AP alternatives. Up to 6 alternatives can be specified (index 1-6). 
**ap-auth** [<password>]
    WIFI SoftAP password.
**ap-ip** [<ip>]
    WIFI SoftAP IP address. Default is 192.168.0.1. 
**ap-ssid** [<ssid>]
    WIFI SoftAP SSID setting. Default is 'Arctic_XXXX' where XXXX is mycall. Should work in most cases.
**ap-sta**
    Show WIFI SoftAP connected stations
**api-key** [<key>]
    REST API secret key. 
**api-origins** [<regex>]
    Allowed origins for REST API webclients. Default is to allow all.
**connect** <host> <port>
    Connect to internet server (like telnet). Use for testing/debugging.
**fw-cert**
    Certificate for firmware update. Use only if you use a self-signed certificate
**fw-url** [<url>]
    URL for OTA firmware update
**mdns**  <type>
    Scan for MDNS services
**softap** [on|off]
    Wifi softap on/off setting
**wifi** [on|off]
    Wifi on/off setting
**wifi-info**
    Info about Wifi connection
**wifi-scan**
    Scan for access points


APRS tracking commands
----------------------
**altitude** [on|off]
    Altitude setting 
**comment**  [<text>]
    APRS posreport comment
**compress** [on|off]
    Compress setting 
**digi**  [on|off]
    Digipeater setting
**digipath**  [<addr>, ...]
    APRS Digipeater path
**digi-wide1** [on|off]
    Digipeater fill-in mode (WIDE1)
**digi-sar**  [on|off]
    Digipeater preemption on 'SAR'
**extraturn**  [on|off]
    Send extra posreport when changing direction
**igate** [on|off]
    Igate setting 
**igate-host** [<hostname>]
    Igate server host
**igate-port**  [<portnr>]
    Igate server port
**igate-user**  [<callsign>]
    Igate server user
**igate-pass** [<code>]
    Igate server passcode 
**igtrack** [on|off]
    Send posreports directly to APRS/IS when available  
**listen**
    Monitor radio channel for incoming APRS packets
**maxframe** [<val>]
    APRS max frames in a transmission 
**maxpause** [<val>]
    Tracking max pause (10 sec units) 
**minpause** [<val>]
    Tracking min pause (10 sec units) 
**mindist** [<val>]
    Tracking min distance (meters) 
**mycall** [<callsign>]
    My callsign 
**osymbol** [<T><S>]
    APRS symbol for objects (sym-table symbol) 
**objectid** <str>
    ID prefix for object reports 
**repeat**  [val]
    # Times to repeat posreports (0-3)
**reportbeep** [on|off] 
    Beep when report is sent 
**statustime** [<val>]
    Status report time (10 sec units)
**symbol** [<T><S>]
    APRS symbol (sym-table symbol) 
**testpacket**
    Send test APRS packet (for testing/development)
**timestamp** [on|off]
    Timestamp setting 
**tracker**  [on|off]
    APRS tracker setting
**turnlimit** [<val>]
    Threshold for change of direction 
**txmon** [on|off]
    Tx monitor (show TX packets) 

Track logging commands
----------------------
The tracker can store position-reports in the file-system and upload them to a Polaric Server instance when internet is in range. Commands related to track-logging are: 

**tracklog**
    Track logging [on|off]
**trklog-get**
    Get tracklog record (for testing/development)
**trklog-put**
    Put tracklog record (for testing/development)
**trklog-int**
     Interval for track logging (seconds) [<val>]
**trklog-post**
    Track log automatic post to server [on|off]
**trklog-ttl**
     Max time to keep tracklog entries (hours) [<val>]
**trklog-key**
    KEY for authenticating tracklog-messages to Polaric Server [<key>]
**trklog-url**
    URL for posting tracklog updates to Polaric Server [<url>]



AFSK APRS radio commands
------------------------

**ptt**
    Transmitter on
**radio**
     Radio module power [on|off]
**rxfreq**
    RX frequency (100 Hz units) [<val>]
**softsq**
    Soft Squelch setting [<val>]
**squelch**
    Squelch setting (1-8) [<val>]
**teston**
    HDLC encoder test <byte> 
**tone**
    Tone generator test. Use space to cycle between 1200 and 2200 Hz
**txdelay**
    APRS TXDELAY setting [<val>]
**txfreq**
    TX frequency (100 Hz units) [<val>]
**txlow**
    Tx power low [on|off]
**txtail**
    APRS TXTAIL setting [<val>]
**volume**
    RX audio level setting (1-8) [<val>]


LoRa APRS radio commands
------------------------
**freq**
    TX/RX frequency (Hz) [<val>]
**heard**
     Last heard packet
**lora-cr**
    LoRa coding rate (5-8) [<val>]
**lora-sf**
    LoRa spreading factor (7-12) [<val>]
**txpower**
    Tx power (1-6) [<val>]

