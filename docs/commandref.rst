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

**rssi**

**tone**

**ptt**

