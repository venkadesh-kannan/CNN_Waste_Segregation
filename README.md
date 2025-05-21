# CNN_Waste_Segregation
## **Objective**

The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

The key goals are:

* Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
* Improve waste segregation efficiency to support recycling and reduce landfill waste.
* Understand the properties of different waste materials to optimise sorting methods for sustainability.

## **Data Understanding**

The Dataset consists of images of some common waste materials.

1. Food Waste
2. Metal
3. Paper
4. Plastic
5. Other
6. Cardboard
7. Glass


**Data Description**

* The dataset consists of multiple folders, each representing a specific class, such as `Cardboard`, `Food_Waste`, and `Metal`.
* Within each folder, there are images of objects that belong to that category.
* However, these items are not further subcategorised. <br> For instance, the `Food_Waste` folder may contain images of items like coffee grounds, teabags, and fruit peels, without explicitly stating that they are actually coffee grounds or teabags.

  #### **5.1 Conclude with outcomes and insights gained** 
* Report your findings about the data
Dataset Structure:
Images are organized in subdirectories like a tree, each representing a class label.

Example structure:
dataset/
├── class_1/
├── class_2/
└── class_3/

Class Distribution:
A bar plot was used to visualize the number of images per class.
This helps identify class imbalance, which can affect model performance.

Image Dimensions:
The dataset contained images of varying sizes.
Smallest and largest dimensions were identified.
All images were resized to a uniform shape (e.g., 224×224) for model input.

Label Encoding:
Class labels (folder names) were encoded into numerical values using LabelEncoder.

* Report model training results

Model Training Results

Model Architecture:
A CNN with 3 convolutional layers was built.
Included:
Batch Normalization after each convolution
MaxPooling layers
Dropout for regularization
Dense layers for classification
Softmax output for multi-class classification

Compilation:
Optimizer: Adam
Loss: categorical_crossentropy
Metrics: accuracy

Training Process:
Data was split into training and validation sets.
ImageDataGenerator was used for rescaling and augmentation.
Model was trained using model.fit() with validation monitoring.

Evaluation on Test Set:
Metrics computed:
Accuracy
Precision
Recall
F1-score
