PyTorch GPU version is not natively supported on macOS. Furthermore GT 750M does not support PyTorch GPU version due to its cc deficiency. The release is going to build from source in a similar environment and help developers save time from installation.

## System Requirement

Make sure you are working on one of the following two environments, and macOS High Sierra.
(1) **Python 3.7**, **CUDA 10.0**, **CUDNN 7.4**
(2) **Python 3.6**, **CUDA 10.1**, **CUDNN 7.6**

```brew install libomp``` or ```conda install intel-openmp```

My desktop with E3-1220 v3 and GTX 760 is very similar with Macbook Pro Mid 2015 with i7-4870HQ and GT 750M. I also keep my environment requirement consistent with https://github.com/TomHeaven/pytorch-osx-build. The only difference is my release works for cc 3.0, but his release will report an error ```no kernel image is available for execution on the device``` because GT 750M is recognized but not supported by PyTorch v1.4.0 and requires a re-build.

## Why v1.4.0 but not further version

My PI and Group AIMG are working on https://github.com/NiftyTorch/NiftyTorch.v.0.1. It is still at developing stage and requires PyTorch v1.4.0 by default.
