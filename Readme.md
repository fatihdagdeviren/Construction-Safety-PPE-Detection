Construction Safety Detection with YOLOv8
This repository contains a YOLOv8 model trained for detecting various safety-related equipment in a construction environment. The model is designed to detect the presence of personal protective equipment (PPE) such as hardhats, masks, safety vests, and also identify vehicles, machinery, and workers. This can be used to monitor compliance with safety protocols on construction sites.

Model Overview
The YOLOv8 model is trained on a custom dataset consisting of different safety equipment and personnel categories. It was optimized to detect and classify the following objects:

Hardhat
Mask
No-Hardhat
No-Mask
No-Safety Vest
Person
Safety Cone
Safety Vest
Machinery
Vehicle
Results
Training Metrics
The model was trained over 100 epochs, and the training and validation losses (box, classification, DFL) showed steady convergence, indicating strong learning patterns. Precision, recall, and mean Average Precision (mAP) metrics improved consistently as shown in the loss and metric graphs below:


Precision: 0.79
Recall: 0.70
mAP@50: 0.79
mAP@50-95: 0.49
These metrics demonstrate the model's ability to accurately detect and classify safety equipment in the validation set, with particularly high precision across all classes.

F1-Confidence Curve
The F1-Confidence curve below shows the model's performance across varying confidence thresholds. The optimal F1 score of 0.79 was achieved at a confidence level of 0.443 for all classes combined.


Individual class performance varies, with some categories like "Mask" and "Safety Vest" showing excellent F1 scores close to 0.9, while others such as "No-Hardhat" or "Vehicle" performed slightly lower but still effective for real-world detection.

Dataset
The dataset used for training was manually labeled and included both positive examples (e.g., workers with proper PPE) and negative examples (e.g., workers without safety equipment). The images were collected from diverse sources, including construction sites under different lighting and environmental conditions.

Classes
Hardhat
Mask
No-Hardhat
No-Mask
No-Safety Vest
Person
Safety Cone
Safety Vest
Machinery
Vehicle
