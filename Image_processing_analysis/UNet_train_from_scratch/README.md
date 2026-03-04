# U-Net Image Segmentation (From Scratch)

This project implements a U-Net convolutional neural network from scratch in PyTorch for image segmentation. The model was trained on the Oxford-IIIT Pet dataset to segment foreground objects (pets) from the background. 

U-Net is a popular architecture for semantic segmentation, especially in biomedical and object segmentation tasks. It consists of an encoder–decoder structure with skip connections that help preserve spatial information during upsampling. Mask preprocessing operation is used to convert the dataset labels into binary masks: Background as 0; Pet (object) as 1.

## Training Setup

Framework: PyTorch
Optimizer: Adam
Loss function: BCEWithLogitsLoss + UNet Loss
Metric: Intersection over Union (IoU)
Learning rate scheduler: ReduceLROnPlateau

## Performance Metrics

The model converged successfully and achieved strong segmentation performance.The final Validation IoU was ~0.90–0.91.

The best model checkpoint is available as Unet_BEST_oxfordpet.pth

## Future Improvements

Possible extensions:

1. Train with larger datasets and apply stronger data augmentation

2. Experiment with attention U-Net variants