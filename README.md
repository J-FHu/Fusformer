# Fusformer
Code for the paper: "Fusformer: A Transformer-based Fusion Approach for Hyperspectral Image Super-resolution"

Plateform: Python 3.8.5 + Pytorch 1.7.1

* demo_cave.h5: A testing image from the CAVE dataset, containing "GT" ( 512x512x31), "RGB" (128x128x3) and "LRHSI" (128x128x31).
* demo_cave_patches_h5: If your GPU memory is too small to run with the whole testing image, we cut the testing image into 64 patches with the size 64x64x31 of GT, 63x64x3 of RGB, and 16x16x31 of LRHSI, respectively.

Download link: https://github.com/J-FHu/Fusformer/releases/tag/Pytorch
----------------------------------------------------------------------------
* data.py: The dataloader of the training and testing data.
* main.py: The training and testing function of our Fusformer.
* model.py: The whole model of our Fusformer.
* reshape2big.m : If you use the "demo_cave_patches.h5" as the testing data, the output ("PatchOutput-cave.mat") generated by the network will be 64 patches with the size of 64x64x31, which should be reshaped to the original size of 512x512x31.
