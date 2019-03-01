# Seg-UNet(SegNet + UNet)
SegUNet is a model of semantic segmentation based on SegNet and UNet (these model are based on Fully Convolutional Network).
Architecture dedicated to restoring pixel position information.
This architecture is good at fine edge restoration etc.

This repository contains the implementation of learning and testing in keras and tensorflow.

## Architecture

This architecture is encoder-decoder model(29 conv2D layers).
- Skip connection(UNet) and indeces pooling(SegNet) are incorporated to propagate the spatial information of the image.


## Usage

### train

- Segmentation involving multiple categories

  `python train.py --options`

- Segmentation of mask image

  `python train_mask.py --options`

  - options

    - image dir
    - mask image dir
    - batchsize, nb_epochs, epoch_per_steps, input_configs
    - class weights
    - device num

