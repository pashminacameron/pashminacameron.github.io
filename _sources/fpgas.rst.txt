.. post:: Aug 30, 2018
   :tags: Hardware
   :author: Pashmina Cameron

.. _page-fgpas:

Field Programmable Gate Arrays (FPGAs)
======================================

We will use the term FPGA to cover the class of programmable hardware
which can be used to implement almost any digital circuit at runtime.
This means that the hardware architecture can be optimized to the precise
use case, allowing flexibility around variable precision and vector width
across the pipeline and massive amounts of controlled parallelism.

There are two major manufacturers of FPGAs who are both focussing heavily
on their usage as compute accelerators:

* `Xilinx <http://www.xilinx.com>`_
* `Altera <http://www.altera.com>`_ (now part of Intel)

As you will see much of the following divides into the different approaches
each of these players has taken.

*****************************
What can you do with an FPGA?
*****************************

Modern FPGAs are a mixture of 

* Hard IP (not reprogrammable): which are somewhat general purpose components, such as memory or arithmetic units 
* Soft IP (reprogrammable): such as Logic Gate arrays in which you can implement general digital circuits 

This combination allows for much better speed, space and power efficiency.

The main advantages over Domain Specific Architectures are:

* Enabling compute on demand as the cost of the FPGA hardware can be shared by
  a large number of different applications.  Hence we get the rapid scale up
  options in the cloud that we are used to for CPU instances.

* Flexiblity as your requirements change.  This leads to very fast turn around.
  FPGAs are suited for approaches such as agile development that are not
  possible when timescales to do make a new chip are involved. Simply reprogramming the FPGA is sufficient. 

**********************
Programming an FPGA
**********************

FPGAs have traditionally been programmed using hardware description languages
such as `Verilog <https://en.wikipedia.org/wiki/Verilog>`_ and
`VHDL <https://en.wikipedia.org/wiki/VHDL>`_.
These are also the languages used to describe
hardware which will become an actual chip.  Whilst extremely powerful, they
represent a steep enough learning curve for an experienced software engineer
that a lot of research and development has gone into tools and compilers to
make the FPGA development workflow closer to that developers are already
familiar with.

C++ / OpenCL
************

A number of projects exist to take OpenCL code and compile it into the
hardware description that is programmed to the FPGA:

**Altera**

* `OpenCL SDK <https://www.intel.com/content/www/us/en/software/programmable/sdk-for-opencl/overview.html>`_
* `FPGA HPC using OpenCL: Case Study in 3D FFT <https://www.bu.edu/caadlab/HEART18a.pdf>`_ - Ahmed Sanaullah and Martin Herbordt

**Xilinx**

* `SDAccel <https://www.xilinx.com/products/design-tools/software-zone/sdaccel.html>`_
* `Simultaneous multiprocessing in a software-defined heterogeneous FPGA <https://link.springer.com/article/10.1007/s11227-018-2367-9>`_ - Jose Nunez-Yanez et l. 

********************
Connectivity options
********************

Here we are mostly interested in the potential to accelerate an existing
algorithm by using an FPGA to accelerate some elements whilst a conventional
CPU is responsible for the full program and FPGA management etc.  Hence
we will focus on those 

CPU integrated FPGAs
********************

Intel has annouced a variant of the Xeon CPU that includes, in package
a large FPGA. See 
`Intel Xeon FPGA Hybrid cip <https://www.nextplatform.com/2018/05/24/a-peek-inside-that-intel-xeon-fpga-hybrid-chip/>`_.

Xilinx has a range of products integrating CPUs directly within the FPGA
and provides good support for running Linux on these. See 
`Xilinx Ultrascale MPSOC <https://www.xilinx.com/products/silicon-devices/soc/zynq-ultrascale-mpsoc.html>`_.

Expansion bus connected accelerators
************************************

Currently most FPGA accelerators are attached to normal servers via the PCIe
bus at Gen 3.0 speeds. All the major devices are available in this form factor.
Gen 4.0 PCIe devices are starting to become available.

Emerging interconnect options such as 
`Intel QPI <https://www.intel.com/content/www/us/en/io/quickpath-technology/quickpath-technology-general.html>`_, 
`OpenCAPI 2.0 <https://opencapi.org/>`_ and `CCIX <https://www.ccixconsortium.com/>`_ 
allow for coherent caches with the CPUs, greatly accelerating some types of applications.


Example Systems / Usecases
**************************

* `Project Catapult - Microsoft <https://www.microsoft.com/en-us/research/project/project-catapult/>`_

* `Project Brainwave - Microsoft <https://www.microsoft.com/en-us/research/uploads/prod/2018/06/ISCA18-Brainwave-CameraReady.pdf>`_

* `List of Xilinx Based Cloud Server Offerings <https://www.xilinx.com/products/design-tools/cloud-based-acceleration.html>`_ includes Alibaba, Amazon, Baidu, Huawei, Nimbix and Tencent





