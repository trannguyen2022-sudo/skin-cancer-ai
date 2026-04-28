# skin-cancer-ai
# AI-Assisted Skin Cancer Detection System


Team members 
- Micen Desjardins
- Tran Nguyen
- Ashley Holness
- Toufique Ahmed
- Sarah Abuadas

## Overview
This project uses artificial intelligence to assist in the early detection of skin cancer through image classification with deep learning and explainable AI. The system uses MobileNetV2 with transfer learning to classify skin lesion images as benign or malignant. The goal is to support early diagnosis and improve patient outcomes by providing fast and reliable predictions.

THIS IS NOT A MEDICAL DIAGNOSIS TOOL.

## Objectives
+ The Problem: Skin cancer is among the most common cancers worldwide. Manual diagnosis depends on specialist availability, which is limited in many regions.
+ Why It Matters: Early detection dramatically improves survival rates. Millions lack timely access to dermatology expertise, especially in underserved areas
+ Our Goal: Build an AI screening tool that analyzes skin lesion images, predicts benign or malignant, and explains its reasoning. This improve early detection of skin cancer, and provide interpretable results that can assist healthcare professionals in decision-making.

## Dataset
Dataset: HAM10000
+ 10,000+ labeled skin lesion images
+ Multiple lesion types (dermoscopic)
+ Source: Kaggle
+ Reason: This dataset is widely used in medical imaging research and provides a strong foundation for training classification models.

## Model
Model: MobileNetV2 with Transfer Learning on ImageNet
+ Fast, lightweight, mobile-friendly
+ Transfer Learning is applied by using pre-trained weights, allowing the model to efficiently learn complex visual patterns in medical images.
+ Binary classification: Benign / Malignant
    + Benign lesions are non-cancerous and generally not harmful
    + Malignant lesions indicate the presence of skin cancer and require medical attention

## Methodology/Pineline
1. Data Prep:
   + Resize to 224×224 pixels
   + Normalize pixels from [0,255] down to [0,1]
   + Data Augmentation: flip/rotate/zoom
   + Split the data into training, validation, and test sets
     
2. Model Training:
   + Pretrained MobileNetV2 used as feature extractor (ImageNet weights)
   + Top classification layers added (Dense + Dropout)
   + Optimizer: Adam
   + Loss: Binary Crossentropy
   + Class imbalance handled using class weights
   + EarlyStopping and ReduceLROnPlateau used to prevent overfitting
    
3. Evaluation:
   + Metrics:
       - Accuracy
       - Precision
       - Recall
       - F1-score
   + Confusion Matrix used to analyze classification performance
   + Precision-Recall curve used due to class imbalance
     
4. Explainability:
   + Grad-CAM (Gradient-weighted Class Activation Mapping) used
   + Highlights regions of the image influencing predictions
   + Helps interpret model decisions and improve trust

## Results 
+ The model achieved approximately 82% accuracy on the test set, demonstrating effective classification performance.
+ Higher recall for the malignant class was prioritized to reduce false negatives, which is critical in medical screening.
+ Overall, the model shows strong potential as a supportive screening tool, though further validation and improvement are needed for real-world use.

## Conclusion 
In conclusion, this project demonstrates the potential of AI in improving early detection of skin cancer using deep learning. The model achieved approximately 82% accuracy, showing its ability to distinguish between benign and malignant lesions. While it is not a replacement for medical professionals, it can significantly assist in diagnosis and help support faster, more accessible screening. With further improvements, this approach has the potential to contribute to better patient outcomes and potentially save lives.

## Links:
Google Collab: https://colab.research.google.com/drive/1bpAoKoNzt9mB4ojcODF8yygnJNX9P3ei?usp=sharing

Powerpoint: https://1drv.ms/p/c/bd672e9d0a8f5bcd/IQBvW_EbyrBfQL3DRyIo_jhSAWDwjCaaZNZCGnMO19edr2k?e=d4z2u4

Youtube video:


