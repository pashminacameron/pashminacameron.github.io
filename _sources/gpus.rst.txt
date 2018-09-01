.. post:: Aug 30, 2018
   :tags: Hardware
   :author: Pashmina Cameron

.. _gpu_label:
   
Graphics Processing Units (GPUs)
================================

   
Graphics processing units were one of the earliest forms of accelerator put
to general purpose uses.  Initially this was entirely done by using / missusing
the graphics processing pipelines.   This limited what could be done and lead
to some very creative algorithms to make progress under these limitations.

As graphics processors became more programmable (Vertex and Pixel Shaders) it
became possible to accelerate wider classes of algorithms, but this was still
a specialist field. The gains were sometimes huge, but the learning curve
was extremely steep. `GPU Gems 2 <https://developer.nvidia.com/gpugems/GPUGems2/gpugems2_part04.html>`_  (predating CUDA by 2 years)

More recently, a trend led primarily by NVIDIA has been the move to
General Purpose GPU (GPGPU) architectures in which hardware features have
been added to the chips specifically to make them suitable for use in more
general environments.  Software approaches such as `CUDA <https://developer.nvidia.com/cuda-zone>`_ and `OpenCL <https://www.khronos.org/opencl/>`_ have
exposed these features.

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

  - High bandwidth memory (HBM), fast ram DDR5

  - Support for shared virtual memory
