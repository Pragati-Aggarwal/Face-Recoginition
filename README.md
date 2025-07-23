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
Python 3

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



