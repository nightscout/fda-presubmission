
Meeting Minutes
===============
What follows are minutes of the first Nightscout FDA Pre-submission
Meeting which took place on October 8, 2014.

Summary
-------
  *  FDA expressed interest in a continuing conversation related to
     the Nightscout project
  *  While Medical Device regulations are applicable to the Nightscout
     project, Medical device requirements are implemented to ensure
     patient safety and were written to be flexible to address all
     types of medical devices and device manufacturers.
     How these regulations can be met was discussed with the agency.
  *  Areas to be discussed – is there one responsible party? -
  *  How are design controls met during software development?
    - How to fulfill post market requirements?
    - What product claims are made?
    - How are data security and privacy handled?
  *  FDA and NightScout project members discussed performing a gap
     analysis regarding the regulations for the next discussion.
     Meeting time TBD.

Attendees
---------
Participant introductions of attendees:

CGM in the Cloud / Nightscout
_____________________________
John Costik, Ping Fang, Ben West, and Scott
Leibrand

Your Diabetes May Vary
......................
Bennet Dunlap

Invited guests
..............
Medtronic: Mark O’Donnell


FDA
___
Beth Stephen, Don St. Pierre, Robert Sauer,
Stayce Beck, Courtney Lias, Katherine Serrano,
Suzanne Schwartz, and Ariel Seeley

Discussion Topics
-----------------
Introduction: 
FDA requested some background discussion on Nightscout's software and
project, history, open-source development methodology, and some
existing controls, including general project oversight, how system
updates are handled, and directions available to users.

FDA provided some initial comments to emphasize that FDA doesn't have
a bias against the open source route, nor is Nightscout the first time
FDA has seen open source software.  FDA emphasized that a key tenet of
device regulation is that some entity be responsible for assuring the
safety and effectiveness of the device and that postmarket safety is
adequately monitored and that any potential problems are adequately
addressed.  FDA further emphasized that the requirements for medical
devices were implemented to ensure patient safety and were written to
be flexible to address all types of medical devices and device makers,
and that FDA believes it is acheivable for Nightscout to meet
applicable requirements even with non-traditional methods of
development.


FDA asked questions about Nightscout's current processes and
how/whether they currently control software versions that go out to
general use of Nightscout.  Further questions were discussed about how
Nightscout handles topics that should be addressed in device
development, including quality, safety, and responsibility (e.g.
Design Controls, Change Controls, Postmarket Surveillance, Claims, and
Data/Cybersecurity) were also discussed.  Nightscout provided a
description of how core developers maintain the main community
version, and review and test new features before they are incoportated
or distributed to end users.  Nightscout used an example of a current
issue of incorrect time values to address questions such as:

  * How quickly are changes/problems addressed?

    - Determined by interest of developers and safety concerns

  * How is information on updates distributed?

    - Currently an informal process for development updates and
      checking

  * Who is responsible for code updates?

    - Ben currently triages, is the source code curator, coordinates
      efforts between developers.  This activity is currently
      voluntary and informal.

  * How are updates tracked?

    - Website can track which version people are using, can push
      update requests to users.


The group discussed the FDA's and and Nightscout’s shared goal of safety. The
FDA hears the demand from patients for devices like Nightscout to
exist, and doesn’t have a particular problem with safe and effective
devices of this kind
coming to market.  In fact, they want to make this happen faster.

The FDA also
recognizes the need for device interoperability to improve data
access, along the lines of what Tidepool is working on.
They noted
recent progress on interoperability from CGM makers.
Subsequent to the meeting, the FDA would like to hear from our
community to help make sure interoperability moves forward.

The group discussed FDA’s desire that there be a single responsible party to
ensure that nothing falls through the cracks. The FDA emphasized the need for
one party to take responsibility. For example, change control to determine when
updates were ready to be implemented to general users, what problems need to be
addressed and on what timeline, etc. should be adequately addressed. The FDA
also asked about how problems are identified, reported, and addressed. They
want to make sure there is a mechanism to handle, triage, and prioritize the
response to complaints that might affect safety, to ensure that fixes can be
distributed to people using the system, and to make sure that Nightscout is
preventing unexpected complications from modifications.  Nightscout stated that
currently, how quickly a problem is addressed is determined by how quickly a
developer picks up the issue and propose a solution. This may depend on the
interest of the developers, the safety concern raised, and the complexity of
the issue and its solution. The FDA discussed the benefits of implementing a
process for evaluating the severity of issues and tailoring the speed at which
solutions are developed to address the relative risk associated with the
particular scenario. The FDA recognizes that Nightscout’s existing methods and
processes, while informal, appear to address some of these concerns, but would
like to see further documentation of how Nightscout is doing so, and wants to
ensure that there is someone ultimately responsible. FDA interests include what
happens if developers do not “jump” in quickly enough to develop solutions, the
need to track issue severity, and concerns regarding the importance of
reporting problems. Nightscout noted that they had determined that one person
needed to be assigned as the lead. Ben West was voted by the core contributors
to be the source code curator. FDA noted that was encouraging and that a
similar approach could be more broadly implemented to address some of the FDA’s
safety and regulatory concerns.

The group discussed how Nightscout might be able to provide the FDA with better
visibility into any events that affect patient safety. The FDA would welcome
submissions from Nightscout to MedWatch, especially if they can include as much
detail as possible to see what was really going on. Such processes will help
Nightscout make decisions on how to improve the system.

FDA requested that Nightscout begin working on a gap analysis to document what
is already being covered, and which areas require improvements to come into
compliance. The FDA requested a follow-up meeting with Nightscout within a few
months.

