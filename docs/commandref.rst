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


APRS and radio commands
-----------------------

**listen**
    Monitor radio channel
**trklog-get**
    Get tracklog record
**trklog-put**
    Put tracklog record
**mycall**
    My callsign [<callsign>]
**digipath**
    APRS Digipeater path [<addr>, ...]
**symbol**
    APRS symbol (sym-table symbol) [<T><S>]
**osymbol**
    APRS symbol for objects (sym-table symbol) [<T><S>]
**objectid**
    ID prefix for object reports <str>
**comment**
    APRS posreport comment [<text>]
**repeat**
    # Times to repeat posreports (0-3) [val]
**trklog-int**
     Interval for track logging (seconds) [<val>]
**trklog-ttl**
     Max time to keep tracklog entries (hours) [<val>]
**trklog-key**
    KEY for authenticating tracklog-messages to Polaric Server [<key>]
**trklog-url**
    URL for posting tracklog updates to Polaric Server [<url>]
**maxframe**
    APRS max frames in a transmission [<val>]
**maxpause**
    Tracking max pause (10 sec units) [<val>]
**minpause**
    Tracking min pause (10 sec units) [<val>]
**mindist**
    Tracking min distance (meters) [<val>]
**statustime**
    Status report time (10 sec units) [<val>]
**turnlimit**
    Threshold for change of direction [<val>]
**timestamp**
    Timestamp setting [on|off]
**compress**
    Compress setting [on|off]
**altitude**
    Altitude setting [on|off]
**digi**
    Digipeater setting [on|off]
**igate**
    Igate setting [on|off]
**digi-wide1**
    Digipeater fill-in mode (WIDE1) [on|off]
**digi-sar**
    Digipeater preemption on 'SAR' [on|off]
**igate-host**
    Igate server host [<hostname>]
**igate-port**
    Igate server port [<portnr>]
**igate-user**
    Igate server user [<callsign>]
**igate-pass**
    Igate server passcode [<code>]
**tracklog**
    Track logging [on|off]
**trklog-post**
    Track log automatic post to server [on|off]
**radio**
     Radio module power [on|off]
**tracker**
    APRS tracker setting [on|off]
**reportbeep**
    Beep when report is sent [on|off]
**extraturn**
    Send extra posreport when changing direction [on|off]
**igtrack**
    Send posreports directly to APRS/IS when available [on|off] 
**txmon**
    Tx monitor (show TX packets) [on|off]
**testpacket**
    Send test APRS packet

**teston**
    HDLC encoder test <byte> 
**txdelay**
    APRS TXDELAY setting [<val>]
**txtail**
    APRS TXTAIL setting [<val>]
**squelch**
    Squelch setting (1-8) [<val>]
**softsq**
    Soft Squelch setting [<val>]
**volume**
    RX audio level setting (1-8) [<val>]
**txlow**
    Tx power low [on|off]
**txfreq**
    TX frequency (100 Hz units) [<val>]
**rxfreq**
    RX frequency (100 Hz units) [<val>]

**lora-sf**
    LoRa spreading factor (7-12) [<val>]
**lora-cr**
    LoRa coding rate (5-8) [<val>]
**txpower**
    Tx power (1-6) [<val>]
**freq**
    TX/RX frequency (Hz) [<val>]
**heard**
     Last heard packet
