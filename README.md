# Face Recognition Project

## Introduction
This project is a **Face Recognition System** that uses **OpenCV** and **LBPH (Local Binary Patterns Histograms)** algorithm to recognize human faces in real-time. It can be used for applications like security systems, attendance tracking, and user authentication. 

The project captures images, trains a face recognition model, and detects faces in live video streams or image files.

## Features
- Real-time face detection and recognition.
- Utilizes the LBPH algorithm for efficient and accurate facial recognition.
- Supports multiple users with labeled data.
- Easy integration with webcams or external video feeds.
  
## Prerequisites
Before running the project, you need to install the required dependencies.

### Requirements
- **Python 3.x**
- **OpenCV** (`cv2`)
- **Numpy**
- **Pillow** (for image processing)
  
You can install the required libraries using pip:

```bash
pip install opencv-python opencv-contrib-python numpy Pillow
```

## Setup

### 1. Clone the Repository

Clone this GitHub repository to your local machine:

```bash
git clone https://github.com/yourusername/face-recognition.git
```

### 2. Dataset Preparation

Prepare a dataset of face images for each person you want to recognize. Store each person's images in a separate folder under the `dataset/` directory. Ensure that you have at least 10-20 images for each user to improve recognition accuracy.

### 3. Train the Face Recognizer

To train the face recognition model using your dataset, run the training script:

```bash
python train.py
```

This script will extract the face images from the dataset and train the LBPH model. The trained model will be saved as `face_trainer.yml`.

### 4. Running the Face Recognition

To run the face recognition in real-time from a webcam or external video feed, use the following command:

```bash
python recognize.py
```

The system will start detecting faces and display the recognized person's name on the video stream.

## Project Structure

```
├── dataset/                # Directory to store face images
├── trainer/                # Directory to save the trained model
├── train.py                # Script to train the face recognizer
├── recognize.py            # Script to recognize faces in real-time
├── haarcascade_frontalface_default.xml # Pre-trained face detector
└── README.md               # Project documentation (this file)
```

## Issues and Debugging

### Common Errors:
1. **Error: `cv2.face.LBPHFaceRecognizer_create()` not found**  
   - Make sure you have installed the `opencv-contrib-python` package, as the face recognition algorithms are part of the `opencv-contrib` module.

   Install with:
   ```bash
   pip install opencv-contrib-python
   ```

2. **Error: cv2.imshow() not working**
   - If you encounter issues with displaying images or video frames, make sure that the `cv2.imshow()` function is called in the correct part of the code and that `cv2.waitKey(1)` is used to refresh the video stream.

## Future Enhancements
- Add support for more recognition algorithms like FisherFaces and EigenFaces.
- Integrate the system with a database for storing recognized user information.
- Develop a GUI interface for ease of use.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
