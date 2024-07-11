# Brain Tumor Segmentation on MRI Images

Welcome to the Brain Tumor Segmentation project! This project aims to segment brain tumors from MRI images using advanced deep learning techniques.

## Introduction
Brain tumor segmentation from MRI images is a crucial task in medical image analysis. Accurate segmentation helps in diagnosis, treatment planning, and follow-up of brain tumors. This project leverages deep learning techniques, specifically the 3D U-Net architecture and contextual transformers, to achieve high-quality segmentation.

## Features
- Proposed preprocessing methods on MRI images.
- Accurate Segmentation: High precision in segmenting brain tumors from MRI images.
- 3D U-Net Architecture: Utilizes a 3D U-Net for capturing spatial information.
- Analysis of some segmentation error cases.

## Dataset
We use the BraTS2020 dataset ([kaggle](https://www.kaggle.com/datasets/awsaf49/brats2020-training-data?resource=download), [CBICA](https://www.med.upenn.edu/cbica/brats2020/data.html)), multimodal images to train the model.

Below are some samples from the dataset:

![bbb](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/bf8d1763-1ca2-4624-ad69-578a5788fc16)


| Some samples | 3D image | 
|:-|:-|
|![sma](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/f4d215dd-7b5f-4ce3-a50f-af3ef70542ea) | ![3dimg](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/44035826-f6c0-4d28-8b2f-80b3d9f64528) |

__*Preprocessing*__

| 1. Crop volums: Remove unimportant background parts to optimize costs and help the model focus on the brain. | 2. Combine image: we do not combine the T1 method because this image carries quite little useful information, most of the valuable information is already in the remaining methods | 
|:-|:-|
| ![crop](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/dbeed92a-809b-440a-817b-1812cf15e0ad)| ![comb](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/a30555bc-a6a6-4b05-a7e7-cb5c23c6f29d)|


## Functions of each code file
- Survey.ipynb: Initial data survey file.
- ExtractionAndTrainNomal.ipynb: Code for surveying some data points and building a U-Net model for the initial data.
- Pre-Processing.ipynb: Used for data preprocessing.
- GenDataAndTrainAfterProcess.ipynb: Proceeds to build a 3D U-Net model for the preprocessed data.


## Technologies Used
- Python: Core programming language.
- Keras: Deep learning frameworks used for model training and inference. [3D U-Net model](https://arxiv.org/pdf/1606.06650)
- Numpy: For numerical computations.
- Matplotlib: For visualizing the results.

## Result

| Some good case | Some not good case | 
|:-|:-|
|![gog](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/e7565c56-d6cc-4063-a0c0-1bd93224102e) |![bad](https://github.com/PoLsss/Medical-Image-Processing/assets/98370447/d0b0f9da-c251-46fd-936a-9d97080a3857)|


*"This is the Medical Image Processing course project - It is the result of the group members' work."*
