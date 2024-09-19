
# Look Control

## Overview

**Look Control** is a computer vision-based project that allows you to control your mouse using your eye movements. It captures live video from a webcam, detects facial landmarks, and maps eye movements to screen coordinates to move the mouse. You can also perform actions like clicking by simply blinking your eyes. This implementation leverages OpenCV, Mediapipe, and PyAutoGUI libraries for real-time processing and interaction.

## Features

- Real-time video capture and processing using OpenCV.
- Eye tracking using the Mediapipe FaceMesh model to control mouse movements.
- Eye blink detection to simulate mouse clicks.
- Simple and easy to use with minimal setup.

## Technologies Used

- **Python:** The programming language used for building the application.
- **OpenCV:** Used for capturing video and processing each frame.
- **Mediapipe:** For detecting facial landmarks and tracking eye movements.
- **PyAutoGUI:** Used to control the mouse based on eye position and blinks.

## Prerequisites

- Python 3.x
- A webcam for real-time video capture.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/look-control.git
   cd look-control
   ```

2. **Create a Virtual Environment (Optional)**

   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Dependencies**

   Install the required Python packages using pip:

   ```bash
   pip install opencv-python mediapipe pyautogui
   ```

## Usage

1. **Run the Eye-Control Script**

   Execute the main Python script:

   ```bash
   python main.py
   ```

2. **Operating the Application**

   - A window will open, displaying the live video feed from your webcam.
   - Move your eyes to control the mouse cursor on the screen.
   - Blink to simulate a mouse click.
   - Press the 'q' key to stop the video stream and close the application.

## Code Breakdown

### Step 1: Import Libraries

- Import necessary libraries such as `cv2` for OpenCV, `mediapipe` for facial landmark detection, and `pyautogui` for mouse control.

### Step 2: Initialize Webcam and Face Mesh Model

- Set up the webcam to capture live video and initialize the Mediapipe FaceMesh model for detecting facial landmarks.

### Step 3: Control Mouse Using Eye Landmarks

- Get the screen size to map eye movements to screen coordinates.
- Capture frames from the webcam, process them using the FaceMesh model, and identify specific eye landmarks.
- Calculate the screen coordinates based on the detected eye position and use `pyautogui` to move the mouse.
- Detect eye blinks by tracking the distance between specific facial landmarks to simulate mouse clicks.

### Step 4: Display the Video Feed

- Draw circles on the detected eye landmarks and highlight blinking action on the video feed.
- Use OpenCV's `imshow()` method to display the live video with visual markers.

### Step 5: Exit the Application

- Use the 'q' key to stop the video stream and release the webcam.

## Troubleshooting

- Ensure adequate lighting for accurate eye tracking.
- Adjust the camera position for better landmark detection if the mouse control is inaccurate.

## Future Enhancements

- Add additional gestures to simulate right-click or scrolling actions.
- Introduce calibration to adapt to different screen sizes and user distances.
