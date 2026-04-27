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

## Objective
+ The Problem: Skin cancer is among the most common cancers worldwide. Manual diagnosis depends on specialist availability, which is limited in many regions.
+ Why It Matters: Early detection dramatically improves survival rates. Millions lack timely access to dermatology expertise, especially in underserved areas
+ Our Goal: Build an AI screening tool that analyzes skin lesion images, predicts benign or malignant, and explains its reasoning. This improve early detection of skin cancer, and provide interpretable results that can assist healthcare professionals in decision-making.

## Dataset
Dataset: HAM10000
+ 10,000+ labeled skin lesion images
+ Multiple lesion types (dermoscopic)
+ Source: Kaggle
+ Reason: This dataset is widely used in medical imaging research and provides a strong foundation for training classification models.

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
     
2. Model Trainning:
    +
3. Evaluation:
4. Explainability:
5. Links: 





