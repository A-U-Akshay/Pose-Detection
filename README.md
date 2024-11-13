# ✨ Body Pose Detection with MoveNet ✨

## 📝 Overview
This project is a simple web application using the **ml5.js** library to perform body pose detection through the **MoveNet** model. It captures video input from the user's webcam, detects body poses in real-time, and visualizes the detected keypoints and skeleton connections on a canvas.

## 🌟 Features
- 🎥 Real-time webcam video feed.
- 🏃‍♂️ Detection and visualization of body keypoints.
- 📐 Display of skeleton connections between detected keypoints.

## 🛠️ Technologies Used
- **HTML5 Canvas** (via p5.js) for drawing and rendering.
- **ml5.js** for machine learning and body pose detection.
- **p5.js** for video capture and canvas handling.

## 🚀 Getting Started

### ✅ Prerequisites
Ensure you have the following installed on your system:
- A modern web browser (e.g., Chrome, Firefox)
- A webcam for video input

### 📦 Installation
1. Clone this repository or download the source files.
   ```bash
   git clone https://github.com/yourusername/pose-detection.git
   cd pose-detection
   ```
2. Ensure you have a local server set up to run the application (e.g., using **Live Server** extension in VS Code).

### ▶️ Running the Application
1. Open `index.html` in your web browser.
2. Grant webcam access when prompted.
3. The app will display a real-time video feed with detected keypoints and skeleton connections overlayed.

## 📂 Code Explanation

### 🔑 Key Files
- **sketch.js**: Contains the primary logic for the application.
- **index.html**: Hosts the canvas and links the JavaScript.
- **libraries**: Ensure `p5.js` and `ml5.js` are linked or loaded.

### 📝 Main Functions
- **preload()**: Loads the MoveNet model.
- **setup()**: Sets up the canvas, video capture, and initializes pose detection.
- **draw()**: Continuously draws the video feed, keypoints, and skeleton connections on the canvas.
- **gotPoses()**: Callback to update detected pose data.

### 🔧 Important Variables
- `poses`: Array to store the detected body poses.
- `connections`: Stores information about the skeleton structure for visualization.

## 🛡️ How It Works
1. The `bodyPose` model is loaded using `ml5.bodyPose('MoveNet')`.
2. The video feed is captured and hidden (used only as a source for detection).
3. The `bodyPose.detectStart()` method is called to start pose detection, passing the `gotPoses` function as the callback.
4. The `draw()` function displays the video and overlays detected keypoints and connections if their confidence is above a set threshold.

## 🎨 Customization
- Adjust `confidence` threshold in `draw()` to fine-tune which keypoints and connections are drawn.
- Modify `stroke()` and `fill()` properties to change visualization styles.

## 📸 Example Output
The application displays a webcam feed with green circles representing keypoints and red lines for skeleton connections.

## 🔮 Future Improvements
- Add more styling options and interactive elements.
- Support saving snapshots of the pose overlay.
- Expand compatibility for mobile devices.

## 🛠️ Troubleshooting
- Ensure the webcam is allowed by your browser.
- Confirm `ml5.js` and `p5.js` are correctly linked in `index.html`.

## 📜 License
This project is licensed under the MIT License. Feel free to use, modify, and distribute as needed.

## 🤝 Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss potential changes.

## 🙏 Acknowledgements
- [p5.js](https://p5js.org/)
- [ml5.js](https://ml5js.org/)
- [Google's MoveNet](https://github.com/tensorflow/tfjs-models/tree/master/pose-detection)
