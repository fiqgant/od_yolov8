# YOLOv8 Object Detection App

![YOLOv8 Logo](./assets/image.png)

This repository contains a comprehensive object detection app using YOLOv8, developed with Python, Streamlit, and OpenCV. The app allows for image, video, and live stream processing using various YOLOv8 models, including the ability to upload custom models. Additionally, it includes a standalone script for regular video processing using `main_reg.py`.

## Features

- **Image Processing:** Upload an image and process it using the selected YOLOv8 model, with bounding boxes, class names, confidence scores, and more.
- **Video Processing:** Upload and process a video file. The processed video can be downloaded, with annotations saved in a JSON file.
- **Live Stream Processing:** Real-time processing of webcam or live stream URLs using YOLOv8.
- **Custom Model Upload:** Upload and use custom YOLOv8 models for processing.
- **DeepSort Tracker Integration:** Optional object tracking using DeepSort, allowing object tracking across video frames.
- **FPS Display:** Real-time display of frames per second (FPS) during live stream and video processing.
- **JSON Output:** Detection results can be saved as JSON files for further analysis.
- **Standalone Video Processing (main_reg.py):** A standalone script for processing video files with YOLOv8, displaying bounding boxes, class names, confidence scores, and FPS on the video feed.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/fiqgant/od_yolov8.git
   cd od_yolov8
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the YOLOv8 models and place them in the `models/` directory. The `model_list.txt` file contains the available model names.

## Usage

### Running the Streamlit App

To start the Streamlit app, run the following command:

```bash
streamlit run main.py
```

### Using the Streamlit App

- **Image Processing:** Upload an image, select the YOLOv8 model, and click "Process Image" to see the results.
- **Video Processing:** Upload a video, select the YOLOv8 model, and click "Process Video." The processed video and results will be available for download.
- **Live Stream Processing:** Enter a live stream source, select the YOLOv8 model, and start the live stream processing.
- **Custom Model Upload:** Upload a YOLOv8 model file (`.pt`), and it will be added to the available models for processing.

### Using the Standalone Script (main_reg.py)

The `main_reg.py` script is a standalone Python script designed for direct video processing. It can be used with video files, webcams, or CCTV streams.

1. **Run the Script:**
   ```bash
   python main_reg.py
   ```

2. **Configuration:**
   - **Webcam:** Uncomment the webcam line in the script.
   - **Video File:** Uncomment the line to use a specific video file (e.g., "video.mp4").
   - **CCTV Stream:** Uncomment the line to use an RTSP link for CCTV streams.

The script will display the video with bounding boxes, class names, confidence scores, and FPS on the video feed.

## Model List

The app and standalone script support the following YOLOv8 models:

- `yolov8n`
- `yolov8s`
- `yolov8m`
- `yolov8l`
- `yolov8x`
- `yolov8n-seg`
- `yolov8s-seg`
- `yolov8m-seg`
- `yolov8l-seg`
- `yolov8x-seg`
- `yolov8n-pose`
- `yolov8s-pose`
- `yolov8m-pose`
- `yolov8l-pose`

## Contributing

Contributions are welcome! Please create a pull request or open an issue for any bugs or feature requests.

## License

This project is licensed under the MIT [License](LICENSE).

## Acknowledgements

Special thanks to the YOLOv8 team and the developers of the libraries used in this project.