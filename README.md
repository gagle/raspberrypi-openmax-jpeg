openmax-jpeg
============

#### An OpenMAX IL example that captures a JPEG image with a Raspberry Pi ####

The Multi-Media Abstraction Layer (MMAL) library provided by Broadcom is not documented, so it's nearly impossible to understand how to use it. Furthermore, it's a library that wraps all the OpenMAX IL specification, so if you simply need to capture a JPEG image like in this example, you can just ignore that extra layer and talk directly to OpenMAX IL. Once you understand OpenMAX IL, it's affordable to try to write your own programs without MMAL. In other words, if you are new to the OpenMAX world, it's better to learn OpenMAX IL than MMAL, which is not documented and only works with Broadcom devices.

This example captures an image in a JPEG format. The components involved are: `camera` and `image_encode`. The `image_write` component doesn't work correctly or I don't understand how to use it. I always get the error `OMX_ErrorInsufficientResources` when I change the `image_write` state from LOADED to IDLE.

Build steps:

- Download and install the `gcc` and `make` programs.
- Download this repository.
- Compile and execute: `make && ./jpeg`

Useful documentation:

- [OpenMAX IL Specification v1.1.2](https://www.khronos.org/registry/omxil/specs/OpenMAX_IL_1_1_2_Specification.pdf)
- [Understanding OpenMAX IL](http://www.slideshare.net/pchethan/understanding-open-max-il-18376762)
- [Broadcom OpenMAX IL components](https://github.com/raspberrypi/firmware/tree/master/documentation/ilcomponents)
- [OpenMAX IL header files](https://github.com/raspberrypi/firmware/tree/master/opt/vc/include/IL)