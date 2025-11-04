# 🧠 Real-Time Age & Gender Detection  
🎥 A deep learning–powered system that detects faces and predicts **age range** and **gender** in real time using OpenCV’s DNN module and pre-trained Caffe models.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?logo=python">
  <img src="https://img.shields.io/badge/OpenCV-DNN-red?logo=opencv">
  <img src="https://img.shields.io/badge/DeepLearning-Caffe-green?logo=deeplearning">
  <img src="https://img.shields.io/badge/License-MIT-yellow">
</p>

---

## 🌟 Overview
This project implements **real-time face, age, and gender detection** using **OpenCV’s deep learning module (DNN)** and **pre-trained Caffe models**.  
It captures live video from your webcam, detects faces, and predicts the **gender** and **approximate age range** for each detected person — all in real time!

> 🧩 Lightweight, efficient, and easy to integrate into any computer vision pipeline.

---

## ✨ Features
- 🧍 Real-time **face detection**  
- 🧒 Accurate **age range prediction**  
- 🚻 Reliable **gender classification**  
- ⚡ Runs efficiently on CPU (no GPU required)  
- 🧰 Built using pre-trained deep learning models  

---

## 🧰 Tech Stack
| Component | Description |
|------------|-------------|
| **Language** | Python 3.x |
| **Libraries** | OpenCV, NumPy |
| **DL Framework** | Caffe (via `.prototxt` and `.caffemodel` files) |
| **Models Used** | FaceNet, AgeNet, GenderNet |

---

## 📁 Folder Structure
```
real-time-age-gender-detector/
│
├── models/
│ ├── age_deploy.prototxt
│ ├── age_net.caffemodel
│ ├── gender_deploy.prototxt
│ ├── gender_net.caffemodel
│ ├── opencv_face_detector.prototxt
│ ├── opencv_face_detector.caffemodel
│
├── age_gender_detector.py
└── README.md
```
---

## ⚙️ Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/real-time-age-gender-detector.git
cd real-time-age-gender-detector
```
### 2️⃣ Install Dependencies
```
pip install opencv-python numpy
```
### 3️⃣ Download Model Files
Download the required Caffe models from LearnOpenCV’s Age-Gender Repo
and place them inside the models/ directory as shown above.

---

### ▶️ Run the Program
To start the live webcam detection:
- python age_gender_detector.py
- Press q to exit the window.

📊 Example Output
[INFO] Gender: Male
[INFO] Age Range: (25-32)

### 🧠 How It Works
- Face Detection – Uses OpenCV’s DNN face detector (opencv_face_detector.caffemodel).
- Preprocessing – Detected face is cropped, resized, and converted into a blob.
- Prediction – The blob is passed to AgeNet and GenderNet for inference.
- Display – Results (age & gender) are displayed above the detected face in real time.

### 🧩 Model Labels

- Age Groups:

> ['(0-2)', '(4-6)', '(8-12)', '(15-20)', '(25-32)', '(38-43)', '(48-53)', '(60-100)']

- Gender:

> ['Male', 'Female']
---
### 💡 Applications

- 👁️ Audience analytics
- 🏬 Smart advertising and retail insights
- 🤖 Human-computer interaction
- 🕵️ Surveillance & demographic estimation

# 🧑‍💻 Author

Krish Bharadwaj
- 📍 Manipal Institute of Technology
- 💼 Aspiring AI Engineer | Passionate about Computer Vision & Deep Learning

<p align="left"> <a href="https://www.linkedin.com/in/krish-vardhan-bharadwaj-469b1720a" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-Krish_Vardhan_Bharadwaj-blue?logo=linkedin"></a> <a href="mailto:krishvardhanbharadwaj@gmail.com"><img src="https://img.shields.io/badge/Email-krish-red?logo=gmail"></a> </p>
🪪 License

This project is licensed under the MIT License — feel free to use, modify, and share it with proper credit.
