
Overview of Product Development
===============================

Community based, social technical development
---------------------------------------------

Nightscout begins
+++++++++++++++++
As an open source project, the entire source code came into existence
when people affected by type 1 diabetes with access to the best and
safest therapy options found themselves unable to obtain therapy
without any adverse events.  In order to help monitor, communicate,
and understand therapy, a few individuals created a data management
system using commodity equipment allowing them to easily monitor the
CGM without requiring physical access to the CGM receiver.  Spurred by
the improved family relationships and finding therapy easier to track,
communicate, and manage, more and more people have added small
improvements or helped others to gain liberties on their own.  Many of
these individuals cite "keeping their own children safe" as reasons
for beginning their involvement with the project.

As of July 1, 2014, a dozen or so like-minded individuals record all
proposed changes in their own Github forks or Github branches
dedicated to discussing improvements or changes to a code base that is
in active use by several dozen individuals and families.  After the
community reviews and tests these proposals in a public audit called a
"pull request," one of the core contributors accepts the changes into
the "master" branch.  This process of tracking, recording, and auditing work is
sometimes called gitflow_.

.. _gitflow: http://nvie.com/posts/a-successful-git-branching-model/

After the "master" branch has updated with changes relevant to the
community, specially crafted pull requests allow tracking the exact
git deltas necessary to bring another repository up to date with the
community accepted versions.  When community members report bugs, this
tracking system allows developers to reproduce and co-ordinate fixes,
in some cases specifically tailored to members' needs.

.. raw:: pdf

    FrameBreak 50

For example, in one instance, a several individuals outside the U.S.
needed displays in ``mmol/L`` vs ``mg/dL``.  A group of interested members
teamed up to work on special mmol/l versions.  The member actually
completed the required changes, sharing the needed deltas with the
group.  As a result, we were able to re-use these same git tracking
methods to compare and issue updates specifically for these users
needing mmol/l.

Open source methodology
+++++++++++++++++++++++

The development of Nightscout as an open source project follows a
predictable development pattern to identify issues, incorporate bug
fixes, as well as develop new features.  The model, as discussed by
Gabriel Coleman in `Coding Freedom`_ relies heavily on an open review
process to share and distribute improvements.

The Software Freedom Law Center, in `Transparent medical devices`_,
also outlines the need for greater transparency in the operation of
these medical devices.  We encourage the FDA to adopt regulations that
are consistent with the protections provided by open source methods,
including `Linus's Law`_ to make all bugs shallow and accessible to
those affected by them.
In designing Nightscout, we try to adhere to the design principles
outlined in `Unix philosophy`_ in order to ensure safe, predictable,
and effective operation of the Nightscout rig.

.. _Coding Freedom: http://codingfreedom.com/
.. _Transparent medical devices: http://www.softwarefreedom.org/resources/2010/transparent-medical-devices.pdf
.. _Linus's Law: http://www.catb.org/esr/writings/homesteading/cathedral-bazaar/ar01s04.html
.. _Unix philosophy: http://www.faqs.org/docs/artu/ch01s06.html

Known issues
++++++++++++

There are several proposed improvements and known issues. One key
feature liberating people, and thus making them safer, is the ease of
use that accompanies data being made accessible to other trusted
individuals. While we will adopt optional controls for authorizing and
accessing data, parents of this system value easily sharing data with
a school nurse with minimum hassle; and adults using this system value
easily sharing their data as well.

Future plans
------------

The sponsors would like to discuss appropriate regulatory controls
that protect open source authors' free speech as well as provides FDA
with an appropriate framework to fulfill their mission.
The sponsors passionately share the FDA's mission to protect and
promote public safety, a key reason Nightscout development is done as
a "public performance," and freely shared.

Oversight
+++++++++
Given the community's frustration with safety in available medical
devices to manage type 1 diabetes therapy, we believe there are
opportunities for open source authors and FDA to work together.  One
such opportunity is in post-market surveillance.  We have developed an
aggregation tool which redisplays, depersonalized, many Nightscout
remote monitors in a single "spaghetti plot."  We propose modifying
the aggregating tool to automatically compile and submit reports to
the FDA in order to aide in post market surveillance of devices used
in diabetes therapy, and to generate useful research data on larger
populations.


Integration
+++++++++++

In the interest of safety, we need a single display to contextually
manage type 1 diabetes.  We will add data transfer from Medtronic
insulin pumps to obtain "treatment" data consisting of the bolus
wizard and bolus records.  Additionally, the display will
automatically show both the treatment data, carbohydrates consumed,
insulin, and carbohydrate ratio, from insulin pumps overlaid with
glucose readings from the Dexcom CGM.

In addition, we will also explore integrating with many other health,
fitness, and nutrition APIs.

We will follow up with additional premarket submissions as required to
discuss further development efforts.  See also, `decoding-carelink`_,
and the pending `decoding-carelink pre-submission`_.

.. _`decoding-carelink`: https://github.com/bewest/decoding-carelink
.. _`decoding-carelink pre-submission`: http://medevice-users.github.io/decoding-presub/#


Operational metadata
++++++++++++++++++++
We anticipate adding indicators showing the connectivity status of the
uploader device, as well as battery status, and other operational
details of the system.  These details will help quickly assess
validity of the data, and whether or not the system is working and
trustworthy.

Access controls
+++++++++++++++

During development, the community has expressed an interest in
developing access controls to help protect who can access displays.
We anticipate development of "named views" which can be used to
control who accesses the remote monitor website, as well as when and
how.  These views may optionally be protected by user name and password
type of login system, or through creating unique and opaquely encoded
tokens explicitly for sharing.  We have found that the flexibility in
sharing information in public outweighs the relative risks in the data
being made public.  As the community and software matures, we
anticipate personalizing the access controls to meet the needs of its
users.

Support/Commercialization
+++++++++++++++++++++++++

One criticism of open source is the lack of commercial support for
individuals who lack the ability to safely assemble and operate their
own rig.  While the open source culture provides a large community
able to train and offer support, the project remains accessible only
to those with sufficient technical ability to assemble and debug their
own equipment.  We propose that the community would be safer if the
public could buy assembled rigs on the market with support contracts
to help ensure high quality operation for individuals lacking the time
and effort.  However, we are concerned that the current regulations
considering this a "high risk" device prevents unprepared individuals
from obtaining the help they need.


