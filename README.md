# Vehicle-Detection-and-Traffic-Counting-Using-YOLOv8
This project implements a real-time vehicle detection and traffic counting system using the YOLOv8 object detection model. It processes either prerecorded videos or live camera feeds to detect vehicles, classify them, and monitor their movement across a predefined counting zone.
The system automatically tracks vehicle direction, records inbound and outbound traffic, and generates annotated video output displaying detected objects along with live traffic statistics.

## Project Workflow

The application follows the steps below:

### 1. Video Acquisition

* Load a video file or connect to a live video stream using OpenCV.
* Read and process frames sequentially for real-time analysis.

### 2. Frame Optimization

* Resize input frames to improve inference speed while maintaining detection accuracy.
* Adjust the scaling factor according to available hardware resources.

### 3. Object Detection

* Apply the YOLOv8 model to identify vehicles within each frame.
* Filter detections using a configurable confidence threshold to reduce false positives.

### 4. Detection Processing

* Extract the following information for every detected vehicle:

  * Bounding box coordinates
  * Confidence score
  * Object class label
* Draw bounding boxes and display the detected vehicle type with its confidence score.
* Calculate the center point of each detected object for movement analysis.

### 5. Vehicle Counting

* Define a virtual counting line across the roadway.
* Monitor vehicle center points as they cross the counting region.
* Determine travel direction based on the crossing sequence.
* Update traffic statistics for:

  * Incoming vehicles
  * Outgoing vehicles
* Maintain separate counts for each detected vehicle category.

### 6. Output Generation

* Display the processed video with detection overlays.
* Show real-time traffic statistics on each frame.
* Save the annotated video for later review and analysis.

## Technologies Used

* Python 3
* OpenCV
* Ultralytics YOLOv8
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Jupyter Notebook / IPython

## Features

* Real-time vehicle detection
* High-accuracy YOLOv8 inference
* Support for video files and live camera streams
* Automatic inbound and outbound vehicle counting
* Per-class traffic statistics
* Adjustable confidence threshold
* Configurable counting line
* Annotated output video generation
* Efficient frame processing for improved performance

## Requirements

Install the required Python packages before running the project:

* OpenCV
* Ultralytics
* NumPy
* Pandas
* Matplotlib
* Seaborn
* IPython

## Results

The system successfully detects multiple vehicle types, identifies their direction of movement, and maintains accurate traffic counts in real time. The final output includes an annotated video showing detected vehicles, confidence scores, bounding boxes, and continuously updated traffic statistics, making it suitable for traffic monitoring, transportation analytics, and intelligent surveillance applications.

