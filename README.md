# Volume Control using Hand Tracking
This project allows you to control system volume using hand gestures detected through a webcam.
It uses OpenCV for video capture and visualization, MediaPipe for hand landmark detection, and PyCaw to interact with the system audio volume.
This is based on handTracking module which detects the 21 landmarks on the cropped image of your hand, the handTracking module is prebuilt individually and itd directly imported
The module is present in the repo and i have a seperate repositary for it and its basics

# How It Works
The webcam captures your hand in real-time.

MediaPipe Hands detects landmarks on your hand.

The distance between the thumb tip and index finger tip is calculated.

This distance is mapped to the system volume range using NumPy interpolation.

The volume bar on the screen shows the current volume level, and the system volume adjusts accordingly.

# Requirements
Make sure you have the following Python packages installed:

# pip install opencv-python mediapipe numpy pycaw comtypes

opencv-python → for webcam access and drawing visuals

mediapipe → for hand tracking landmarks

numpy → for distance and volume interpolation

pycaw → for controlling Windows system volume

time (comes with Python) → for FPS calculation

# Project Structure

volumeHandControl.py       # Main script to control volume
handTrackingModule.py      # Custom hand tracking wrapper using MediaPipe
# How to Run
Clone or download this project.

Ensure your webcam is connected.

# Show your hand to the camera:

Move the thumb and index finger apart to increase volume

Bring them closer to decrease volume

# Features
Real-time hand tracking with MediaPipe

Smooth volume interpolation based on finger distance

On-screen volume bar and FPS counter

Works on Windows via PyCaw
