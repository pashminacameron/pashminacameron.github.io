.. post:: Aug 30, 2018
   :tags: Hardware
   :author: Pashmina Cameron

.. _gpu_label:
   
Graphics Processing Units (GPUs)
================================

   
Graphics processing units were one of the earliest forms of accelerator put
to general purpose use.  Initially this was entirely done by using / missusing
the graphics processing pipelines. This limited what could be done and lead
to some very creative algorithms (and incredibly capable programmers) to make progress under these limitations.

As graphics processors became more programmable (Vertex and Pixel Shaders) it
became possible to accelerate wider classes of algorithms, but this was still
a specialist field. The gains were sometimes huge, but the learning curve
was extremely steep. See `GPU Gems 2 <https://developer.nvidia.com/gpugems/GPUGems2/gpugems2_part04.html>`_  (that predated CUDA by 2 years)

More recently, a trend led primarily by NVIDIA has been the move to
General Purpose GPU (GPGPU) architectures in which hardware features have
been added to the chips specifically to make them suitable for use in more
general environments. This makes them more widely suited to applications that involve 
doing the same operations on a large amount of data in parallel. 

Accompanying software development kits such as `CUDA <https://developer.nvidia.com/cuda-zone>`_ 
and `OpenCL <https://www.khronos.org/opencl/>`_ have
exposed these features in a much more programmer-friendly way, making it easier 
for programmers to leverage the capabilities of GPUs.

**********************
GPGPU focused features
**********************

* Targetting HPC

  - Double Precision - driven by HPC / simulation markets, a very big customer
    for high end GPUs.

  - Special purpose interconnects NVLINK

* Targetting AI

  - Half Precision (FP16) - driven by AI where the lower precision can be
    sufficient and can allow near double the performance.

  - Tensor units.

* Targetting all users (helps for graphics as well)

  - High bandwidth memory (HBM), fast RAM DDR5

  - Support for shared virtual memory

In addition, NVIDIA has supported the development of various targeted libraries 
such as cuBLAS (CUDA BLAS) and cuDNN (Deep Neural Network library). 
This is a great example of the software hardware ecosystem co-evolving in order to get the best end result. 
