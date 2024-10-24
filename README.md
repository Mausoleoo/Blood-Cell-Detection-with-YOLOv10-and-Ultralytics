# Blood Cell Detection with YOLOv10 and Ultralytics
This repository contains a YOLOv10-based object detection model trained with the Blood Cell Detection dataset using the Ultralytics framework. The dataset consists of 364 images and 4888 labeled instances across three main classes:

* WBC (White Blood Cells)
* RBC (Red Blood Cells)
* Platelets
  
The model is designed to detect and classify blood cells in microscopic images, an important task in medical diagnostics.

-----------------------------------------------------------------------------

# Dataset

The **Blood Cell Detection** dataset is commonly used to evaluate object detection models in the field of medical imaging. It is a small-scale dataset, making it suitable for fast experimentation and benchmarking.

**Data split**
* Training: 70%
* Testing: 20%
* Validation: 10%

The dataset is preprocessed for YOLOv10 and organized into the following folder structure:

images/: Contains the images of blood cells.

labels/: Contains the corresponding labels (in YOLO format) for each image.

link: https://www.kaggle.com/datasets/adhoppin/blood-cell-detection-datatset

-----------------------------------------------------------------------------

# Importance of Blood Cell Recognition

Accurately detecting and classifying blood cells is critical for diagnosing and monitoring various health conditions. Blood cells are categorized into three main types:

* **WBC (White Blood Cells)**: These cells are part of the immune system and help fight infections. Abnormalities in their number can indicate infections, autoimmune diseases, or blood cancers.

* **RBC (Red Blood Cells)**: These cells are responsible for carrying oxygen throughout the body. A low count can lead to anemia, while a high count may indicate other medical conditions.

* **Platelets**: These cells are involved in blood clotting. Abnormal platelet counts can lead to excessive bleeding or clotting disorders.

By automating the detection of these cells, we can speed up diagnostic processes and improve the accuracy of medical diagnoses.

-----------------------------------------------------------------------------

# Training the YOLOv10 Model

The YOLOv10 model was trained using the Ultralytics framework, which provides a simple interface for training, validating, and deploying YOLO models. The model was trained for 20 epochs with the following parameters:

* Image size: 416x416
* Batch size: 16
* Device: CUDA (GPU A100)

-----------------------------------------------------------------------------

# Predictions

![val_batch0_labels_20_726668898c6df4cef0c0](https://github.com/user-attachments/assets/cbe01dbd-d69e-4d5c-a399-1c97301413f3)

-----------------------------------------------------------------------------

# Metrics (Test set)

* Precision(B): 0.831
* Recall(B): 0.804
* mAP50(B): 0.877
* mAP50-95(B): 0.615
* fitness: 0.641

**Metrics (training)**

![image](https://github.com/user-attachments/assets/d2b258fa-9b9d-44a3-a0b8-c08830f75b67)

-----------------------------------------------------------------------------

# Future Work

Possible improvements and extensions for this project include:

* Fine-tuning the model with a larger blood cell dataset for improved performance.
* Adding more classes for different types of blood cells or anomalies.
* Deploying the model in a real-time medical application for automated diagnostics.

-----------------------------------------------------------------------------

# Acknowledgments

This project uses the Blood Cell Detection dataset, which is publicly available for use in object detection tasks. The dataset and model are provided under the public domain, and all code in this repository can be freely modified and shared.

The Ultralytics framework makes the entire process of training and deploying YOLO models easy and straightforward. Whether you're a beginner or an experienced developer.
