# 🥗 nutriVision: Food Item Detection using YOLOv5

**nutriVision** is a computer vision project that uses a custom-trained **YOLOv5** model to detect common food items and ingredients from fridge or kitchen images.


## 📌 Features

- 🔍 Detects multiple food items in a single image
- 🧠 Trained on a custom dataset with food classes like:
  - tomato, onion, avocado, carrot, eggplant, bell pepper, beans, beet, etc.
- 🖼️ Generates bounding boxes and class labels
- 🛠️ Ready for future extension (e.g., recipe recommendation)

## 🏗️ Project Structure
```text
nutriVision/
│
├── yolov5/ # YOLOv5 official repo (cloned locally)
├── runs/ # YOLOv5 output folder with inference results
├── nutrition_best.pt # Trained model weights
├── test_images/ # Sample test images
├── detect.py # Modified script for local detection
├── README.md # This file
└── requirements.txt # Required Python packages

```

## 🚀 Getting Started

### 1. Clone the repo and install requirements

git clone https://github.com/Greeshma-10/nutriVision.git
cd nutriVision/yolov5
pip install -r requirements.txt

### 2. Place your model weights
Make sure nutrition_best.pt is in the correct path (either root or inside yolov5/).

### 3. Run detection on an image

python detect.py --weights nutrition_best.pt --img 640 --conf 0.25 --source ../test_images
Outputs will be saved in runs/detect/exp with bounding boxes drawn.

📦 Requirements
Python 3.8+

PyTorch

OpenCV

YOLOv5 dependencies (requirements.txt from their repo)

