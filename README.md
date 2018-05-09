# tf_Medical-Image-Segmentation
This is detailed jupyter notebook that uses Tensorflow for medical image segmentation, in particular brain tumors.
The net trained with data from Brats2017

## Capabilities
* Has mini_batch parcelation
* Has tensorboard support
* Creates txt summary
* Multiple cost and accuray functions

## 1.  Data
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


## 2. Model
Helper functions implemented to build a model.
The model:

* Creates placeholders
* Initializes parameters
* Forward propagate
* Computes the cost
* Creates an optimizer

## 3. Results
![Alt text](notebook-images/results2018-05-09.png?raw=true "Current Results")


