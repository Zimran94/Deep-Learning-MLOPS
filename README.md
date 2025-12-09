# Deep-Learning-MLOPS
Trained a deep learning model that detects mango leaf diseases, tracked our experiments using MLflow, versioned data &amp; models using DVC, and saved everything in GitHub with proper MLOps practices.


Project Overview
🔍 Goal

Automatically classify mango leaf images into eight disease categories using Deep Learning.

🧠 Model Used

ResNet50V2 (ImageNet pretrained)

Custom residual dense layers

Gradual unfreezing

Warmup + Cosine Learning Rate Schedule

🗂 Dataset

The dataset contains images classified into 8 disease categories:

Anthracnose
Bacterial Canker
Cutting Weevil
Die Back
Gall Midge
Healthy
Powdery Mildew
Sooty Mould

Dataset was preprocessed using:

Rotation (up to 45°)  
- Width/height shift (20%)  
- Zoom (20%)  
- Horizontal & vertical flip  
- Brightness shift (0.7 → 1.3)  
- Channel shift  
- Shear transformation  

🧩 Architecture

✔ ResNet50V2 base
✔ Global Average Pooling
✔ BatchNorm + Dropout
✔ Residual dense blocks (1024 → 512 → 256)
✔ Softmax output layer

⚙ Model Training
Training features:

Early stopping

Gradual Layer Unfreezing

Warmup + Cosine decay

Class weights

Image augmentation

Label smoothing

📊 Model Performance 
Metrics 

Accuracy - 96%

Loss - 0.12

AUC - 0.99

Precision - 95%

Recall -95%

Confusion matrix
