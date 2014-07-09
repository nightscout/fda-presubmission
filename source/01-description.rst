
==========
Nightscout
==========

Nightscout is a suite of open source projects.  A smartphone provides
ubiquitous network connectivity to Dexcom's wireless receiver.  After a polling
period the last reading from the Dexcom reciever is transmitted to a database
on the internet.  A website renders near-real-time views of the records stored
in that database.  Additionally, the website offers an http endpoint that a
pebble watch can use to display the last known alarm status, trend, and glucose
level as reported by the Dexcom receiver.

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

When assembled, the completed device is called a "Nightscout rig."
In addition to the raw source code for these applications, other
community maintained resources exist to help people learn how to
assemble their own rigs.  These include groups, photos, shared
documents, videos on a variety of social media, including a
centralized community curated website for documentation as well as
community maintained forum software.

cgm-remote-monitor
##################

This is a web app which simulates the display of a Dexcom receiver.
In addition to showing the last known glucose level, it displays when
the reading was taken, and offers a way to pan several hours
retrospectively.

Every 5 minutes, a node.js server polls a mongo database, emitting the
last readings over the last two days to any listeners subscribed to
the server's "sgv" websocket event.  The server also serves a
combination of html, css, and javascript to simulate a
near-real-time display of the Dexcom receiver.

The web display works on most modern web browsers.

dexcom-uploader
###############

`dexcom-uploader` is an Android application implemented in java.  The
application starts when a Dexcom receiver is detected using the
operating system's usb management system.  The application reads data
from the serial port made available by Dexcom's usb connection, and
uploads the latest record to a specified data backend.  The backend
may either be a RESTful API or a mongo db, and is configured using a
preferences panel inthe application.

The `dexcom-uploader` source code must be compiled and distributed as
an APK before it can run on an Android smartphone.  Once installed and
configured to upload data to the preferred cloud "backend", a USB OTG
cable is used to connect the smartphone to the Dexcom receiver's micro
usb port.  The Dexcom receiver is a device cleared by the FDA for
continuously monitoring glucose levels sampled from interstitial
fluid.  The receiver is designed to store and display values
transmitted by the Dexcom sensor.  `dexcom-uploader` uses the serial
connection provided by this usb capability to exchange data with the
Dexcom receiver.  The behavior of the uploader has been designed to
behave as Dexcom would expect any data management system to behave.
There is no expected difference in Dexcom's behavior when the uploader
smartphone is attached or while our software is auditing the records
on the Dexcom receiver.


cgm-pebble
##########

`cgm-pebble` is a C and javascript watchface developed using
PebbleSDK.  The javascript code runs on a Smartphone maintaining
bluetooth connectivity to the Pebble watch.  The javascript code
retrieves information from `cgm-remote-monitor` and sends the last
reading to over bluetooth to the pebble watch.  The C code runs on the
watch, receiving messages over bluetooth from a smarthphone, and
rendering the date, time, value, and trend as reported by a running
instance of `cgm-remote-monitor`.


Development
-----------

Development takes place using github, from the nightscout organization
page: https://github.com/nightscout/.
Modifications, upgrades, development, and issue tracking happen using
the resources connected to assets shared by a community of people.
Each and every change to the source code is tracked by git and
discussed through a github pull request.  Upgrades are provided by
providing git merge requests, often using the Github UI, by
identifying the last commit hash in use, and a verified change
controlled path to apply latest updates from trusted contributors.


Assembly and guides
-------------------
The git repos merely provide the source code, and a verified way of
exchanging source code for these projects.  In order to be used, the
source code must be configured, compiled, deployed, and installed.

While each repo contains instructions on how to test and work with
that repo, the Nightscout guides, forums, youtube videos, pictures,
and Facebook group provide "educational" material on how people have
combined and configured these disparate parts to assemble something
resembling a "medical device."  The web guides also reside in a git
repo, where improvements are proposed by the community, reviewed, and
adopted in similar manner to the source code itself.

The guides explain how to configure and install each component, with
warnings of "things that might go wrong" at each phase.  When people
experience issues following the guides or during use, they use social
media to find people that have similar issues or ask for help.  There
are also recommendations, optimized for cost and predictability, on
which service providers are available, as well as how to work with
those service providers.




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


