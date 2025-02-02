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
**sysinfo**
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
    Show battery status and voltage
**write** <file>
    Write content to file
**rssi**
    Show signal strength. 



Networking commands
-------------------

**ap** [<index> <ssid> [<password>]]
    List or change AP alternatives. Up to 6 alternatives can be specified (index 1-6). 
**ap-auth** [<password>]
    WIFI SoftAP password
**ap-ip** [<ip>]
    WIFI SoftAP IP address
**ap-ssid** [<ssid>]
    WIFI SoftAP SSID setting
**ap-sta**
    Show WIFI SoftAP connected stations
**api-key** [<key>]
    REST API secret key
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
**altitude**
    Altitude setting [on|off]
**comment**
    APRS posreport comment [<text>]
**compress**
    Compress setting [on|off]
**digi**
    Digipeater setting [on|off]
**digipath**
    APRS Digipeater path [<addr>, ...]
**digi-wide1**
    Digipeater fill-in mode (WIDE1) [on|off]
**digi-sar**
    Digipeater preemption on 'SAR' [on|off]
**extraturn**
    Send extra posreport when changing direction [on|off]
**igate**
    Igate setting [on|off]
**igate-host**
    Igate server host [<hostname>]
**igate-port**
    Igate server port [<portnr>]
**igate-user**
    Igate server user [<callsign>]
**igate-pass**
    Igate server passcode [<code>]
**igtrack**
    Send posreports directly to APRS/IS when available [on|off] 
**listen**
    Monitor radio channel for incoming APRS packets
**maxframe**
    APRS max frames in a transmission [<val>]
**maxpause**
    Tracking max pause (10 sec units) [<val>]
**minpause**
    Tracking min pause (10 sec units) [<val>]
**mindist**
    Tracking min distance (meters) [<val>]
**mycall**
    My callsign [<callsign>]
**osymbol**
    APRS symbol for objects (sym-table symbol) [<T><S>]
**objectid**
    ID prefix for object reports <str>
**repeat**
    # Times to repeat posreports (0-3) [val]
**reportbeep**
    Beep when report is sent [on|off]
**statustime**
    Status report time (10 sec units) [<val>]
**symbol**
    APRS symbol (sym-table symbol) [<T><S>]
**testpacket**
    Send test APRS packet (for testing/development)
**timestamp**
    Timestamp setting [on|off]
**tracker**
    APRS tracker setting [on|off]
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
**turnlimit**
    Threshold for change of direction [<val>]
**txmon**
    Tx monitor (show TX packets) [on|off]



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

