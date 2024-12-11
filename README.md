# Drowsiness Detection System

This repository contains a **Drowsiness Detection System** implemented in Python using OpenCV, Dlib, and Pygame libraries. The system monitors the user's eyes through a webcam and raises an alert when drowsiness is detected, making it particularly useful for drivers or operators of heavy machinery.

## Features

- Real-time detection of facial landmarks and eye aspect ratio (EAR).
- Alerts the user with a sound notification when drowsiness is detected.
- Configurable thresholds for sensitivity.
- Visual feedback via contours around detected eyes.

## Requirements

- Python 3.6+
- Libraries:
  - OpenCV
  - Dlib
  - Imutils
  - Scipy
  - Pygame

To install the required libraries, run:

```bash
pip install opencv-python dlib imutils scipy pygame
```

## How It Works

1. **Eye Aspect Ratio (EAR)**: The system calculates the EAR to determine if the eyes are closed.
2. **Threshold-Based Alert**: If the EAR falls below a predefined threshold (`thresh`) for a certain number of frames (`frame_check`), it triggers an alert.
3. **Audio Alert**: An alert sound (`alert_sound.mp3`) is played when drowsiness is detected.
4. **Visual Feedback**: Eye contours are drawn on the video feed for visual feedback.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/PraveenKumar-A02/Drowsiness-detection.git
   cd Drowsiness-detection
   ```

2. Place the required files:
   - `shape_predictor_68_face_landmarks.dat`: Pre-trained facial landmark model.
   - `alert_sound.mp3`: Sound file for the alert.

3. Run the program:
   ```bash
   python drowsiness_detection.py
   ```

4. The webcam feed will open. Press `q` to exit.

## Configuration

- **Threshold (`thresh`)**: Set the EAR value below which an alert is triggered (default: `0.25`).
- **Frame Check (`frame_check`)**: Number of consecutive frames for which the EAR must be below the threshold before triggering an alert (default: `20`).
- Modify these parameters in the script to customize sensitivity.

## Example

### Alert Triggered:

- When the EAR value drops below `0.25` for 20 consecutive frames, the following happens:
  - Red alert text is displayed on the screen.
  - Alert sound is played.

## Limitations

- Requires good lighting for accurate detection.
- May not work well with glasses or obstructed faces.
- Limited to frontal face detection.

## Contributing

Feel free to fork this repository, improve the code, and submit a pull request. Suggestions and enhancements are always welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Stay safe and alert!

