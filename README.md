# Simple ArcFace Tutorial

Based on: [face.evoLVe](https://github.com/ZhaoJ9014/face.evoLVe/tree/master)


`ArcFace is applied to the problem of face recognition.`

### Introduction

<image src = "illustration\image_1.png">

Deep Convolutional Neural Networks (DCNN) have become a popular choice for extracting facial features and have proven to be highly effective in this task. The next step is to classify these feature vectors accurately to improve facial recognition. There are two main approaches: one involves creating an additional classification model, such as using softmax, while the other involves directly training the model using embedding vectors, like with triplet loss. Both methods have shown good results but have notable drawbacks.

Using softmax increases the size of the linear transformation matrix proportionally to the number of identities to classify, making it effective for closed-set classification (when the input and output classes are fixed) but less practical for scenarios where the number of different faces (classes) changes. Triplet loss addresses this issue but has its own challenges. As it compares three samples at a time, the number of triplets increases exponentially with the data, leading to more iterations. Additionally, the semi-hard sample training, which is considered optimal for triplet loss, is challenging to train effectively. Due to these shortcomings, researchers have proposed a new direction for facial recognition by introducing a new loss function called Additive Angular Margin Loss.

<image src = "illustration\image_2.png">

### Principle of face recognition

Here we use the One-Shot technique

+ We have a default dataset of photos of people that we need to perform recognition.
<image src = "illustration\image_4.png">

+ Each face will have a feature vector given by the model.
<image src = "illustration\image_5.png">

+ When there is a new photo of anyone, that new photo is fed into the model and produces a feature vector, calculating the similarity between that vector and each original vector in the default dataset.
<image src = "illustration\image_6.png">

`Testing method for ArcFace model as above.`

### Training implementation

<image src = "illustration\image_3.png">

# Contribute

**Author:** Ha Khai Hoan 
**Nation:** Viet Nam  
**Email:** [khaihoan.ai@gmail.com](mailto:khaihoan.ai@gmail.com)  
**Github:** [hoanha2101](https://github.com/Hoanha2101)