# Video Processing and Object Tracking Project

This project provides a set of tools for video processing, object detection, and tracking using computer vision techniques. It utilizes the YOLOv8 model via Roboflow for object detection and implements custom tracking and counting logic.

## Table of Contents

1. [Features](#features)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Components](#components)
6. [Configuration](#configuration)
7. [Output](#output)
8. [Notes](#notes)

## Features

- Combine resized frames into a video
- Object detection using YOLOv8 model via Roboflow API
- Object tracking across video frames
- Counting objects as they cross a specified line
- GUI for initializing item counts
- Real-time display of object counts on video frames
- Final count display in a user-friendly GUI
- Option to resize input video to 640x640 for standardized processing

## Prerequisites

- Python 3.7+
- OpenCV (cv2)
- NumPy
- Roboflow
- tkinter

## Installation

1. Clone this repository to your local machine.
2. Install the required packages:

   ```
   pip install opencv-python numpy roboflow
   ```

3. Make sure you have a Roboflow account and API key.

## Usage

1. Open the Jupyter notebook `VideoProcess.ipynb`.
2. Run the cells in order, depending on your specific needs.

## Components

The project consists of several components:

1. **Frame Combination**: Combines resized frames into a video.
2. **YOLOv8 Model Initialization**: Sets up the object detection model using Roboflow.
3. **Object Detection and Tracking**: 
   - Version without GUI
   - Version with GUI for initial item count
4. **Video Resizing**: Option to resize input video to 640x640

## Configuration

- Modify the `KNOWN_ITEMS` list to include the objects you want to track.
- Adjust the `mid_line` calculation to change where objects are counted.
- Set the `TARGET_SIZE` variable to change the video resolution (default is 640x640).

## Output

- Processed video file with bounding boxes and object labels.
- Real-time display of object counts on the video frames.
- Final counts shown in a GUI window at the end of processing.

## Notes

- The script assumes objects moving from bottom to top of the frame are entering, and those moving from top to bottom are exiting. Adjust the counting logic if your use case differs.
- Resizing the video to 640x640 may cause distortion if the original aspect ratio is different. Consider adding padding instead of stretching if this is an issue.
- The Roboflow API key is included in the notebook. For security, consider moving this to an environment variable or configuration file.

## License

[Specify your license here]

---

For any questions or issues, please [open an issue](link-to-your-issue-tracker) on the project repository.
