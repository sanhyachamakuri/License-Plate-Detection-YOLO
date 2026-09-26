# License Plate Detection Using YOLO

## ITAI 1378 – Tier 1 Computer Vision Group Project

**Project:** License Plate Detection Using YOLO  
**Tier:** Tier 1 – Core Project  
**Task:** Object Detection

---

## Team Members

- Sandhya Chamakuri
- Keichara Opara
- Dulce Zuniga

---

## Project Overview

This project focuses on detecting vehicle license plates in images using YOLO (You Only Look Once), an object detection model.

The system takes a vehicle image as input, processes the image using a trained YOLO model, and identifies the location of the license plate by drawing a bounding box around it.

The project is being developed and tested in Google Colab using Python and the Ultralytics YOLO framework.

---

## Tier Selection and Justification

This project is classified as a **Tier 1 – Core Project** because it focuses on one computer vision task using one object detection model.

The main task is license plate detection, and YOLO is used to locate license plates in vehicle images. The project focuses on detection only and does not currently include additional tasks such as OCR or license plate text recognition.

---

## Problem

License plates are important identifiers for vehicles, but manually locating license plates in large numbers of vehicle images can be time-consuming.

An automated license plate detection system can help identify the location of license plates in vehicle images. This type of computer vision technology can be useful as a foundation for applications involving parking management, traffic monitoring, and vehicle identification systems.

---

## Proposed Solution

Our solution uses a YOLO object detection model to automatically locate license plates in vehicle images.

### Workflow

**Vehicle Image → YOLO Model → License Plate Detection → Bounding Box Output**

The input is an image containing a vehicle. The YOLO model analyzes the image and predicts the location of the license plate. The output displays a bounding box around the detected license plate along with a confidence score.

---

## Technical Approach

The project uses YOLOv8n through the Ultralytics framework for object detection.

### Technologies

- Python
- Google Colab
- Ultralytics YOLO
- YOLOv8n
- OpenCV
- GitHub

A pretrained YOLOv8n model is used as the starting point and is trained on a license plate dataset containing labeled vehicle images.

Google Colab is used for development and GPU-based model training.

---

## Dataset Plan

The dataset contains vehicle images with labeled license plates in YOLO bounding-box format.

### Dataset Summary

- Total images: 1,695
- Training images: 1,526
- Validation images: 169
- Number of classes: 1
- Class name: `license_plate`
- Annotation format: YOLO bounding-box format

The dataset was inspected before training by viewing sample images and their annotations. The image and label counts were also checked to verify the dataset structure.

The complete dataset is not stored in this GitHub repository because of its size. Additional dataset information is available in `data/README.md`.

---

## First Working Demo

Before custom model training, a pretrained YOLOv8n model was tested in Google Colab to confirm that the environment, model loading, and inference process were working correctly.

The pretrained model was also tested on an image from the project dataset before beginning custom training.

---

## Model Training

The YOLOv8n model was trained using the license plate dataset in Google Colab.

### Training Configuration

- Epochs: 20
- Image size: 640
- Batch size: 16
- GPU: NVIDIA T4
- Object class: `license_plate`

The trained model was then tested on validation images to examine license plate detections, bounding boxes, and confidence scores.

---

## Success Metrics

The project will evaluate the license plate detection model using:

- Precision
- Recall
- mAP50
- mAP50-95
- Visual inspection of bounding-box detections
- Review of successful and unsuccessful detection examples

The goal is to produce reliable license plate detections on validation images while maintaining strong object detection metrics.

---

## Preliminary Model Results

Initial model validation produced approximately:

- Precision: 0.994
- Recall: 0.991
- mAP50: 0.994
- mAP50-95: 0.882

These preliminary results demonstrate that the trained model can successfully detect license plates in the validation dataset. Additional testing and review of success and failure cases will be used to better understand model performance.

---

## Milestone Plan

### 1. Blueprint

Define the problem, project scope, technical approach, dataset, success metrics, and project risks.

### 2. First Working Demo

Run a pretrained YOLO model successfully and verify that the object detection environment works.

### 3. Make It Ours

Prepare the license plate dataset and train YOLO on the project-specific `license_plate` class.

### 4. Improve and Measure

Evaluate the trained model using validation images, performance metrics, confidence scores, and success/failure cases.

### 5. Package and Present

Organize the GitHub repository, complete project documentation, prepare the presentation, and demonstrate the project results.

---

## Risks and Plan B

### Risk 1: Dataset or Annotation Problems

Some images may contain unclear, small, or difficult-to-see license plates, and incorrect annotations could affect model performance.

**Plan B:** Inspect sample images and annotations, verify image-label pairs, and remove or correct problematic data if necessary.

### Risk 2: Limited Computing Resources

Model training may be affected by Google Colab runtime limits, GPU availability, or session disconnections.

**Plan B:** Use the lightweight YOLOv8n model, keep the dataset and training scope manageable, save important model files to Google Drive, and maintain notebook backups.

---

## Project Files

The repository contains:

- `Group_Project_License_Plate_Detection_YOLO.ipynb` – Google Colab project notebook
- `data/README.md` – Dataset documentation
- `docs/AI_usage_log.md` – AI usage documentation
- `docs/proposal.pdf` – Midterm Blueprint presentation (to be added)

---

## Team Contributions

### Sandhya Chamakuri

- Worked with the dataset in Google Colab.
- Verified dataset structure, images, labels, and annotations.
- Configured the dataset for YOLO.
- Ran the YOLO model and training process.
- Tested and evaluated the trained model.
- Reviewed model outputs and performance metrics.
- Saved the trained model and training results.
- Helped organize the GitHub repository and documentation.

### Keichara Opara

- Identified the dataset for the project.
- Participated in project planning and organization.
- Helped review the dataset and project requirements.
- Assisted with organizing the GitHub repository.
- Helped review the YOLO model results and project progress.
- Contributed to project documentation and preparation for submission.

### Dulce Zuniga

- Participated in the group project.
- Helped review project information and documentation.
- Assisted with organizing project materials for submission.

---

## AI Usage

AI was used as a learning and support tool for understanding project requirements, receiving step-by-step guidance, troubleshooting technical issues, interpreting model results, and organizing documentation.

AI-assisted guidance was reviewed and applied during the project workflow. The project dataset, Colab execution, model training, testing, evaluation, and project outputs were reviewed by the team.

Detailed AI usage documentation is available in:

`docs/AI_usage_log.md`

---

## Project Status

The project currently has a working YOLO license plate detection prototype. The dataset has been prepared, the model has been trained and evaluated, and preliminary results have been reviewed.

The remaining work focuses on completing the Midterm Blueprint presentation, organizing final documentation, and preparing the project for submission.
