🧠 Real-Time Age and Gender Detection using OpenCV & Deep Learning

This project implements a real-time age and gender detection system using OpenCV’s deep learning module (DNN) and pre-trained Caffe models. The system captures live video from a webcam, detects faces, and predicts the age range and gender of each detected individual in real time.

🚀 Features

Detects faces in live video streams.

Predicts age range (e.g., 0–2, 4–6, 8–12, etc.).

Predicts gender (Male/Female).

Uses deep learning models for accurate predictions.

Lightweight, runs efficiently on CPU.

Simple and easy to use with minimal setup.

🧩 Technologies Used

Python 3.x

OpenCV (cv2.dnn module)

NumPy

Pre-trained Caffe models:

age_net.caffemodel

age_deploy.prototxt

gender_net.caffemodel

gender_deploy.prototxt

opencv_face_detector.caffemodel

opencv_face_detector.prototxt

🛠️ Installation and Setup
1. Clone this repository
git clone https://github.com/<your-username>/real-time-age-gender-detector.git
cd real-time-age-gender-detector

2. Install dependencies
pip install opencv-python numpy

3. Download model files

Download the required Caffe model files and place them in a folder named models/:

AgeNet model

GenderNet model

Face detection model

Directory structure should look like:

real-time-age-gender-detector/
│
├── models/
│   ├── age_deploy.prototxt
│   ├── age_net.caffemodel
│   ├── gender_deploy.prototxt
│   ├── gender_net.caffemodel
│   ├── opencv_face_detector.prototxt
│   ├── opencv_face_detector.caffemodel
│
└── age_gender_detector.py

🧠 How It Works

The face detector uses OpenCV’s deep learning-based SSD face detection model.

Each detected face is cropped and passed to the age and gender networks.

The models predict probabilities across categories (8 for age, 2 for gender).

The result is displayed in real time with bounding boxes and labels.

▶️ Running the Program

Run the following command:

python age_gender_detector.py


A window will open showing the webcam feed. The detected age range and gender will appear above each detected face.

Press ‘q’ to quit the program.

📊 Example Output
[INFO] Gender: Male
[INFO] Age Range: (25-32)


🖼️ (You can add screenshots or demo GIFs here if available)

⚙️ Code Overview
getFaceBox(net, frame, conf_threshold)

Detects faces in each frame using OpenCV’s DNN.

Main loop:

Captures video from webcam.

Runs face detection.

For each detected face:

Crops and preprocesses the region.

Feeds it into both the age and gender models.

Displays results in real time.

🧮 Age & Gender Labels

Age Groups:

['(0-2)', '(4-6)', '(8-12)', '(15-20)', '(25-32)', '(38-43)', '(48-53)', '(60-100)']


Gender Labels:

['Male', 'Female']

💡 Applications

Audience analytics (e.g., in retail, events)

Smart advertising systems

Human-computer interaction

Demographic data collection

🧑‍💻 Author

Krish Bharadwaj
📍 Manipal Institute of Technology
💼 Aspiring AI Engineer | Passionate about Computer Vision and Deep Learning

🪪 License

This project is licensed under the MIT License – you’re free to use, modify, and distribute it with proper attribution.
