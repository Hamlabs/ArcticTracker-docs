
Current Arctic Tracker hardware
===============================

The current Arctic Tracker hardware is available in two versions: a VHF
tracker for AFSK APRS and a UHF tracker for LoRa APRS. Both are compact,
ESP32-S3-based trackers with GNSS, a display, Wi-Fi, and a rechargeable
battery. They run the Arctic Tracker firmware and can be configured through
the USB command shell or over Wi-Fi.

Arctic Tracker 4 VHF
--------------------

The VHF version uses a NiceRF SA868 transceiver for AFSK APRS. It is designed
around a 3.7 V battery and includes battery management and charging, with
charging and USB power provided through a USB-C connector on the PCB. A
separate DC/DC converter supplies the radio. Transmit power can reach 3 W;
software can reduce it to about 1 W.

The tracker is built on a compact, four-layer PCB in a Hammond enclosure,
with 3D-printed top and bottom covers. The radio and ESP32-S3 are fitted as
modules.

.. image:: img/20240922_154745.jpg
   :width: 70%
   :alt: Arctic Tracker 4 VHF

Arctic Tracker 4 UHF/LoRa
-------------------------

The UHF version operates at 433 MHz and supports LoRa APRS. It is based on
the VHF design, with a LoRa1268F30-Mini radio module in place of the SA868.
Its power supply is adapted for the radio module, which uses a 4 V transmitter
supply. The transmitter can provide up to 1 W, and the receiver includes a
low-noise amplifier (LNA).

.. image:: img/20241119_213542.jpg
   :width: 80%
   :alt: Arctic Tracker 4 UHF/LoRa PCB

For more on the development and design choices behind these versions, see
:doc:`hardware`.
