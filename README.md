# YOLOv7 Training and Detection Pipeline

This project involves training and utilizing the YOLOv7 model for object detection on a custom dataset. Below is a summary of the steps taken to achieve this, including data preparation, model training, and detection on new videos.

## Data Preparation

1. **Labeling Images**:
    - The images were divided into two sets.
    - Using the labelImg software, the images were annotated with six classes: `Portugal`, `Spain`, `Ball`, `Referee`, `Goalkeeper.s`, and `Goalkeeper.p`.

2. **Data Split**:
    - After correcting any labeling errors, the dataset was divided into `train` and `validation` sets with an 80:20 ratio.

## Setting Up the Environment

1. **Google Drive Access**:
    - The first cell in the code provides access to Google Drive to save and load necessary files.

2. **Directory Setup**:
    - Change the directory to `MyDrive`.
    - Create a new directory if it doesn't exist and navigate to it.

3. **Cloning YOLOv7 Repository**:
    - Clone the YOLOv7 repository from GitHub into the newly created directory.
    - Navigate into the `YOLOv7` folder.

4. **Downloading Pre-trained Weights**:
    - Download the pre-trained weights for YOLOv7x.

## Customizing YOLOv7 for Custom Dataset

1. **Data Configuration**:
    - Load training data and create a copy of the `coco.yaml` file.
    - Edit the file to include the number of classes and their names.

2. **Model Configuration**:
    - Edit the `yolov7x.yaml` file located in the `cfg/training` directory to reflect the custom dataset.
    - Set `Epoch` to 32, `BatchSize` to 16, and `ImageSize` to 416x416.

## Training the Model

1. **Initial Training**:
    - Train the model with the above configuration using the specified data and configurations using the script.

2. **Saving Trained Weights**:
    - The best weights from training were saved from the `runs/training/weights` directory and copied to the main `yolov7` folder.

## Detection on New Data

1. **Video Processing**:
    - A 4-minute video clip not included in the training set was processed.
    - This video was uploaded to the main directory.

2. **Running Detection**:
    - Using the `detect.py` script with the best-trained weights and a confidence level of 0.25, the algorithm detected objects in the video.
    - The detected results were saved in the `yolov7/runs/detect` directory.

## Additional Information

- The best training weights and the detection code exists.
- Example images and their corresponding labels have been placed in their appropriate directories within the dataset structure but they are not not enough and you should upload your own labeled images like example.
- You can download mp4 file separately by clicking on them and then tapping on download.
- if you set epoch 100 and confidence level 0.5 you will reach even higher precision and recall but also you will need more resources and tim.


