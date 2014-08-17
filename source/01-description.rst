
==========
Nightscout
==========

Nightscout is a suite of open source projects.  A smartphone provides
ubiquitous network connectivity to Dexcom's wireless receiver.  After a polling
period the last reading from the Dexcom receiver is transmitted to a database
on the Internet.  A website renders near-real-time views of the records stored
in that database.  Additionally, the website offers a ``RESTful API`` that a
pebble watch can use to display the last known alarm status, trend, and glucose
level as reported by the Dexcom receiver.

Device Description
==================

Nightscout project
------------------
The Nightscout project is actually a suite of several independent
projects:

* `android-uploader`_ - Android application to poll the Dexcom receiver,
  transferring the data to cloud.

* `cgm-remote-monitor`_ - A ``node.js`` web application that displays values
  stored by the Dexcom.

* `cgm-pebble`_ - A pebble watch face that displays values reported by 
  `cgm-remote-monitor`_.

When assembled, the completed device is called a "Nightscout rig."
In addition to the raw source code for these applications, other
community maintained resources exist to help people learn how to
assemble their own rigs.  These include groups, photos, shared
documents, videos on a variety of social media, including a
centralized community curated website for documentation as well as
community maintained forum software.

cgm-remote-monitor_
###################

This is a web application which simulates the display of a Dexcom
receiver.  In addition to showing the last known glucose level, it
displays when the reading was taken, and offers a way to pan several
hours retrospectively.

Every 5 minutes, a ``node.js`` server polls a mongo database, emitting
the last readings over the last two days to any listeners subscribed
to the server's ``sgv`` websocket event.  The server also serves a
combination of html, css, and javascript to simulate a near-real-time
display of the Dexcom receiver.

The web display works on most modern web browsers.

android-uploader
###############

`android-uploader`_ is an Android application implemented in java.  The
application starts when a Dexcom receiver is detected using the
operating system's usb management system.  The application reads data
from the serial port made available by Dexcom's usb connection, and
uploads the latest record to a specified data backend.  The backend
may either be a RESTful API or a mongo database, and is configured using a
preferences panel in the application.

The `android-uploader`_ source code must be compiled and distributed as
an APK before it can run on an Android smartphone.  Once installed and
configured to upload data to the preferred cloud "backend", a USB OTG
cable is used to connect the smartphone to the Dexcom receiver's micro
usb port.  The Dexcom receiver is a device cleared by the FDA for
continuously monitoring glucose levels sampled from interstitial
fluid.  The receiver is designed to store and display values
transmitted by the Dexcom sensor.  `android-uploader`_ uses the serial
connection provided by this usb capability to exchange data with the
Dexcom receiver.  The behavior of the uploader has been designed to
behave as Dexcom would expect any data management system to behave.
There is no expected difference in Dexcom's behavior when the uploader
smartphone is attached or while our software is auditing the records
on the Dexcom receiver.


cgm-pebble
##########

`cgm-pebble`_ is a C and javascript watch face developed using
PebbleSDK.  The javascript code runs on a Smartphone maintaining
bluetooth connectivity to the Pebble watch.  The javascript code
retrieves information from `cgm-remote-monitor`_ and sends the last
reading to over bluetooth to the pebble watch.  The C code runs on the
watch, receiving messages over bluetooth from a smartphone, and
rendering the date, time, value, and trend as reported by a running
instance of `cgm-remote-monitor`_.


Development
-----------

Development takes place using Github, from the Nightscout organization
page: https://github.com/nightscout/.
Modifications, upgrades, development, and issue tracking happen using
the resources connected to assets shared by a community of people.
Each and every change to the source code is tracked by git and
discussed through a Github pull request.  Upgrades are provided by
providing git merge requests, often using the Github UI, by
identifying the last commit hash in use, and a verified change
controlled path to apply latest updates from trusted contributors.


Assembly and guides
-------------------
The git repositories merely provide the source code, and a verified way of
exchanging source code for these projects.  In order to be used, the
source code must be configured, compiled, deployed, and installed.

While each repository contains instructions on how to test and work with
that repository, the Nightscout `development guides`_, `forums`_, `youtube
videos`_, `pictures`_, `twitter account`_, and `Facebook group`_
provide "educational" material on how people have combined and
configured these disparate parts to assemble something resembling a
"medical device."  The web guides also reside in a git repository, where
improvements are proposed by the community, reviewed, and adopted in
similar manner to the source code itself.

The guides explain how to configure and install each component, with
warnings of "things that might go wrong" at each phase.  When people
experience issues following the guides or during use, they use social
media to find people that have similar issues or ask for help.  There
are also recommendations, optimized for cost and predictability, on
which service providers are available, as well as how to work with
those service providers.



.. _cgm-remote-monitor: https://github.com/nightscout/cgm-remote-monitor
.. _cgm-pebble: https://github.com/nightscout/cgm-pebble
.. _Nightscout github organization: https://github.com/nightscout
.. _development guides: http://nightscout.github.io/
.. _android-uploader: https://github.com/nightscout/android-uploader
.. _forums: http://www.nightscout.info/
.. _youtube videos: https://www.youtube.com/channel/UChgmRw-YYFCtLbRVFDlSMHA
.. _pictures: http://imgur.com/a/cxcGG/all
.. _twitter account: https://twitter.com/nightscoutproj
.. _Facebook group: https://www.facebook.com/groups/cgminthecloud/

