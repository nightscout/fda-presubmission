
Overview of Product Development
===============================

Development of decocare
-----------------------

The library was developed by via careful analysis of messages passed
between Medtronic's Carelink software, blood glucose meters equipped
with the feature known as ``meter-link``, Medtronic's pump remote
control, Carelink software, and the carelink usb stick.

Messages from the Carelink data management application software were
analyzed for structure and semantics.  Python code was then written to
recreate the messages needed to successfully transfer data from remote
equipment to a local application.  The full logs and output from each
experiment were captured in git for additional debugging and perusal.

The software includes a suite of tests.  Many of the tests will
prevent the software from running in an abnormal condition is found
in the tests.  The Carelink USB stick offers a facility for counting
how many messages have been sent and recieved in error, corrupted, or
successfully.  All experiments capture the status of these counters at
the beginning and end of each use to provide diagnostic information on
the operation of the usb stick.  This information can be helpful in
determining if the protocol is exchanging messages as Medtronic
intended.


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
