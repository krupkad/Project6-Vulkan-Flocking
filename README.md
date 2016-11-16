Vulkan Flocking: compute and shading in one pipeline!
======================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 6**

* Daniel Krupka
  Debian testing (stretch), Intel(R) Core(TM) i7-4710HQ CPU @ 2.50GHz 8GB, GTX 850M

* Questions:
** Vulkan requires explicit descriptors for most things as, like memory, pipelines and commands and the like
are pre-allocated or pre-registered in order to guarantee that on-the-fly resource allocation/validation/controls
do not occur and cause unexpected latencies.
** Instancing, e.g. changing textures and parameters without changing shaders.
** Resources must be properly fenced to ensure that they are not invalidly in flight (e.g. being overwritten while being
used) in multiple contexts (e.g. different GPUs, different command queues).
** The largest benefit is more efficient visualization of compute results, e.g. displaying path tracer results without
much copying framebuffers from CUDA to GL.

### Credits

* [Vulkan examples and demos](https://github.com/SaschaWillems/Vulkan) by [@SaschaWillems](https://github.com/SaschaWillems)
