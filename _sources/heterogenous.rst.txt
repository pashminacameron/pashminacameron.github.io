.. post:: Aug 29, 2018
   :tags: Hardware
   :author: Pashmina Cameron

Heterogenous Compute
====================

As we reach the end of Moore's law (CPU performance doubles every 2 years) and
Dennard scaling (as transistors get smaller their power density remains
constant - so each transistor uses less power), the focus of computer
architecture has moved towards Heterogenous computing.

A good overview of computer architecture in general and this topic in particular may be found in:

* Computer Architecture: A Quantative Approach (John Hennesy, David Patterson)
  `Amazon <https://www.amazon.co.uk/Computer-Architecture-Quantitative-Approach-Kaufmann/dp/012383872X>`_

* John Hennesy and David Patterson 2017 ACM Turing Award Lecture `YouTube video <https://www.youtube.com/watch?v=3LVeEjsn8Ts>`_

*****************************
What is heterogenous compute?
*****************************

This term is used to cover the mixture of traditional CPU based computing that 
is meant to do fairly well on most tasks with
more special purpose devices that are optimized for particular types of
algorithm.

This includes:

* **CPUs** - It may seem obvious but the thing that makes these approaches
  heterogenous is that we have a mixture of different compute devices.
  The highest performance systems make use of the CPU for what it is best
  at in conjunction with more specialist devices.
* :ref:`GPUs <gpu_label>` - Modern Graphics Processors have features specifically to enable
  / enhance their use for non graphics, i.e. compute tasks.
* :doc:`DSPs <DSPs>` - A class of general purpose CPUs with very different characteristics
  from a CPU.  These are especially suited for stream processing. 
* :doc:`FPGAs <fpgas>` - Flexible devices that let you implement almost any hardware design
  you want.  This is often the path to a *cheap* or *on demand* domain
  specific accelerator.
* :doc:`DomainSpecificArchitectures` - These can still have a high degree of
  programability but they are designed to take on
  one class of problems.  GPUs started as domain specific processors but have evolved to 
  handle a wide range of applications, putting them in a class of their own.

This section is not intended to be a complete description of any of these
large areas, but rather a brief introduction to point you in the right
direction.

********************
System on Chip (SoC)
********************

Mobile processors and increasingly desktop processors are heterogenous
devices.  An extreme example is the recently announced
`NVIDIA Xavier SoC <https://developer.nvidia.com/embedded/buy/jetson-xavier-devkit>`_

* 8 Core CPU
* 8 SM Volta GPU
* Deep learning accelerator
* Programable vision accelerator (vector processing unit)
* Stereo and optic flow engine
* Image/signal processor

*****************
General Resources
*****************

There are some good online resources and conferences with the latest news
on hardware accelerators.

Websites
--------

* http://www.nextplatform.com : A website focused on HPC and large scale
  computing.  As heteregenous computing forms a large part of high end HPC,
  this is often a good place to follow upcoming trends.

Conferences
-----------

Computer architecture conferences:

* http://www.hotchips.com : Mainly industry presentations.

* http://www.isca.com : A conference with a more academic focus.

