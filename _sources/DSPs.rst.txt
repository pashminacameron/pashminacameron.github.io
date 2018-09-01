.. post:: Aug 30, 2018
   :tags: Hardware
   :author: Pashmina Cameron


Digital Signal Processors (DSPs)
================================

Whilst DSPs are mostly found in mobile platforms, they are an important for
of accelerator.

They are a processor typically made up of a number of parallel special
purpose blocks and are most useful in applications where a large number
of mathematical operations need to be performed quickly and repeatedly on
a data series.  Whilst they were originally designed to handle typical
analog data flows in activities such as wireless transmission and audio they
are very efficient at operations that are common in AI such as convolution.

There are specialist forms forms of DSP for individual markets:

* Video processing
* Audio processing
* Neural networks

However, DSP elements are most frequently found inside SoCs or as hard
IP with an FPGA.

* Qualcomm's SnapDragon mobile processors to provide AI services. `Qualcomm Neural Processing SDK <https://developer.qualcomm.com/software/qualcomm-neural-processing-sdk>`_

* Visual Processing for automotive applications. `Cadence VisionC5 <https://www.cadence.com/content/cadence-www/global/en_US/home/company/newsroom/press-releases/pr/2017/cadence-unveils-industrys-first-neural-network-dsp-ip-for-automo.html>`_


