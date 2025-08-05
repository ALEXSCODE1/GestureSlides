# GestureSlides 

## 👥 Contributors

- Alex Xu  
- Michael Yang  
- Andy Li

**GestureSlides** is a Python-based computer vision project that lets you control slide presentations using hand gestures. It uses the [YOLOv8 pose estimation model](https://docs.ultralytics.com/models/pose/) to detect body keypoints from your webcam feed, allowing intuitive slide navigation by raising your hands.

## 🎯 Features

- 🤖 Real-time pose detection using YOLOv11 (`yolo11n-pose.pt`)
- ✋ Gesture-based slide control:
  - Raise **left hand** → ⏩ Next slide
  - Raise **right hand** → ⏪ Previous slide
- ⏸ Cooldown mechanism to prevent multiple triggers
- 🎥 Live annotated webcam feed with keypoints and skeleton
- 🧠 Intelligent shoulder distance check to reduce false positives

## 🧪 How It Works

1. Captures video frames from your webcam.
2. Runs YOLO pose estimation to identify 17 keypoints per person (COCO format).
3. Checks if the wrist is raised above the shoulders by a buffer margin.
4. Uses `pyautogui` to simulate key presses (`←` and `→`) to control slides.
5. Displays real-time feedback on the screen using OpenCV.

## 📦 Requirements

- Python 3.8+
- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
- OpenCV
- NumPy
- Pandas
- PyAutoGUI

Install dependencies with

```bash
pip install ultralytics opencv-python numpy pandas pyautogui
