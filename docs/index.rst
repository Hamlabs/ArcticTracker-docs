
Welcome to Arctic Tracker documentation!
========================================

Arctic Tracker is an APRS tracker platform based on the ESP32S3 MCU module, a GPS, a display and a VHF/UHF transceiver module. Hardware prototypes were created mainly as experimental prototypes to show how we can build a tracker using affordable modules. The Arctic Tracker is also a IoT device capable of using WIFI and the internet when this is available: For easy configuration, for pushing APRS data, etc. It can also function as a igate. 

See http://www.hamlabs.no for some blogging about this project and on the `port to the T-TWR <http://hamlabs.no/2024/03/22/arctic-tracker-software-on-lilygo-t-twr-plus/>`_ in particular.


Main features
-------------

* Based on free and Open Source software. Open REST API for interoperability.

* The user interface is a web application which allows users to browse maps, view and manipulate real-time tracking information using a standard web browser.

* Authorized users can, on the server, add information (including APRS objects) and manipulate how objects are displayed in a view shared by all users. For example choice of icons, use descriptive labels (tactical callsigns), tagging, hiding of unnecessary information, etc..

* It can integrate live tracking information from various sources in addition to APRS. Examples include AIS and Datex II.

* With the client, it is a GIS software that can use many open raster layer sources like e.g. WMS, WMTS, Google Maps or OpenStreetmap. It supports caching/storage of map tiles on server for offline use. It supports vector sources like WFS as well, and file formats like GPX or GeoJSON. It can seamlessly switch between multiple map projections.

* Support for drawing features directly on the map. Support for drawing distance circles (bike wheel model).

* To help dealing with information overload, servers can be set up with programmable filters and automatic tagging (sysadm can set up rules) to configure what items are displayed as well as how the items are displayed. For example we have full control over trail-lengths, use of labels, etc. Users can select from a set of predefined filters.

* Support for APRS messages and bulletins. Support for APRS telemetry (can show graphs)

* Can be set up with multiple server instances that can synchronize labels, tags, etc using authenticated APRS messages. Can operate offline with cached map-data. Suitable for small devices like e.g. Raspberry PI and mobile use.

* Supports role-based authorization of users. Highly configurable what groups of users may see and do.

* Plugin with database support (PostgreSQL with GIS extension) for safe storage of important information and storage and retrieval of tracking (trails) from the past. Useful for looking up information about past missions. Database plugin also supports (eventual consistency) synchronisation of some data with other server instances.


Some of its use is discussed in `this book chapter <https://doi.org/10.5772/intechopen.75371>`_ and `ISCRAM 2015 paper <http://idl.iscram.org/files/oyvindhanssen/2015/1211_OyvindHanssen2015.pdf>`_ and `ISCRAM 2021 paper <http://idl.iscram.org/files/oyvindhanssen/2021/2350_OyvindHanssen2021.pdf>`_. 

Copyright and license
---------------------

Polaric Server is free software. See GNU General Public License v.2 and GNU AGPL v.3) Some parts of the source code may use compatible licenses like BSD. Copyright is owned by the respective authors of the software. We also encourage crediting the radio amateur (HAM) community and the Norwegian Radio Relay League for deveopment of APRS technology. If used for a publicly available online service and you make improvements or additions we encourage you to publish these improvements as open source. “APRS” is a registered trademark of Bob Bruninga.

Contents
--------

.. toctree::
   
   concepts
   gettingstarted
   config
   interface
