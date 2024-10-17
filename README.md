## Project: Live YOLOv8 Object Detection

This project demonstrates real-time object detection in the browser using YOLOv8 and ONNX. The program captures video from a webcam and processes it to detect various objects, displaying bounding boxes and class labels in real-time. It also uses speech synthesis to audibly announce the detected objects.

### Table of Contents
- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Setup and Usage](#setup-and-usage)
- [Code Explanation](#code-explanation)
- [Contributing](#contributing)
- [License](#license)

### Introduction
This project provides a simple, browser-based object detection system that leverages YOLOv8 for detecting objects in real-time. The core of the application uses ONNX runtime to run the model in the browser, process live video feed, and identify objects using the pre-trained YOLOv8 model. Detected objects are also read aloud using the browser's built-in speech synthesis.

### Technologies Used
- **YOLOv8**: A state-of-the-art object detection model.
- **ONNX Runtime**: A runtime for running machine learning models in browsers using ONNX.
- **JavaScript**: Client-side scripting to handle video input, canvas rendering, and model inference.
- **HTML5 Canvas**: Used to draw the video feed and detection boxes.
- **Web Speech API**: Used for real-time speech synthesis of detected objects.

### Features
- **Real-time Object Detection**: Detect objects from a webcam feed in real-time.
- **Visual Feedback**: Draw bounding boxes around detected objects.
- **Audio Feedback**: Speak detected objects aloud.
- **Browser-based**: Runs entirely in the browser without the need for server-side computation.
- **Uses YOLOv8**: Leverages the power of YOLOv8, a state-of-the-art object detection model.

### Setup and Usage
1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/divineDev-dotcom/yolov8-onnx.git
    ```
2. Open `index.html` in a browser that supports webcam access (e.g., Chrome, Firefox).
3. Allow webcam access when prompted.
4. The model will start detecting objects in real-time, displaying bounding boxes and labels, and speaking the detected objects aloud.

### Code Explanation
- **HTML Structure**: The HTML file includes a `canvas` for displaying the video feed and bounding boxes. The ONNX runtime is loaded via a CDN.
- **Main Functions**:
  - `init()`: Initializes the webcam feed and sets up the object detection loop.
  - `detectAndDraw()`: Handles capturing the video frame, running the YOLOv8 model, and drawing the detected objects.
  - `prepare_input()`: Prepares the video frame data to feed into the model.
  - `run_model()`: Runs the YOLOv8 model on the prepared input using ONNX.
  - `process_output()`: Processes the model output to extract bounding boxes and class labels.
  - `draw_boxes()`: Draws the bounding boxes and labels on the canvas and triggers the speech synthesis for detected objects.
  - `speakObjects()`: Uses the Web Speech API to speak the names of detected objects.

### Contributing
If you'd like to contribute, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

### License
This project is licensed under the MIT License.