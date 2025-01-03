# Hand Gesture Controlled Screen Brightness

This project utilizes a combination of **OpenCV**, **MediaPipe**, and **screen_brightness_control** to control your computer's screen brightness using hand gestures. The program captures video from your webcam, detects hand landmarks, and calculates the distance between the tips of the thumb and index finger. Based on this distance, it adjusts the screen brightness dynamically.

## Requirements

To run this project, you'll need to install the following Python libraries:

- **OpenCV**: for capturing video frames from the webcam and manipulating images.
- **MediaPipe**: for hand landmark detection.
- **screen_brightness_control**: to control the screen's brightness.
- **numpy**: for numerical operations like linear interpolation.

You can install the necessary dependencies with:

```bash
pip install opencv-python mediapipe screen-brightness-control numpy
```

## Features

- **Hand Landmark Detection**: Detects the position of key hand landmarks using MediaPipe's hand tracking model.
- **Brightness Control**: The distance between the thumb and index finger is mapped to a screen brightness level. This is done using linear interpolation.
- **Real-time Video Feed**: A webcam feed is displayed in real-time with key hand landmarks drawn on the video frame.

## How It Works

1. **Capturing Video**: The program starts by capturing video from the webcam using OpenCV.
2. **Hand Detection**: MediaPipe’s hand tracking model is used to detect the hand landmarks. Specifically, it identifies the tip of the thumb (landmark 4) and the tip of the index finger (landmark 8).
3. **Brightness Adjustment**: The Euclidean distance between the thumb and index finger tips is calculated. This distance is then mapped to a brightness range from 0 to 100 using linear interpolation. The screen brightness is adjusted using `screen_brightness_control`.
4. **Video Display**: The program displays the webcam feed with green circles on the thumb and index finger tips, and a green line connecting them. The video is updated in real-time.

## Running the Project

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/hand-gesture-brightness-control.git
    cd hand-gesture-brightness-control
    ```

2. Install the required dependencies:
    ```bash
    pip install opencv-python mediapipe screen-brightness-control numpy
    ```

3. Run the Python script:
    ```bash
    python hand_gesture_brightness.py
    ```

4. The webcam feed will appear, and the brightness will adjust based on the thumb and index finger distance. Press 'q' to exit.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
