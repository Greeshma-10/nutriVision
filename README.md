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
├── yolov5/               # YOLOv5 official repo (cloned locally)
├── runs/                 # YOLOv5 output folder with inference results
├── nutrition_best.pt     # Trained model weights
├── test_images/          # Sample test images
├── detect.py             # Modified script for local detection
├── README.md             # This file
└── requirements.txt      # Required Python packages

```

## 🚀 Getting Started
✅ Prerequisites
1. Python 3.8+
2. PyTorch
3. OpenCV

All packages from the yolov5/requirements.txt file

## 🔧 Installation & Setup
Clone the repository:

```Bash

git clone https://github.com/Greeshma-10/nutriVision.git
cd nutriVision
```
## Install dependencies:
Navigate to the YOLOv5 directory and install the required packages.

```Bash

cd yolov5
pip install -r requirements.txt
Return to the root directory: cd ..
```

## Place Model Weights:
Ensure your trained model file, nutrition_best.pt, is located in the main nutriVision/ directory.

## ▶️ Run Detection
Execute the detection script from the root directory on a sample image:

```Bash

python yolov5/detect.py --weights nutrition_best.pt --img 640 --conf 0.25 --source test_images/your_image_name.jpg
```
The annotated output images will be saved in the yolov5/runs/detect/exp directory.images
