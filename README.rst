resetusb
========

``resetusb`` Tool for resetting all connected USB devices by looping overa all USB busses and devices. 
  
Get and Build resetusb
======================

source
^^^^^^

We use git for our source control. You can get a copy of our repo by doing the following::

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
