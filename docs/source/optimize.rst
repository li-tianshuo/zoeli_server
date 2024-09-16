Using Server GPU Resources 
==============================

Check GPU Usage
------------------------------------

To check if there are other tasks or your tasks is executed by GPU. Please type following command in server terminal.

.. code-block:: console
  
    nvidia-smi

Ongoing tasks will listed in compute processes section.


Optimization Your Code with GPU
------------------------------------

General Python Code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can use CUDA JIT to boost your general python function. Here is a example:

.. code-block:: python
  
    from numba import jit

    @jit
    def f(x, y):
        # A somewhat trivial example
        return x + y

The documentation of CUDA JIT can be found in `here <https://numba.readthedocs.io/en/stable/user/jit.html>`_.

Segment Anything Model (SAM)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Segment Anything Model is a powerful computer vision model for image Segmentation. However, the example code is not GPU in default, here is a example to let SAM model execute by GPU.

.. code-block:: python
  
    from segment_anything import SamPredictor, sam_model_registry
    sam = sam_model_registry["vit_h"](checkpoint="sam_vit_h_4b8939.pth")
    sam.to(device = "cuda")


PYMC
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
PYMC is a python package in statistical data science and it can used to construct Bayesian model. It took long time in sampling with default method, and this `blog post <https://www.pymc-labs.com/blog-posts/pymc-stan-benchmark/>`_ presented performance of other sampling method in PYMC with GPU.