
===============
ComLink2 Driver
===============

The device, ``decocare``, is a comlink2 driver, a software library,
which implements methods and functions to facilitate communication
between Paradigm-compatible RF devices and data management application
software using the Carelink USB stick from Medtronic (MMT-7305NA).

The user's guide:
http://www.medtronicdiabetes.com/sites/default/files/library/support/carelink_usb_user_guide.pdf
indicates intended use is:

    Indications for use The Medtronic CareLink™ USB is indicated for
    use by patients at home and clinicians in a medical office setting
    to facilitate communication between Medtronic diabetes therapy
    management devices that use Paradigm-compatible RF telemetry
    (MWT1)* and a personal computer that uses data management
    application software.

Device Description
==================

decocare - the library
----------------------
Decocare is the name of a python package, a re-usable suite of python
source modules, which implements functions and methods to encode and
decode messages compatible with the ``ComLink2`` protocol used by the
MMT-7305NA Carelink USB stick.

Usage
#####

The library allows authors of python source code to write methods
needed to implement data management software.
In order to use the library, authors need to download the python
package, configure their local system to use the module, write new
python source code implementing the desired remote management
features, then execute their newly written source.

The library contains a listing of different messages, commercially
supported by Medtronic, allowing data management software to remotely
communicate with compatible devices.

Dissemination
#############
The source code is distributed using ``git``, a version control
system, ensuring that changes or versions of the source code are kept
in sync.

A user must know how to configure and use python modules and git in
order to install the software on a local PC.

The git repo, is hosted online https://github.com/bewest/decoding-carelink
available as an educational resource for discussing potential
applications of remote management software.

Installing
^^^^^^^^^^
In order to run the software, the source must be retrieved, deployed
and configured to run on a PC.  Currently the user must know how to
perform these steps, the easiest way is on the commandline:

    git clone https://github.com/bewest/decoding-carelink.git
    cd decoding-carelink
    sudo python setup.py install

mm-* tools, investigational tools
---------------------------------

Another set of devices are tools showing example usage of the library,
and tools to investigate how the library and the serial protocol are
used to communicate with the remote equipment work.

These tools facilitate use of the decocare library to exchange
messages with the usb stick, to audit the operation of the usb stick,
as well as to exchange and record messages with remote RF equipment
for debugging and analysis.

After configuring and installing the tool, these tools allow
initializing RF communications with compatible devices, exchanging a
series of predefined or customized commands, and saving the results
for later perusal.

These tools support communicating with remote Paradigm-compatible
equipment using commands supported by Medtronic in other commercial
products, in exactly the same way as those products, from the command
line, shell environment.  The following options allow users to control
how remote equipment is uniquey addressed or distinguished from other
compatible devices, and how communication begins.

``--init``
    Send remote signal to initialize RF communication.

``--serial``
    Only communicates with the remote equipment responding to this
    serial number.  This matches the number, I.E. on the back of
    Medtronic insulin pumps.

mm-send-comm.py
^^^^^^^^^^^^^^^

``mm-send-comm.py`` allows sending or customizing commands Medtronic
intends to support using their own software and devices.

mm-latest.py
^^^^^^^^^^^^^^^

``mm-latest.py`` Example showing construction of data management
software using the Carelink usb and protocol.  Uses same commands as
Carelink in a demonstration to query the given minutes of history and
pump activity.

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


