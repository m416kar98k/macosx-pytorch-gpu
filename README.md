# macosx-pytorch-gpu
Build from source for MacBook Pro

The latest MacBook Pro with NVIDIA Graphics card is MacBook Pro Mid-2015 with i7-4870HQ and GT 750M.
Unfortunately, GT 750M has a compute capability of 3.0, which has already been dropped from Facebook.
You have to build from source to get a CUDA support.

I followed instructions from https://github.com/TomHeaven/pytorch-osx-build.
His v1.4.0 release could return **True** for ```torch.cuda.is_available()``` function but will not actually work in model.
You will get an error ```no kernel image is available for execution on the device``` because your card is recognized but not supported.

## Why I build for v1.4.0?
Because my PI and his group are working on a project called NiftyTorch. It is still at developing stage and requires PyTorch v1.4.0 by default.

## What is different from TomHeaven's build?
My release would support compute capability 3.0. If your graphics card is not cc 3.0, please go to his repo. I believe his build is more stable.

## What is my desktop specification?
My desktop is very similar with Macbook Pro Mid 2015.
It is also based on Haswell E3-1220 v3 and a Kepler GTX 760.
I try to keep consistent with TomHeaven's build. If you already fulfill the requirement for his build, you can continue with my build.
I build with Python 3.7 (your version has to be 3.7), CUDA 10.0 (your version has to be 10.0), CUDNN 7.4.2 (your version has to be 7.4.1 or 7.4.2), and XCode 9.4.1 (you do not need to download it anymore).

## What else do you need to do after pip install?
Install libomp and add CUDNN lib to your LD_LIBRARY_PATH.
