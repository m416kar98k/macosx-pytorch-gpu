PyTorch GPU version is not natively supported on macOS. Furthermore, MacBook Pro GT 750M is also dropped due to its cc deficiency. The release is going to build from source in a similar environment and help developers save time from installation.

## Why I build for v1.4.0 not further version

My PI and Group AIMG are working on https://github.com/NiftyTorch/NiftyTorch.v.0.1. It is still at developing stage and requires PyTorch v1.4.0 by default.

## System Requirement

Make sure you are working on **Python 3.7**, **CUDA 10.0**, **CUDNN 7.4**, and macOS High Sierra.

My desktop with E3-1220 v3 and GTX 760 is very similar with Macbook Pro Mid 2015 with i7-4870HQ and GT 750M. I also keep my environment requirement consistent with https://github.com/TomHeaven/pytorch-osx-build. The only difference is my release works for cc 3.0, but his release will report an error ```no kernel image is available for execution on the device```.

## Installation

```brew install libomp```

```export LD_LIBRARY_PATH=/path-to-cudnn/lib:${LD_LIBRARY_PATH}```
