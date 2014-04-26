
Specific Questions
==================

Intended use
------------

* What is intended use of carelink stick MMT-7305NA?
* What are intended use of commands/messages sent to MMT-7305NA from
  application

* Does Medtronic/FDA know of any bugs triggered by these commands
  sent to/from MMT-7305NA that may cause unexpected behavior, or
  behavior other than originally intended?


Use of MMT-7305NA
^^^^^^^^^^^^^^^^^

The instruction manual indicates that the usb stick is intended for
use by patient or doctor to exchange messages between a data
management application and compatible medical devices.  The
instruction manual does not seem to include any instructions
demonstrating use of the usb stick.  It also does not indicate
semantics for messages transferred to remote equipment.

The MMT-7305NA was designed to exchange all messages that remote
equipment supports, but no instructions on usage are available from
its sponsor.

The messages facilitate creating a record of treatment.
Should patients be able to get a copy of their records as the pump
produces them?

  * What if the vendor software does not work?


* How does use of MMT-7305NA affect remote equipment, ie battery life
  of pump, total number of capitance charge cycles, etc...

  * Is this
    part of intended use of MMT-7305NA?

Commands
++++++++

The MMT-7305NA is capable of exchanging many different types of
commands, each with a different intended purpose.  Are each of these
certified/pre-subed separately?  Different equipment and models
respond differently to different commands.  Are there any indications
how these commands are intended to be used with these devices?

* What if decocare only sends commands supported by each device?

  * Does it stay within the intended use of vendor?

* What is intended use case for the remote control?

  * If the remote exchanges a message to bolus, a new tool, eg,
    ``mm-send-bolus-example.py`` both send the exact same message, 
    is the tool covered by the remote's use case?


* Are there commands which trigger otherwise unexpected behavior?

  * Are there firmware bugs known to exist in different models, eg
    1.16 vs 1.17, suspend bug?

  * If some commands are less stable with regard to behavior in the
    firmware, should the vendor share this information with users of
    the device?  Should it be in the instruction manual?

Should MMT1's commands be documented so that users know what each
command is intended to do?

Fault / responsibility
++++++++++++++++++++++

If something goes wrong who is at fault?
Depends on what goes wrong whether or not device was used according to
intended use or not.  What is the intended use of the MMT-7305NA, how
will users use it, how do users get support?



Future software devices
+++++++++++++++++++++++

Authors using decocare could create additional tools:

* logging

  * log all history
  * query for recent history

* audit

  * create log of device behavior
  * injury/adverse event reporting tool might
    automatically compile report of all injurious events in therapy
    history and submit to FDA

* bolus wizard

  * bolus wizard on the web/browser
  * bolus wizard on mobile
  * bolus wizard from laptop
  * bolus wizard from data management software

* artificial pancreas

  * auto suspend
  * auto temp basal
  * auto bolus

g. Specific Questions
---------------------

The Pre-Sub should include specific questions regarding review issues
relevant to a planned IDE, or marketing application (e.g., questions
regarding pre-clinical and clinical testing protocols or data
requirements) as our advice will be guided by your questions and may
not identify all submission requirements. Appendix 1 of this guidance
contains sections specific to IDE, 510(k), PMA, and HDE that list
examples of questions appropriate to each submission and application
type.  

