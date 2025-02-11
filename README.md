# Head Pose Estimation Using MediaPipe & OpenCV

This project implements real-time head pose estimation using MediaPipe FaceMesh and OpenCV. The algorithm detects facial landmarks, calculates the 3D head orientation, and classifies the user's posture based on head tilt.

## Features
- Real-time face landmark detection using MediaPipe FaceMesh
- Estimation of head pose using Perspective-n-Point (PnP) solving
- Classification of head orientation:
  - Looking left
  - Looking right
  - Hunched (looking down)
  - Sitting back (looking up)
  - Correct posture
- Visual representation of nose direction using OpenCV
- Real-time FPS counter

## Requirements
Ensure you have the following dependencies installed:
```bash
pip install opencv-python mediapipe numpy
```

## Usage
1. Clone the repository:
```bash
git clone https://github.com/yourusername/head-pose-estimation.git
cd head-pose-estimation
```
2. Run the script:
```bash
python head_pose_estimation.py
```
3. The webcam will activate, and the real-time head pose estimation will be displayed.
4. Press `ESC` to exit the program.

## Explanation
- The script captures frames from the webcam and processes them using MediaPipe FaceMesh.
- Six key facial landmarks are used to estimate head orientation using the `cv2.solvePnP()` function.
- The 3D head position is calculated, and Euler angles are extracted to determine head pose.
- The classified head orientation is displayed on the screen along with an FPS counter.

## Example Output
The program provides a real-time display of the head pose estimation, including:
- A visual indicator (blue line) showing nose direction
- Text annotations indicating head orientation
- FPS counter

## License
This project is licensed under the MIT License.

## Author
Jack Parsons - [GitHub Profile](https://github.com/jackrafaelparsons)


