***************
Advanced topics
***************

Arctic Tracker can do more than simple APRS tracking. Here we describe some of the more advanced options like encrypting packets or pushing tracks to a server using a REST API. 

Encryption
----------
Available from version 4.1. 

Sometimes trackers may be used to convey information that is sensitive. It may be information about search-and-rescue missions or persons that shouldn't be exposed for the whole world. Governments may require protection of such information.  It is possible to encrypt APRS position reports when transmitted. This is an *'experimental'* feature using an 'experimental' APRS format. Before using encryption for *HAM-radio transmissions*, please be sure that it is legal in your country. In some countries (Norway) it is legal to encrypt for certain purposes though *not* legal in general.

Encryption is based on AES-256 which is a popular and strong encryption scheme. To be more specific, it is AES-GCM-SIV which also authenticates the packets. It is *symmetric* crypto which means that all participants must have the same key to communicate. This scheme is supported by `Polaric Server <https://aprs.no/polaricserver>`_ and `is documented here <https://polaricserver.readthedocs.io/en/latest/aprs-messages.html#encrypted-aprs-position-reports>`_. It is open-source (free software). Packets encrypted by Arctic Tracker may be decrypted by Polaric Server as long as the key is the same in both ends. 
   
Before activating encryption it necessary to set the key manually. It is generated from a password or passphrase which of course shouldn't be too short or too easy to guess. Use this command to set the key::

   crypto-key <key>

or if the key contains spaces::

   crypto-key "<key>"

To activate encryption for all outgoing APRS position reports use::

   crypto on

To turn it off use::

   crypto off

It is also possible to use the web-interface to control the use of encryption.


Track logging
-------------

Arctic tracker can log positions in memory (e.g. every 10th second) and automatically upload this over the internet to a server (e.g. Polaric Server). The idea is that while the tracker sends updates over radio and this is shown on the map almost immediately, the tracks can be enhanced with more precise info when the tracker is in range of a Wifi network. 

(more info to come.. stay tuned..)
