resetusb
========

``resetusb`` is (yet another) tool for resetting all connected USB
devices. It loops over all USB busses and devices. For each device, the
tools opens the corresponding device handle and sends a RESET to the
port. The tools will disaply a list of all found devices together with
the success state of resetting (0 in case of success, <0 if an error
occured).

The tool comes in handy when devices get stuck, e.g., under heavy load
when using several cameras.
  
Get and Build resetusb
======================

source
^^^^^^

We use git for our source control. You can get a copy of our repo by doing the 
following::

   git clone git://github.com/dirkholz/resetusb.git

dependencies
^^^^^^^^^^^^
resetusb requires

- libusb (http://www.libusb.org/)

On ubuntu you can get most of these through apt::

   sudo apt-get install libusb-dev


build
^^^^^
To build you should just follow a normal cmake recipe::
   
   cd resetusb
   mkdir -p build
   cd build
   cmake ..
   make
   sudo make install

Running
=======

In order to run resetusb simply type::

   sudo resetusb
