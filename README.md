# ASL Gesture Recognition using Deep Learning

A deep learning project for recognizing American Sign Language (ASL) hand gestures from images. The project explores image classification using CNN-based techniques and transfer learning with MobileNetV2.

This project was developed as part of university Deep Learning coursework and is accompanied by an academic research paper covering the methodology, literature review, model design, evaluation, and results.

## Project Overview

Sign language recognition can help reduce communication barriers for people with hearing and speech impairments. This project focuses on recognizing static ASL hand gestures using computer vision and deep learning.

The implementation uses transfer learning with MobileNetV2 to take advantage of features learned from ImageNet and adapt them to ASL gesture classification.

## Key Features

- ASL hand gesture image classification
- MobileNetV2 transfer learning
- Image preprocessing and normalization
- Data augmentation
- Training and validation pipeline
- Fine-tuning of the pre-trained model
- Learning-rate adjustment during training
- Accuracy and loss visualization
- Model evaluation on test data

## Model Architecture

The project uses MobileNetV2 as the pre-trained feature extractor.

The general pipeline is:

```text
Input Image
    ↓
Image Preprocessing & Augmentation
    ↓
MobileNetV2 (ImageNet Pre-trained)
    ↓
Global Average Pooling
    ↓
Dense Layer
    ↓
Dropout
    ↓
Softmax Classification
```

The model is initially trained with the MobileNetV2 base frozen and is later fine-tuned using a lower learning rate.

## Data Augmentation

Data augmentation is used to improve generalization and reduce overfitting. Transformations include techniques such as:

- Rotation
- Width and height shifting
- Shearing
- Zooming
- Horizontal flipping

## Technologies Used

- Python
- TensorFlow
- Keras
- MobileNetV2
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Project Files

```text
ASL-Gesture-Recognition-Deep-Learning/
│
├── ASL_Gesture_Recognition_MobileNetV2.ipynb
├── Deep_Learning_Based_Sign_Language_Gesture_Recognition-2 (1).pdf
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Code-With-Salman/ASL-Gesture-Recognition-Deep-Learning.git
```

Move into the project directory:

```bash
cd ASL-Gesture-Recognition-Deep-Learning
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Then launch Jupyter Notebook and open:

```text
ASL_Gesture_Recognition_MobileNetV2.ipynb
```

## Dataset Setup

The dataset is not included in this repository because image datasets can be large.

Before running the notebook, download or prepare the ASL image dataset and update the dataset paths inside the notebook according to your local directory.

The project works with static hand gesture images organized into class-based folders for training and testing.

## Training

The training process includes:

1. Loading and preprocessing the image dataset.
2. Applying data augmentation.
3. Loading MobileNetV2 with ImageNet pre-trained weights.
4. Training the classification layers while the base model is frozen.
5. Fine-tuning selected layers using a lower learning rate.
6. Monitoring training and validation performance.
7. Evaluating the trained model on test data.

## Results

The project demonstrated that deep learning can effectively classify static sign language gestures. The accompanying research work reports an accuracy of approximately **90%** and discusses the role of data augmentation in improving model generalization.

Performance is evaluated using training and validation accuracy/loss along with classification-based evaluation techniques.

## Research Paper

This repository also includes the academic paper:

**Deep Learning-Based Sign Language Gesture Recognition**

The paper covers:

- Sign language gesture recognition
- Convolutional Neural Networks
- Transfer learning
- MobileNet/MobileNetV2
- Data augmentation
- Related research and comparative analysis
- Model methodology
- Evaluation and results
- Future improvements

The paper was prepared as part of the academic work associated with this project.

## Limitations

The current project focuses primarily on static hand gesture images. Real-world sign language recognition would require handling challenges such as:

- Dynamic gestures and video sequences
- Different lighting conditions
- Complex backgrounds
- Signer-to-signer variation
- Real-time inference

## Future Work

Possible improvements include:

- Real-time gesture recognition using a webcam
- Dynamic sign recognition from video
- Improved signer-independent recognition
- Lightweight deployment on mobile devices
- Testing additional transfer-learning architectures
- Building a real-time ASL interpretation interface

## Authors

**Mohammad Salman**  
Department of Artificial Intelligence  
University of Management and Technology (UMT), Lahore

## Note

This repository represents an academic Deep Learning project. The research paper included in the repository is provided as supporting academic documentation for the implementation.
