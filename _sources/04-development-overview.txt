
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
the "master" branch.  This workflow is sometimes called "gitflow"
http://nvie.com/posts/a-successful-git-branching-model/.

After the "master" branch has updated with changes relevant to the
community, specially crafted pull requests allow tracking the exact
git deltas necessary to bring another repo up to date with the
community accepted versions.  When community members report bugs, this
tracking system allows developers to reproduce and co-ordinate fixes,
in some cases specifically tailored to members' needs.

For example, in one instance, a mom from outside the U.S. needed
displays in mmol/l vs mg/dl.  A group of interested members
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
Gabriel Coleman in Coding Freedom, http://codingfreedom.com/ relies
heavily on an open review process to share and distribute
improvements.

The Software Freedom Law Center
http://www.softwarefreedom.org/resources/2010/transparent-medical-devices.pdf

Known issues
++++++++++++
There are several proposed improvements and known issues.  Notably,
the system as-is is not HIPAA compliant.  One of the key features in
this system that has helped to liberate people, and thus make them
safer, is the ease of use that accompanies pubically accessible data.
While we will adopt optional controls for authorizing and accessing
data, parents of this system value easily sharing data with a school
nurse with minimum hassle.

Future plans
------------

The sponsors would like to discuss appropriate regulatory controls
that protect open source authors' free speech as well as provides FDA
with an appropriate framework to fulfill their mission.

.. TODO::

  * Additional pre-subs
  * clinical trials/surveys
  * aggregrator

Oversight
+++++++++
Given the community's frustration with safety in available medical
devices to manage type 1 diabetes therapy, we believe there are
opportunities for open source authors and FDA to work together.  One
such opportunity is in post-market surveillance.  We have developed an
aggregator which re-displays de-personalized many Nightscout remote
monitors in a single "spaghetti plot."  We propose modifying this
aggregator to automatically compile and submit reports to the FDA in
order to aide in post market surveillance of devices used in diabetes
therapy.


Integration
+++++++++++

In the interest of safety, we need a single display to contextually
manage type 1 diabetes.  We will add data transfer from Medtronic
insulin pumps to obtain "treatment" data consisting of the bolus
wizard and bolus records.  Additionally, the display will
automatically show both the treatment data, carbohydrates, insulin,
and carb ration, from the insulin pump overlaid with glucose readings
from the Dexcom CGM.

In addition, we will also explore integrating with many other health,
fitness, and nutrition APIs.

We will follow up with additional pre-subs if required to discuss
further development efforts.


Instructions
^^^^^^^^^^^^
Please provide an overview of the product development, including an
outline of nonclinical and clinical testing either planned or already
completed. However, please note that our review of a Pre-Sub will not
include a review of bench or clinical data that you have already
collected. 
 
If you intend to include complete copies of literature articles as
part of this section, please try to include only those that are
relevant to the questions you are asking.  Additional articles can be
provided in any subsequent marketing application or IDE.  
