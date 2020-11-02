# TensorFlow implementation of the U-net

[![Build Status](https://travis-ci.com/zaccharieramzi/tf-unet.svg?branch=master)](https://travis-ci.com/zaccharieramzi/tf-unet)

The U-net is a network introduced by Olaf Ronneberger et al. in “U-Net: Convolutional Networks for Biomedical Image Segmentation”, MICCAI 2015.
If you use this network, please cite their work appropriately.

A change when compared to the initial architecture is that we use zero-padding to keep a constant image size.


There are lots of unofficial implementation of the U-net all over the web, here are some examples with comments:

- in [Keras](https://github.com/zhixuhao/unet/blob/master/model.py), however this model is not very modular.
- in [PyTorch](https://github.com/milesial/Pytorch-UNet/blob/master/unet/unet_model.py), again this model is not very modular off-the-shelf.
- in [TF v1.x](https://github.com/jakeret/tf_unet/blob/master/tf_unet/unet.py).
- in [TF v2.x](https://github.com/jakeret/unet/blob/master/src/unet/unet.py), by the same people as above.
- and [many more...](https://github.com/search?q=u-net)


The goal of this implementation in TensorFlow is to be easy to read and to adapt:

- all the code is in one file
- defaults are those from the paper (for gray image denoising)
- there is no other imports than from TensorFlow
