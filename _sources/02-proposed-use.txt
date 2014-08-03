
Proposed Use
============

Nightscout
^^^^^^^^^^
Nightscout is intended to be used as part of a data management system.
The system provides for a "glanceable" secondary display of the
information originating from the Dexcom CGM.  A website allows the
display to be presented on any device which can display websites to
duplicate the display of the Dexcom.

The best way to get an idea of how people use Nightscout is to peruse
the `public testimonials`_ of use, or the `Facebook group`_.

.. image:: http://i.imgur.com/q9gWTAd.png
.. image:: http://i.imgur.com/y8V7SMW.png
.. image:: http://i.imgur.com/hopdq1X.png
.. image:: http://i.imgur.com/a1rRb3X.png


.. _public testimonials: http://imgur.com/a/cxcGG/all
.. _Facebook group: https://www.facebook.com/groups/cgminthecloud/

Single pane of glass
++++++++++++++++++++
The website url is typically shared with caregivers and interested
parties.  This allows multiple people to monitor a Dexcom user's
glucose levels from concurrently from any internet connection.
Multiple redundant displays eliminates transcription error and raises
the fidelity of communicating current therapy status.



Glanceability
+++++++++++++
Displays are duplicated in multiple redundant locations.  This
alleviates people from needing to physically locate and attend to the
receiver.  The lowered burden enables people to be more persistently
aware, and therefore respond to scenarios with treatment with greater
ease.

For example, in scenarios where no therapeutic action is required, but
the glucose levels must be considered, the glanceable display
eliminates the 30 second interuption to an existing workflow.


Reliance on pre-existing work
-----------------------------

The Nightscout project relies on commodity components, as well as the
excellent work from the folks at Dexcom.  The android software
interacting with the Dexcom receiver attempts to faithfully transmit
data from the receiver to a configured storage/data management service
hosted on the internet.  The android software is agnostic of the data
management service, and can be configured to work with several
different data management service providers.  It also attempts to
behave in the way that Dexcom expects all data management systems to
behave.  An open analysis of the source code listings and comparisons
of behavior reveals that the behavior of the Dexcom receiver is
unaffected when this system is in use.  The use or non-use of
Nightscout has no observable difference in the Dexcom equipment or
system, either while Dexcom is in use or after.  Eg, we believe that
Nightscout has no effect on Dexcom's performance, quality, or safety.

When Nightscout is in use, the community recommends that users
maintain their normal therapy.  Nightscout should not alter therapy
plans or decisions.  Many of the community members recommend falling
back to baby monitors, phone, sms, smbg finger-sticks, and physically
checking the Dexcom receiver as tools to augment therapy, even while
Nightscout is in use.
The guiding philosophy behind this advice is that technology is a tool
for managing therapy; that people administer therapy, not technology.
Nightscout is another tool using commonly available technology, like
baby-monitors, to bring diabetes therapy, specifically communicating
current satus of therapy, more in line with the way the users of these
tools, like Dexcom, feel is acceptable.

Uses of Nightscout
------------------

Nightscout is useful any time remote near-real-time monitoring of
Dexcom readings are desirable.  People with diabetes find it useful to
keep mindfulness of glucose levels while biking or other activities
requiring both hands.  People with diabetes find it useful for sharing
and gaining empathy of their glycaemic states.

Due to the ease of use, parents have been able to co-ordinate with
school Nurse to prevent or treat injuries which are otherwise common.
In some cases, use of Nightscout has helped gain insight into how
common these injuries are, and we believe that the community
aggregator can be used to report these injuries to the FDA for
increased oversight of Dexcom and Medtronic devices in the
marketplace.  The community has also received reports of some parents
using Nightscout to co-ordinate sleep-overs or camp visits, and in
some cases walks with Grandpa, many for the first time, that would not
other wise happen.  They all cite Nightscout's remote telemetry in
liberating these activities, in some cases with pictures indicating
injuries staved off or critical rescue care co-ordinated.

Adult users have cited Nightscout in increasing discretion.  A common
complaint among users of type 1 diabetes medical equipment is that
the mandated use of the equipment combined with the time it takes to
use the equipment often presents the unknowing public with a rude
experience.  It often appears that a PWD is ignoring someone by
favoring a phone or pager or just producing rude beeps.  When
Nightscout is in use, the requirement to touch one of these medical
devices disappears, which allows incorporating mindfulness more often
and in a variety of different ways into the every day work flow.  As a
result, fewer interuptions from physically touching the medical device
increases discretion because social disruptions are also reduced.

Requirements
------------

Nightscout uploader device
++++++++++++++++++++++++++
Android smartphone capable of "USB OTG" capability.  These are
commonly available.  WIFI only versions, known as "android mini-pcs"
or and "Android TV box" are also commonly available.  The prices vary
widely from vendor to vendor, and depending on the cell network
carrier subsidies.

Without any help, the DIY version requires downloading the source code
from the internet.  Google's Android software development kit is
required to configure and compile the source listings from the git
repo.  This process requires that users know, or learn how to, prepare
their device for debugging, go through basic debugging steps in order
to configure, compile, and deploy the software as binary android
package, and then install and run the software on their own
smartphone.

