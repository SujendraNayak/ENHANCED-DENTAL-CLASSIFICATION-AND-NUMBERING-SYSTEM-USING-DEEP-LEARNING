###🦷 ENHANCED DENTAL CLASSIFICATION AND NUMBERING SYSTEM USING DEEP LEARNING
📌 Introduction
The Enhanced Dental Classification and Numbering System Using Deep Learning aims to revolutionize dental healthcare by automating dental X-ray analysis. Traditional dental classification methods are manual, time-consuming, and prone to human errors. This system leverages deep learning (CNN) to accurately classify dental features and automatically assign tooth numbers based on standardized numbering systems.

✅ Key Features:

Automated detection of teeth and dental features.

Tooth numbering using FDI World Dental Federation notation.

Accurate classification of dental conditions (crowns, cavities, root canals, etc.).

Integration with dental records for clinical use.

🛠 Methodology
1️⃣ Data Collection and Preprocessing
Dental X-rays collected from public datasets and hospitals.

Images annotated for tooth positions and conditions.

Preprocessing steps:

Resizing images to a fixed resolution.

Normalization for uniform pixel intensity.

Data Augmentation: Rotation, flipping, and zooming to improve generalization.

2️⃣ Model Architecture
Backbone network: ResNet 50/101 with FPN (Feature Pyramid Network).

Region Proposal Network (RPN) for generating candidate tooth regions.

RoI Align for feature extraction and segmentation.

Three branches:

Mask: For tooth segmentation.

Coordinates: For bounding box regression.

Category: For classification of teeth.

📌 Architecture Diagram:
<img width="1725" height="609" alt="image" src="https://github.com/user-attachments/assets/71365237-951b-4326-ad4f-0a9765cc39da" />


3️⃣ Tooth Classification & Numbering
Assigns tooth numbers using FDI notation.

Segments teeth with masks for better visualization.
<img width="1821" height="1007" alt="image" src="https://github.com/user-attachments/assets/5b5236d0-dd0e-4778-8688-a1adaee0215d" />



4️⃣ Training and Validation
Optimizer: Adam

Loss function: Cross-Entropy Loss

Split: 80% training, 20% validation

Regularization: Dropout to prevent overfitting.

📉 Loss Curve:
<img width="1412" height="767" alt="image" src="https://github.com/user-attachments/assets/a7d440f1-4f81-46de-a64f-500e56846922" />


5️⃣ Results
Achieved high accuracy in tooth detection and numbering.

Generated clear segmentation masks and bounding boxes with confidence scores.
<img width="1241" height="673" alt="image" src="https://github.com/user-attachments/assets/363c2cf4-8ad0-4c5a-843c-2fe4fdcfb9b5" />

6️⃣ Deployment
User-friendly web interface for dentists to upload X-rays.

Integration with electronic dental records (EDRs) for seamless workflow.

🚀 Technologies Used
Python

TensorFlow / Keras

OpenCV (image preprocessing)

ResNet + FPN + Mask R-CNN

Matplotlib & Seaborn (visualizations)
