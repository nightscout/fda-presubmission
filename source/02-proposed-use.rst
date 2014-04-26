
Proposed Use
============

Intended Use of MMT-7305NA
^^^^^^^^^^^^^^^^^^^^^^^^^^

Decocare is an open source driver for a commercially available device,
the MMT-7305NA.
The user's guide:
http://www.medtronicdiabetes.com/sites/default/files/library/support/carelink_usb_user_guide.pdf
indicates intended use is:

    Indications for use The Medtronic CareLink™ USB is indicated for
    use by patients at home and clinicians in a medical office setting
    to facilitate communication between Medtronic diabetes therapy
    management devices that use Paradigm-compatible RF telemetry
    (MWT1)* and a personal computer that uses data management
    application software.

Intended Use of decocare
^^^^^^^^^^^^^^^^^^^^^^^^
Provides methods and utilities to facilitate communication between
Paradigm-compatible devices and data management application software.

Observing device behavior
+++++++++++++++++++++++++

Decocare helps observe the behavior of MMT-7305NA and compatible
medical devices in greater detail.  The tools expose diagnostic
information regarding successful transmission of messages to the
device, as well as allows users to precisely audit and log device
behavior.

A user may use the ``mm-send-comm.py`` tool to request and save a page
of data, as it existed on the pump.

Creating data management software
+++++++++++++++++++++++++++++++++

Decocare allows python authors to create data management tools.
Decocare transfers messages from a data management application
to remote devices and back.  An application developer can use this
facility to create a program which uses the ``ReadHistoryData``
command, decodes the information, and presents it to the user or saves
it for later use.

Frequency of use
^^^^^^^^^^^^^^^^

We are unsure what Medtronic's recommendation is regarding how
frequently remote equipment may communicate with application software.


d. Proposed Intended Use/Indications for Use
--------------------------------------------

Please provide sufficient information regarding the proposed intended
use/indications for use, 

which may include: 

* identification of the disease or condition the device is indicated
  to prevent, mitigate, screen, monitor, treat, or diagnose; 

* identification of the target population; 

* part of the body or type of tissue to which applied or with which
  the device is interacting; 

* frequency of use; 

* physiological use; and 

* statement of whether the device is intended for prescription and/or
  over-the-counter use. 

For an IVD device, this information should include a detailed draft of
the intended use of the device including the intended use population,
the analyte/condition to detect, and the assay methodology (see
Section F of Appendix 1 for more detailed information). 

