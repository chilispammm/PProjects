# Eliteserien Football Detection

This notebook demonstrates the process of training an object detection model on a dataset curated from Norwegian Eliteserien football league matches and evaluating its performance.

## Project Overview

* **Goal:** To train a YOLOv8 object detection model to identify specific objects (players, goalkeepers, referees, ball, etc.) in football match footage.
* **Dataset:** Curated from Norwegian Eliteserien football league matches (2021-2023 seasons).
* **Model:** YOLOv8 (specifically, the yolov8x.pt variant).
* **Key Steps:** Data loading and preparation, Exploratory Data Analysis (EDA), Dataset organization for YOLO training, Model training, Model evaluation, and Running inference on sample images and video.

## Notebook Structure

The notebook is organized into the following sections:

1. **Required Libraries + Setting up Environment:** Installs necessary libraries like `ultralytics`, `opencv-python-headless`, `torch`, `torchvision`, `torchaudio`, `tensorflow`, `matplotlib`, `numpy`, and `yt-dlp`.
2. **Loading and preparing the data:** Downloads and unzips the Eliteserien dataset from Zenodo.
3. **EDA of frames:** Performs basic Exploratory Data Analysis on the image frames from the dataset.
4. **YOLOv8 Model:**
   * Organizes the dataset into the required YOLO format (train/val splits for images and labels).
   * Creates the `data.yaml` file for YOLOv8 training.
   * Trains the YOLOv8 model on the prepared dataset.
   * Evaluates the trained model using metrics like precision, recall, and mAP (via TensorBoard).
   * Runs inference on sample images to visualize predictions.
5. **Running inference on video:**
   * Sources and prepares a sample video clip using `yt-dlp`.
   * Runs real-time object detection on the video clip using the trained model.

## How to Use

1. Open the notebook in Google Colab.
2. Run each cell sequentially.
3. Ensure you have a GPU runtime enabled for faster training.

## Results

* The notebook outputs include:
  * Summary statistics of the dataset (number of images, resolutions, file sizes).
  * Plots of sample images and file size distribution.
  * TensorBoard logs showing training progress and evaluation metrics.
  * Sample images with bounding box predictions.
  * A processed video clip with real-time object detection.

## Future Work

* Explore different YOLOv8 model sizes or other object detection architectures.
* Fine-tune hyperparameters for better performance.
* Implement more advanced evaluation metrics.
* Deploy the model for real-time inference on a platform.

## Acknowledgements

* This project utilizes the Eliteserien dataset available on Zenodo.
* Thanks to the Ultralytics team for the YOLOv8 library.
