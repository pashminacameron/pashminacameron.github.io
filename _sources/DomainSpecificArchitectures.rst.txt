.. post:: Aug 30, 2018
   :tags: Hardware
   :author: Pashmina Cameron

.. _page-dsa:

Domain Specific Architectures (DSAs)
====================================

Certain applications have sufficient demand to lead to the ultimate optmization
technique - designing hardware targeted at that one application.
Examples of this include:

* Cryptography accelerators
* Compression gngines
* Block chain hashers
* Neural networks

In reality, many DSAs are targeting fast moving application areas, and as
such a trade off is made between fixed purpose hardware and some level of
programablility.  However, these devices are still not suited for totally
general purpose usage like A CPU. Devices in this category include

* Network switch processors.  This is a big area with a lot of interesting
  architecture, but in most cases they are not suitable for accelerating
  workloads not closely coupled to network routing / filtering.
  
* `Intel's Exascale Dataflow engine <https://www.nextplatform.com/2018/08/30/intels-exascale-dataflow-engine-drops-x86-and-von-neuman/>`_ (hard to tell how domain specific this is yet)

* Vector processors such as Nec SX-Aurora.
  
A particularly big growth area for DSA is around neural networks:
  
* `Graphcore's AI processor <https://www.graphcore.ai/>`_

* `Google TPU <https://cloud.google.com/tpu/>`_ - Detailed description in Hennesy and Patterson.

* `ARM ML processors <https://developer.arm.com/products/processors/machine-learning/arm-ml-processor>`_

* `Mythic <https://www.nextplatform.com/2018/08/23/a-mythic-approach-to-deep-learning-inference/>`_ - An unsual hardware approach doing inference in the analog domain.

Many other NN accelerators are under development or already on the market, see Wikipedia `AI accelerator <https://en.wikipedia.org/wiki/AI_accelerator>`_

Another big area is image processing DSAs which have been around for a long
time.  Recent progress has been towards making them more programable and
flexible.

* `Google Visual Core <https://www.blog.google/products/pixel/pixel-visual-core-image-processing-and-machine-learning-pixel-2/>`_. 
* Most mobile SoCs have some level of programmable image processor.
  
Programming DSAs
----------------

The wide variety of different DSA architectures typically means that the
method used to work with each device is through a library.  Examples include
Tensorflow for Google's TPU.

Some DSAs have more general programing approaches such as
`Halide <http://halide-lang.org/>`_ for the Google Visual Core 
