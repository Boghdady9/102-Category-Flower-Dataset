# 102 category-flower-dataset classifcation

## 1. Introduction
This is a simple image classification project using the [102 Category Flower Dataset](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html). The dataset contains 102 flower categories commonly occuring in the United Kingdom. Each class contains between 40 and 258 images. The images have large scale, pose and light variations. In addition, there are categories that have large variations within the category and several very similar categories. The dataset is visualized using isomap with shape and colour features.


## 2. Dataset
The dataset contains 102 flower categories commonly occuring in the United Kingdom. Each class contains between 40 and 258 images. The images have large scale, pose and light variations. In addition, there are categories that have large variations within the category and several very similar categories. The dataset is visualized using isomap with shape and colour features.

## 3. preprocessing
The images are restructured into a folder with the following structure:
```
├── training
│   ├── class_1
│   │   ├── image_1
│   │   ├── image_2
│   │   └── ...
│   ├── class_2
│   │   ├── image_1
│   │   ├── image_2
│   │   └── ...
│   └── ...
├── validation
│   ├── class_1
│   │   ├── image_1
│   │   ├── image_2
│   │   └── ...
│   ├── class_2 
│   │   ├── image_1
│   │   ├── image_2
│   │   └── ...
│   └── ...
└── testing
    ├── class_1
    │   ├── image_1
    │   ├── image_2
    │   └── ...
    ├── class_2 
    │   ├── image_1
    │   ├── image_2
    │   └── ...
    └── ...
```
## 4. data augmentation
The images are augmented using the following transformations:
- RandomHorizontalFlip
- RandomAffine
- RandomCrop
- Resize

## 5. Model
The pre-trained model is convformer_s18. The model is fine tuned for 20 epochs with a batch size of 32. The the Adam optimizer is used with a learning rate of 0.0001.

## 6. Results
The model achieves an accuracy of 87% on the test set.
