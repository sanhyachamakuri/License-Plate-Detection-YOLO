# AI Usage Log

## Project Information

**Project Title:** License Plate Detection Using YOLO  
**Project Type:** Tier 1 – Core Computer Vision Group Project  
**Team Members:** Sandhya Chamakuri, Keichara Opara, and Dulce Zuniga

This document records how AI tools were used as learning and development support during the License Plate Detection Using YOLO project. AI assistance was used for understanding project requirements, receiving step-by-step guidance, troubleshooting, interpreting results, and organizing project documentation.

## AI Tool Used

**Tool:** ChatGPT (OpenAI)

## AI Usage Details

### 1. Understanding the Project Requirements

**Questions / Assistance Requested:**
- Asked for clarification of the ITAI 1378 Midterm Project requirements.
- Asked for help understanding the differences between the project tiers.
- Discussed whether License Plate Detection using YOLO was appropriate for a Tier 1 project.
- Asked for guidance on organizing the project into manageable steps.

**What I Learned:**
I learned that a Tier 1 project can focus on one computer vision task using one model. License plate detection is an object detection problem, and YOLO can be used to identify and locate license plates in vehicle images.

**How I Applied It:**
Our group selected License Plate Detection using YOLO as the project topic and organized the project around a single object detection model.

---

### 2. Dataset Setup and Verification

**Questions / Assistance Requested:**
- Requested step-by-step guidance for uploading and extracting the license plate dataset in Google Colab.
- Asked how to examine the dataset folder structure.
- Asked how to verify the training and validation image and label folders.
- Asked how to count the number of training and validation images.
- Requested help understanding the YOLO annotation format.
- Asked how to visually verify that bounding boxes correctly identify license plates.

**What I Learned:**
I learned how a YOLO dataset is organized using separate image and label files. I also learned that each image should have a corresponding label file containing the bounding-box annotation information.

**How I Applied It:**
I inspected the dataset and verified that it contained 1,526 training images and 169 validation images, for a total of 1,695 images. I also viewed sample images and their bounding boxes to confirm that the annotations were correctly placed around license plates.

---

### 3. Dataset Configuration

**Questions / Assistance Requested:**
- Asked for help understanding the provided dataset YAML configuration file.
- Requested guidance for changing the original dataset paths so that they would work in Google Colab.
- Asked for explanations of the class configuration and dataset paths.

**What I Learned:**
I learned that the YOLO configuration file tells the model where the training and validation data are located and defines the number and names of object classes.

**How I Applied It:**
I created a Colab-compatible `data.yaml` file containing the correct paths for the training and validation folders. The project uses one class named `license_plate`.

---

### 4. Google Colab and GPU Setup

**Questions / Assistance Requested:**
- Requested guidance for configuring Google Colab for the project.
- Asked how to enable and verify GPU acceleration.
- Requested help reconnecting Google Drive and restoring the dataset after a Colab runtime restart.

**What I Learned:**
I learned that using a GPU can significantly improve the speed of model training. I also learned that files stored temporarily in the Colab runtime can be lost after a runtime restart.

**How I Applied It:**
I enabled the T4 GPU in Google Colab, verified that the GPU was available, remounted Google Drive when necessary, and restored the project dataset and configuration.

---

### 5. YOLO Installation and Pretrained Model Testing

**Questions / Assistance Requested:**
- Asked how to install the Ultralytics YOLO library.
- Requested guidance for loading a pretrained YOLO model.
- Asked for help understanding the purpose of testing a pretrained model before custom training.
- Requested guidance for testing the pretrained model on a project image.

**What I Learned:**
I learned that testing a pretrained model first helps confirm that the YOLO environment, dependencies, and inference process are working correctly before beginning custom model training.

**How I Applied It:**
I installed the Ultralytics package, loaded a pretrained YOLOv8 model, ran an initial test, and then tested the model on an image from the license plate dataset.

---

### 6. Training the License Plate Detection Model

**Questions / Assistance Requested:**
- Requested guidance for configuring the YOLO training process.
- Asked for explanations of training settings such as epochs, image size, batch size, and GPU device selection.
- Requested help monitoring and understanding the training output.

**What I Learned:**
I learned how YOLO uses labeled training images to learn the location of license plates and how training parameters control the model training process.

**How I Applied It:**
I trained a YOLOv8n model for 20 epochs using the license plate dataset with an image size of 640, batch size of 16, and GPU acceleration.

---

### 7. Model Testing and Evaluation

**Questions / Assistance Requested:**
- Asked how to test the trained model on validation images.
- Requested explanations of Precision, Recall, mAP50, and mAP50-95.
- Asked for guidance for evaluating the model on multiple images.
- Requested help reviewing successful detections and possible failure cases.

**What I Learned:**
I learned that model performance should be evaluated using both visual inspection and quantitative metrics. Precision measures how many predicted detections are correct, Recall measures how many actual objects are detected, and mAP provides an overall measurement of object detection performance.

**How I Applied It:**
I tested the trained model on multiple validation images and reviewed the predicted license plate bounding boxes and confidence scores. I also ran model validation and reviewed Precision, Recall, mAP50, and mAP50-95 results.

The final validation results were approximately:

- Precision: 0.994
- Recall: 0.991
- mAP50: 0.994
- mAP50-95: 0.882

---

### 8. Saving the Model and Results

**Questions / Assistance Requested:**
- Requested guidance for saving the trained YOLO model.
- Asked how to preserve the training and evaluation results in Google Drive.
- Asked how to avoid losing completed work when the Colab runtime changes or disconnects.

**What I Learned:**
I learned that important model files and training results should be stored in persistent storage rather than relying only on Colab's temporary runtime storage.

**How I Applied It:**
I saved the trained model and training results to Google Drive and downloaded a copy of the completed Colab notebook as an additional backup.

---

### 9. GitHub Repository and Documentation

**Questions / Assistance Requested:**
- Requested guidance for creating and organizing the GitHub repository.
- Asked how to upload the project notebook.
- Requested guidance for creating the `data/README.md` file.
- Requested help documenting AI usage according to the project requirements.

**What I Learned:**
I learned how GitHub can be used to organize project files and documentation and how commit messages provide a record of project changes.

**How I Applied It:**
I created a public GitHub repository for the group project, uploaded the project notebook, created dataset documentation, and created this AI usage log.

---

## Overall Reflection

AI was used as a learning and support tool throughout the project. It helped me understand unfamiliar concepts, break the project into smaller steps, troubleshoot issues, and interpret the outputs produced by Google Colab and YOLO.

I reviewed the guidance, ran the project steps in Google Colab, checked the outputs, verified the dataset and annotations, trained and evaluated the model, and organized the project files. This process helped me better understand the workflow of a computer vision object detection project, from dataset preparation through model training, evaluation, and documentation.
