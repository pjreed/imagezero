imagezero\_transport [![Travis CI Build Status](https://travis-ci.org/swri-robotics/imagezero_transport.svg?branch=master)](https://travis-ci.org/swri-robotics/imagezero\_transport)
====================

ImageZero is a fast, lossless compression algorithm for 24-bit color photographic
images developed by [Christopher Feck](mailto:christoph@maxiom.de).  This repository
repackages it as a catkin package, has a package that provides ROS integration,
and has a package that implements a ROS image\_transport plugin that uses it.

The compressed size for natural, photographic color images is comparable to PNG, usually
between 30% to 50% of the original size.  It compresses more than 20 times faster than PNG
and decompresses about twice as fast, which means it is suitable for lossless compression
of real-time camera video feeds.  Read the 
[KDE Blog Post](https://kdepepo.wordpress.com/2012/01/30/fast-lossless-color-image-compression/)
about it for some more details.

Packages
--------

### imagezero

The [ImageZero](http://imagezero.maxiom.de/) image compression library, restructured
into a catkin package.  ImageZero is a high-performance lossless compression algorithm
designed for natural photos.

### imagezero\_ros

A library that provides ROS integration for ImageZero.  It contains methods for 
using ImageZero to convert between `sensor_msgs/Image`s and `sensor_msgs/CompressedImage`s.

### imagezero\_image\_transport

A ROS [image\_transport](http://wiki.ros.org/image_transport) plugin that uses
ImageZero as its compression mechanism.  It can be used like any other ROS
image\_transport by setting the `image_transport` param for your client node to `imagezero`.

Installation
------------

The imagezero packages are currently available in the [ROS Shadow Repository](http://wiki.ros.org/ShadowRepository) and should be in the main repository with the next release of ROS.  If you have the repository installed and are using ROS Indigo, Jade, or Kinetic, you can install any of the packages like so:
```
sudo apt-get install ros-<distro>-<package>
```

ROS Farm Build Status
---------------------

Package | Indigo (Saucy) | Indigo (Trusty) | Jade (Trusty) | Jade (Utopic) | Jade (Vivid) | Kinetic (Wily) | Kinetic (Xenial)
------- | -------------- | --------------- | ------------- | ------------- | ------------ | -------------- | ----------------
imagezero (32-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS32__imagezero__ubuntu_saucy_i386__binary)](http://build.ros.org/job/Ibin_uS32__imagezero__ubuntu_saucy_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT32__imagezero__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Ibin_uT32__imagezero__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT32__imagezero__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Jbin_uT32__imagezero__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU32__imagezero__ubuntu_utopic_i386__binary)](http://build.ros.org/job/Jbin_uU32__imagezero__ubuntu_utopic_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV32__imagezero__ubuntu_vivid_i386__binary)](http://build.ros.org/job/Jbin_uV32__imagezero__ubuntu_vivid_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW32__imagezero__ubuntu_wily_i386__binary)](http://build.ros.org/job/Kbin_uW32__imagezero__ubuntu_wily_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX32__imagezero__ubuntu_xenial_i386__binary)](http://build.ros.org/job/Kbin_uX32__imagezero__ubuntu_xenial_i386__binary/)
imagezero (64-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS64__imagezero__ubuntu_saucy_amd64__binary)](http://build.ros.org/job/Ibin_uS64__imagezero__ubuntu_saucy_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__imagezero__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Ibin_uT64__imagezero__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__imagezero__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Jbin_uT64__imagezero__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU64__imagezero__ubuntu_utopic_amd64__binary)](http://build.ros.org/job/Jbin_uU64__imagezero__ubuntu_utopic_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV64__imagezero__ubuntu_vivid_amd64__binary)](http://build.ros.org/job/Jbin_uV64__imagezero__ubuntu_vivid_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW64__imagezero__ubuntu_wily_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero__ubuntu_wily_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__imagezero__ubuntu_xenial_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero__ubuntu_xenial_amd64__binary/)
imagezero_image_transport (32-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS32__imagezero_image_transport__ubuntu_saucy_i386__binary)](http://build.ros.org/job/Ibin_uS32__imagezero_image_transport__ubuntu_saucy_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT32__imagezero_image_transport__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Ibin_uT32__imagezero_image_transport__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT32__imagezero_image_transport__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Jbin_uT32__imagezero_image_transport__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU32__imagezero_image_transport__ubuntu_utopic_i386__binary)](http://build.ros.org/job/Jbin_uU32__imagezero_image_transport__ubuntu_utopic_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV32__imagezero_image_transport__ubuntu_vivid_i386__binary)](http://build.ros.org/job/Jbin_uV32__imagezero_image_transport__ubuntu_vivid_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW32__imagezero_image_transport__ubuntu_wily_i386__binary)](http://build.ros.org/job/Kbin_uW32__imagezero_image_transport__ubuntu_wily_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX32__imagezero_image_transport__ubuntu_xenial_i386__binary)](http://build.ros.org/job/Kbin_uX32__imagezero_image_transport__ubuntu_xenial_i386__binary/)
imagezero_image_transport (64-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS64__imagezero_image_transport__ubuntu_saucy_amd64__binary)](http://build.ros.org/job/Ibin_uS64__imagezero_image_transport__ubuntu_saucy_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__imagezero_image_transport__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Ibin_uT64__imagezero_image_transport__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__imagezero_image_transport__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Jbin_uT64__imagezero_image_transport__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU64__imagezero_image_transport__ubuntu_utopic_amd64__binary)](http://build.ros.org/job/Jbin_uU64__imagezero_image_transport__ubuntu_utopic_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV64__imagezero_image_transport__ubuntu_vivid_amd64__binary)](http://build.ros.org/job/Jbin_uV64__imagezero_image_transport__ubuntu_vivid_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW64__imagezero_image_transport__ubuntu_wily_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero_image_transport__ubuntu_wily_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__imagezero_image_transport__ubuntu_xenial_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero_image_transport__ubuntu_xenial_amd64__binary/)
imagezero_ros (32-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS32__imagezero_ros__ubuntu_saucy_i386__binary)](http://build.ros.org/job/Ibin_uS32__imagezero_ros__ubuntu_saucy_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT32__imagezero_ros__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Ibin_uT32__imagezero_ros__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT32__imagezero_ros__ubuntu_trusty_i386__binary)](http://build.ros.org/job/Jbin_uT32__imagezero_ros__ubuntu_trusty_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU32__imagezero_ros__ubuntu_utopic_i386__binary)](http://build.ros.org/job/Jbin_uU32__imagezero_ros__ubuntu_utopic_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV32__imagezero_ros__ubuntu_vivid_i386__binary)](http://build.ros.org/job/Jbin_uV32__imagezero_ros__ubuntu_vivid_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW32__imagezero_ros__ubuntu_wily_i386__binary)](http://build.ros.org/job/Kbin_uW32__imagezero_ros__ubuntu_wily_i386__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX32__imagezero_ros__ubuntu_xenial_i386__binary)](http://build.ros.org/job/Kbin_uX32__imagezero_ros__ubuntu_xenial_i386__binary/)
imagezero_ros (64-bit) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uS64__imagezero_ros__ubuntu_saucy_amd64__binary)](http://build.ros.org/job/Ibin_uS64__imagezero_ros__ubuntu_saucy_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__imagezero_ros__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Ibin_uT64__imagezero_ros__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__imagezero_ros__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Jbin_uT64__imagezero_ros__ubuntu_trusty_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uU64__imagezero_ros__ubuntu_utopic_amd64__binary)](http://build.ros.org/job/Jbin_uU64__imagezero_ros__ubuntu_utopic_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Jbin_uV64__imagezero_ros__ubuntu_vivid_amd64__binary)](http://build.ros.org/job/Jbin_uV64__imagezero_ros__ubuntu_vivid_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uW64__imagezero_ros__ubuntu_wily_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero_ros__ubuntu_wily_amd64__binary/) | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__imagezero_ros__ubuntu_xenial_amd64__binary)](http://build.ros.org/job/Kbin_uX64__imagezero_ros__ubuntu_xenial_amd64__binary/)

Building From Source (ROS Indigo, Jade, Kinetic)
------------

These directions assume you have already set up a catkin workspace. See 
[this tutorial](http://wiki.ros.org/catkin/Tutorials/create_a_workspace) on the ROS Wiki
for help setting up a catkin workspace.

### Checking out the source code (wstool)

If you're using wstool, add this repository to your wstool workspace:

    wstool set imagezero --git https://github.com/swri-robotics/imagezero_transport.git -v 0.2.3

### Checking out the source code (git)

If you're not using wstool, you can check out the repositories with git:

    git clone https://github.com/swri-robotics/imagezero_transport.git

### Installing dependencies and building

Install all of the dependencies using rosdep by running the following command from the root of your catkin workspace:

    rosdep install --from-paths src --ignore-src

Build the workspace with catkin\_make:

    catkin_make

