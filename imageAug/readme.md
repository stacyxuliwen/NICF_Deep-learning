This work refers to the (slightly modified) pre-process of retina images by Dr. Graham's https://www.kaggle.com/c/diabetic-retinopathy-detection/discussion/15801 and implemented here https://github.com/usuyama/pydata-medical-image/blob/master/diabetic_retinopathy/scripts/preprocess.py.
- Estimate radius of the circle
- Resize all images
- Crop to squares
- Subtracted the local average color with more focus / attention: the local average gets mapped to 50% gray
- Remove outer boundary (keep 90%)

This work generated augmentated image dataset with modified version of keras' ImageDataGenerator with histogram balancer here https://towardsdatascience.com/image-augmentation-for-deep-learning-using-keras-and-histogram-equalization-9329f6ae5085.

We used training split utility from https://github.com/kouml/keras-split-utils to be used with above image data generator.
