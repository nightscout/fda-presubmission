
==========
Nightscout
==========

Nightscout is a suite of open source projects.  A smartphone provides
ubiquitous network connectivity to Dexcom's wireless receiver.  After
a polling period the last reading from the Dexcom reciever is
transmitted to a database in the cloud.  A website renders
near-real-time views of the records stored.

Device Description
==================

Nightscout project
------------------
The Nightscout project is actually a suite of several independent
projects:

* dexcom-uploder - Android app to poll dexcom, upload to cloud
* cgm-remote-monitor - A node.js web application that displays values
  stored by the Dexcom.
* cgm-pebble - A pebble watchface that reads and displays values from
  cgm-remote-monitor.

cgm-remote-monitor
##################

This is a web app which simulates the display of a Dexcom receiver.
In addition to showing the last known glucose level, it displays when
the reading was taken, and offers a way to pan several hours
retrospectively.


dexcom-uploader
###############

`dexcom-uploader` is an Android application implemented in java.  The
application starts when a Dexcom receiver is detected using the
operating system's usb management system.  The application reads data
from the serial port made available by Dexcom's usb connection, and
uploads the latest record to a specified data backend.  The backend
may either be a RESTful API or a mongo db, and is configured using a
preferences panel inthe application.

cgm-pebble
##########

`cgm-pebble` is a C and javascript watchface developed using
PebbleSDK.  The javascript code runs on a Smartphone maintaining
bluetooth connectivity to the Pebble watch.  The javascript code
retrieves information from `cgm-remote-monitor` and sends the last
reading to over bluetooth to the pebble watch.  The C code runs on the
watch, receiving messages over bluetooth from a smarthphone, and
rendering the date, time, value, and trend reported by
`dexcom-uploader`.

Development
-----------
Development takes place using github, from the nightscout organization
page: https://github.com/nightscout/.
Modifications, upgrades, development, and issue tracking happen using
the resources connected to assets shared by a community of people.


c. Device Description
---------------------

Please provide sufficient information regarding the device description,
25 which may include: 

* pictures of the device (where applicable); 

* engineering drawings (where applicable); 

* physical, chemical and/or biological processes/principles used by
  the device to generate device output, if applicable; 

* physical and biological characteristics of the device output, if
  applicable; 

* samples to demonstrate the use of the device (where feasible and appropriate); 

* explanation of the user interface and/or how the device interacts
  with other devices or with the user (medical professional and/or
  patient); 

* explanation of the materials used in the device; 

* a brief explanation of how the device is manufactured (where
  necessary); 

* discussion of the mechanism of action and how the device and/or, if
  applicable, device output is used; 

* for an IVD, detailed technical description of your device including
  instruments, reagents, components, software, principles of
  operation, and accessories (if there are changes to a previously
  cleared or approved device, then you should describe these changes); 

* discussion of the scientific basis for development of the device or
  an explanation of expected clinical utility; and 

* for a device to be submitted in a 510(k), any anticipated predicate
  and a descriptive comparison of the device to the predicate device. 

In addition to pictures and a written description, other information
about the clinical use of the device, such as a surgical technique
guide or video of how the device is used in the clinical setting, may
be helpful.26


