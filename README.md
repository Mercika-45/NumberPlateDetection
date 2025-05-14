🚘 Indian Number Plate Detection using EasyOCR
This project uses EasyOCR to detect and extract text from vehicle number plates in images. It is optimized for use in Google Colab, reads images from Google Drive, and visualizes the results using OpenCV.

📌 Features
🔍 Automatic detection and extraction of number plate text

🧠 Powered by EasyOCR with English language support

🖼️ Highlights detected text directly on images

🗂️ Processes all images in a directory (batch analysis)

💾 Loads data from Google Drive

📁 Dataset Structure
Ensure your dataset in Google Drive follows this format:

swift
Copy
Edit
/MyDrive/Indian_Number_Plates/
└── Sample_Images/
    ├── car1.jpg
    ├── car2.png
    └── ...
🔧 Dependencies
Install required libraries in your Google Colab notebook:


!pip install easyocr
!pip install opencv-python-headless
Also import essential packages:


import os
import cv2
import easyocr
from google.colab.patches import cv2_imshow
🚀 How to Use
Mount Google Drive in Colab:


from google.colab import drive
drive.mount('/content/drive')
Set dataset path:


dataset_path = '/content/drive/MyDrive/Indian_Number_Plates/Sample_Images'
Run the number plate detection script:


detected_texts = analyze_dataset(dataset_path)
View the results:

Detected number plate text will be printed and annotated on each image.

🧠 How It Works
Uses EasyOCR to scan and recognize text within images.

Bounding boxes are drawn around detected number plates.

Each result is visualized with cv2_imshow() and stored in a dictionary.

🧪 Sample Output

Processing car1.jpg...
Detected Text for car1.jpg: ['KA01AB1234']

Processing car2.png...
Detected Text for car2.png: ['MH12XY9876']
Each image will also be displayed with a green rectangle and the recognized text in blue.
