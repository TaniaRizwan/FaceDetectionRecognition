# Face Detection using Haar-Cascades and Local Binary Patterns

**ENCM 509 - Fundamentals of Biometric Systems Design**
Laboratory Project 6a 

## Overview
This project implements face detection using two primary approaches:
- Haar-Cascades
- LBP-based detection (Local Binary Patterns)

This code performs preprocessing steps (adaptive histogram equalization and normalization) and then uses these techniques to detect faces in images. Different parameter combinations are evaluated to tune detection performance by measuring precision, recll and F1 scores over varying IoU thresholds. 

## Installation and Setup 

_A guide on how to install the tools needed for running the project._

1. Clone the Repository
```bash
git clone https://github.com/TaniaRizwan/FaceDetectionRecognition.git
cd FaceDetectionRecognition
```

2. Create a Virtual Environment
It is recommended to use a virtual environment to manage dependencies:
```bash
# Using venv (Python 3)
python -m venv venv

# Activate the virtual environment:
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

3. Install Dependencies
Install required packages from the requirements.txt file.
```bash
pip install -r requirements.txt
```
## Usage

1. Preprocessing
- Loads images
- Applies adaptive histogram equalization (CLAHE) and normalization to enhance image quality
- Generated 'ground truth' bounding boxes for each image. Adjust these to support your images loaded.

2. Face Detection
- Runs the haar_cascade_detector or the evaluate_lbp_on_subject method on the preprocessed images.
- Detected faces are marked with bounding boxes.

3. Evaluation and Tuning
- Evaluate performance using the precision, recall and F1 scores across various IoU thresholds
- Parameter settings (scaleFactor, minNeighbors, minSize, maxSize) can be adjusted to optimize detection accuracy
- Generates precision-recall curves for the best parameter setting to visualize the trade-offs

## Documentation and Citations
- The project builds upon methodologies described in the following sources:
    - https://www.datacamp.com/tutorial/face-detection-python-opencv#face-detection
    - https://docs.opencv.org/4.x/d5/daf/tutorial_py_histogram_equalization.html
    - https://pyimagesearch.com/2021/02/01/opencv-histogram-equalization-and-adaptive-histogram-equalization-clahe/
    - https://www.v7labs.com/blog/f1-score-guide
    - https://stackoverflow.com/questions/70284265/python-get-the-maximum-of-a-certain-index-in-a-dictionary-of-arrays
    - https://stackoverflow.com/questions/37435369/how-to-draw-a-rectangle-on-image
    - https://pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection/
    - https://medium.com/@amit25173/opencv-haar-cascade-explained-3b39a390871c#:~:text=scaleFactor%20%3A%20This%20parameter%20controls%20how but%20might%20miss%20some%20objects


