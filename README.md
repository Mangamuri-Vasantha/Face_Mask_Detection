# Face_Mask_Detection
📌 Project Overview
This project detects whether a person is wearing a face mask or not in real-time using a webcam. It uses a Convolutional Neural Network (CNN) trained on masked and unmasked face images and integrates with OpenCV for live video detection.

🎯 Objective
Detect faces in real-time

Classify each face as:

Mask
No Mask
Display result with colored bounding boxes

🛠️ Technologies Used
Python
OpenCV
TensorFlow / Keras
NumPy
Scikit-learn
📂 Project Structure
FaceMaskDetection/
│
├── dataset/
│   ├── with_mask/
│   └── without_mask/
│
├── models/
│   └── mask_detector.keras
│
├── train_model.py
├── detect_mask.py
├── haarcascade_frontalface_default.xml
├── requirements.txt
└── README.md
📊 Dataset
Dataset contains two categories:

with_mask
without_mask
Images are resized to 100x100 and normalized before training.

You can download dataset from Kaggle: Face Mask Dataset

🧠 Model Architecture
Conv2D (32 filters)
MaxPooling
Conv2D (64 filters)
MaxPooling
Flatten
Dense (64)
Output layer (Softmax – 2 classes)
Loss: Categorical Crossentropy Optimizer: Adam

🚀 How to Run the Project
Step 1: Clone Repository
git clone <your-repo-link>
cd FaceMaskDetection
Step 2: Create Virtual Environment
python -m venv venv
venv\Scripts\activate
Step 3: Install Dependencies
pip install -r requirements.txt
Step 4: Train the Model
python train_model.py
This will create:

models/mask_detector.keras
Step 5: Run Real-Time Detection
python detect_mask.py
Press ESC to stop the webcam.

🖥️ Output
Green box → Mask
Red box → No Mask
Real-time detection through webcam
📈 Results
Training Accuracy: ~90–95%
Real-time performance using OpenCV
💡 Future Improvements
Add alert sound for No Mask
Deploy using Flask web app
Use MobileNetV2 for higher accuracy
Deploy on edge devices
