# Projects

ML/DL projects

# Plant Doctor

Plant Health is very important when it comes to setting up a hydroponics system to grow vegetables.
Given rising populations and shortages in food due to disastrous climate events, we aim to create an easy to assemble and maintain growing 
system. A crucial part of the system is the ability to quickly identify issues with the specific plant and take a course of action to nurse 
it back to health or avoid the other plants from being infected


Will integrate with Raspberry pi setup which includes humidity, pH and temperature sensors. As well as, control of the frequency of light 
and length of time light is on based on scheduler. Once we have the data from all these endpoints we can create a comprehensive deep 
learning model to have an effective and repeatable setup.

To run jupyternotebook, follow FASTAI guide for virtual cloud instance, found here:

https://github.com/fastai/fastai/blob/master/README.md#installation

### Conda Install

```bash
conda install -c pytorch -c fastai fastai
```

This will install the `pytorch` build with the latest `cudatoolkit` version. If you need a higher or lower `CUDA XX` build (e.g. CUDA 9.0), following the instructions [here](https://pytorch.org/get-started/locally/), to install the desired `pytorch` build.

Note that JPEG decoding can be a bottleneck, particularly if you have a fast GPU. You can optionally install an optimized JPEG decoder as follows (Linux):

```bash
conda uninstall --force jpeg libtiff -y
conda install -c conda-forge libjpeg-turbo
CC="cc -mavx2" pip install --no-cache-dir -U --force-reinstall --no-binary :all: --compile pillow-simd
```
If you only care about faster JPEG decompression, it can be `pillow` or `pillow-simd` in the last command above, the latter speeds up other image processing operations. For the full story see [Pillow-SIMD](https://docs.fast.ai/performance.html#faster-image-processing).

### PyPI Install

```bash
pip install fastai
```

By default pip will install the latest `pytorch` with the latest `cudatoolkit`. If your hardware doesn't support the latest `cudatoolkit`, follow the instructions [here](https://pytorch.org/get-started/locally/), to install a `pytorch` build that fits your hardware.

### Bug Fix Install

If a bug fix was made in git and you can't wait till a new release is made, you can install the bleeding edge version of `fastai` with:

```
pip install git+https://github.com/fastai/fastai.git
```
If you have a good GPU and would like to save money, you can run it off Windows:

https://forums.fast.ai/t/howto-installation-on-windows/10439/18


This dataset was acquired from spMohanty's GitHub Repo
https://github.com/spMohanty/PlantVillage-Dataset

# Winner
Quick Data Analysis on US lottery.

