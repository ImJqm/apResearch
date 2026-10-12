---
created: 2026-10-11 21:19
modified: 2026-10-11 21:24
---
The current method  looks something like the following

We precompute some sort of 3D scene  of a rotating UV Sphere on the CPU with high precision, making sure to save both  rasterized output as PNGs as well as the  actual point cloud data

Then, using cupy, we will leverage  GPU  calculations to write something known as a `RawKernel`  to write a specific custom GPU function to do 3D coordinate transformaitons  on our UV sphere

We will run a warmup calculation of the kernel process

We want to inject 2 GPU events before and after the kernel process, then we will synchronize our CPU program with the gpu.

Then we can compute the $dt$ for each frame, making sure to store the point cloud and rasterized PNG as well.

We repeat this process, making sure to rotate $\forall \theta$ in our bounds(yet to be determined)

We will then repeat for each trigonometric approximation