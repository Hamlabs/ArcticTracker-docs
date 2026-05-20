***************
Advanced topics
***************

Arctic Tracker can do more than simple APRS tracking. Here we describe some of the more advanced options like encrypting packets or pushing tracks to a server using a REST API. 

Encryption
----------
Sometimes trackers may be used to convey information that is sensitive. It may be information about search-and-rescue missions or persons that shouldn't be exposed for the whole world. Governments may require this.  It is possible to encrypt APRS position reports when transmitted. This is an 'experimental' feature using an 'experimental' APRS format. Before using encryption for HAM-radio transmissions, please be sure that it is legal in your country. In some countries (Norway) it is legal to encrypt for certain purposes.

Encryption is based on AES-256 which is strong encryption scheme. To be more specific, it is AES-GCM-SIV which also authenticates the packets. It is symmetric crypto that requires that all participants have the same key. This scheme is currently supported by Polaric Server and is documented here. It is open-source (free software). Packets encrypted by Arctic Tracker may be decrypted by Polaric Server as long as the key is the same in both ends. 
   

