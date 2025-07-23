# Face-Recoginition
This project includes two files:
The first file captures images to create a dataset and trains a model to detect faces.
The second file uses the dataset created by the first file to recognize the faces of different users.

**Description of the first file:**
📸 Face Image Collector using OpenCV
This Python script uses OpenCV to detect faces from a webcam feed and saves them to a dataset for training facial recognition models later.

🔧 What It Does
Detects faces using Haar Cascade (haarcascade_frontalface_default.xml)
Captures and stores 130 grayscale face images (130x100 px) per user
Saves the images under datasets/<user_name>/ folder (e.g., datasets/Prag/)
Displays the webcam feed with face rectangles drawn
Stops automatically after 130 images or if Esc key is pressed

🧪 Requirements
Python 
OpenCV (cv2)
Haarcascade XML file (included in OpenCV)

🗂️ Folder Structure
markdown
Copy
Edit
datasets/
└── Prag/
    ├── 1.png
    ├── 2.png
    └── ...

💡 Usage Notes
Change sub_data = 'Prag' to your name or user label.
cv2.VideoCapture(0) uses the default webcam. Change 0 to 1 if you’re using an external camera.
Script collects 130 face samples for the user.



**Description of the second file:**

🧠 Real-Time Face Recognition using OpenCV (LBPH)
This Python script performs real-time face recognition using the Local Binary Patterns Histograms (LBPH) algorithm from OpenCV.

🔧 What It Does
Loads previously captured face images from the datasets/ directory
Trains a face recognizer model (LBPH)
Opens the webcam and detects faces in real-time
Predicts and labels recognized faces with confidence scores
Displays “not recognized” for unknown faces

📂 Folder Structure
Copy
Edit
datasets/
├── Prag/
│   ├── 1.png
│   ├── 2.png
│   └── ...

💡 Key Features
Uses Haar Cascade Classifier for face detection.
Uses LBPH Face Recognizer for identification.
Dynamically builds label mappings from subfolder names.
Shows live recognition with confidence score.

🗝️ Important Details
haar_file must point to haarcascade_frontalface_default.xml.
Recognition threshold: faces with prediction confidence < 500 are considered “recognized”.
Webcam feed stops on pressing Esc.

🧪 Requirements
Python 
OpenCV (with opencv-contrib-python for LBPH support)
pip install opencv-contrib-python

📌 How It Works
Training Phase:
Walks through datasets/, collects grayscale images and labels.
Trains a model using LBPH (cv2.face.LBPHFaceRecognizer_create()).

Recognition Phase:
Opens webcam.
Detects face using Haar cascades.
Resizes and predicts the face.
Displays name and confidence or “not recognized”.

