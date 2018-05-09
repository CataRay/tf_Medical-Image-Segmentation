# tf_Medical-Image-Segmentation
Use Tensorflow for medical image segmentation. In particular brain tumors.
The net trained with data from Brats2017
## Capabilities
* Has mini_batch parcelation
* Has tensorboard support
* creates txt summary
* multiple cost and accuray functions

1.  Data
The data is loaded from the folder:

/data/Brats17TrainingData/Flair_HGG/flair.nii.gz
/data/Brats17TrainingData/Flair_HGG/seg.nii.gz

The size of the images is [240x240x155] and there are 208 Nifti files. Therefore the total number of images is 32240.

Labels in the seg files are:

* Label 1: necrotic and non-enhancing tumor
* Label 2: edema
* Label 4: enhancing tumor
* Label 0: background

All label were simplified to 1 before creating the hdf5 files. Anything not background will be segemented as tumor.


2. Model
Helper functions implemented to build a model.
The model:

* creates placeholders
* initializes parameters
* forward propagate
* computes the cost
* creates an optimizer
