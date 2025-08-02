# 🥗 nutriVision: From Image to Insight

**nutriVision** is an intelligent computer vision system that transforms a simple photo of your fridge or pantry into a list of ingredients, their nutritional information, and delicious recipe suggestions. Using a custom-trained **YOLOv5** model, it bridges the gap between what you have and what you can create.

---

## 📸 Demo Preview

| Main Page | Ingredient Detection | Recipe Recommendations | Nutritional Analysis |
| :---: | :---: | :---: | :---:
| ![Main Page](https://github.com/user-attachments/assets/68a25f6a-f7b0-4bec-8ff1-c68107385e5f) | ![Ingredient Detection](https://github.com/user-attachments/assets/b61a9e3e-da78-40e0-a5a4-8073a5396f56) | ![Recipe Recommendations](https://github.com/user-attachments/assets/486fd131-a137-4190-9232-0eff2fcb3a74) | ![Nutritional Analysis](https://github.com/user-attachments/assets/dc6be91e-f258-428f-88c8-bde1a9134993) 

---

## ✨ Core Features

-   **📸 Smart Ingredient Detection**: Utilizes a custom-trained YOLOv5 model to accurately detect multiple food items (like *tomato, onion, bell pepper, etc.*) in a single image.
-   **📊 Instant Nutritional Analysis**: Once ingredients are detected, the system displays key nutritional data (e.g., calories, protein, carbs, fats) for each item, helping you make informed dietary choices.
-   **🍲 Intelligent Recipe Suggestions**: Based on the detected ingredients, nutriVision recommends recipes you can make right away, reducing food waste and sparking culinary inspiration.
-   **🖼️ Clear Visual Feedback**: Generates an output image with bounding boxes and class labels overlaid, showing you exactly what the model identified.

---

## 🛠️ Tech Stack & Architecture

-   **Object Detection**: **YOLOv5** (custom trained on a diverse food dataset)
-   **Core Libraries**: **PyTorch**, **OpenCV**
-   **Data Handling**: **Pandas**, **YAML**

The workflow is simple: an image is fed into the `detect.py` script, which uses the `nutrition_best.pt` model weights to identify ingredients. This list is then used to fetch nutritional data and recipe information.

---

## 🚀 Getting Started

### ✅ Prerequisites
-   Python 3.8+
-   PyTorch
-   All packages listed in the `yolov5/requirements.txt` file.

### 🔧 Installation & Setup

1.  **Clone the repository and its submodules (YOLOv5):**
    ```bash
    git clone [https://github.com/Greeshma-10/nutriVision.git](https://github.com/Greeshma-10/nutriVision.git)
    cd nutriVision
    ```

2.  **Install dependencies:**
    Navigate to the YOLOv5 directory and install the required packages.
    ```bash
    cd yolov5
    pip install -r requirements.txt
    ```
    Return to the root directory: `cd ..`

3.  **Place Model Weights:**
    Ensure your trained model file, `nutrition_best.pt`, is located in the root `nutriVision/` directory.

### ▶️ Running Detection

Run the detection script from the **root directory** on any image:
```bash
python yolov5/detect.py --weights nutrition_best.pt --img 640 --conf 0.4 --source test_images/your_image.jpg
```
Of course. Here is a refined version of your README.md that incorporates recipe recommendations, nutritional analysis, and image placeholders for a more professional and complete look.

Markdown

# 🥗 nutriVision: From Image to Insight

**nutriVision** is an intelligent computer vision system that transforms a simple photo of your fridge or pantry into a list of ingredients, their nutritional information, and delicious recipe suggestions. Using a custom-trained **YOLOv5** model, it bridges the gap between what you have and what you can create.

---

## 📸 Demo Preview

| 1. Ingredient Detection | 2. Nutritional Analysis | 3. Recipe Recommendations |
| :---: | :---: | :---: |
| ![Ingredient Detection](https://i.imgur.com/REPLACE_WITH_DETECTION_URL.png) | ![Nutritional Analysis](https://i.imgur.com/REPLACE_WITH_NUTRITION_URL.png) | ![Recipe Recommendations](https://i.imgur.com/REPLACE_WITH_RECIPE_URL.png) |

---

## ✨ Core Features

-   **📸 Smart Ingredient Detection**: Utilizes a custom-trained YOLOv5 model to accurately detect multiple food items (like *tomato, onion, bell pepper, etc.*) in a single image.
-   **📊 Instant Nutritional Analysis**: Once ingredients are detected, the system displays key nutritional data (e.g., calories, protein, carbs, fats) for each item, helping you make informed dietary choices.
-   **🍲 Intelligent Recipe Suggestions**: Based on the detected ingredients, nutriVision recommends recipes you can make right away, reducing food waste and sparking culinary inspiration.
-   **🖼️ Clear Visual Feedback**: Generates an output image with bounding boxes and class labels overlaid, showing you exactly what the model identified.

---

## 🛠️ Tech Stack & Architecture

-   **Object Detection**: **YOLOv5** (custom trained on a diverse food dataset)
-   **Core Libraries**: **PyTorch**, **OpenCV**
-   **Data Handling**: **Pandas**, **YAML**

The workflow is simple: an image is fed into the `detect.py` script, which uses the `nutrition_best.pt` model weights to identify ingredients. This list is then used to fetch nutritional data and recipe information.

---

## 🚀 Getting Started

### ✅ Prerequisites
-   Python 3.8+
-   PyTorch
-   All packages listed in the `yolov5/requirements.txt` file.

### 🔧 Installation & Setup

1.  **Clone the repository and its submodules (YOLOv5):**
    ```bash
    git clone [https://github.com/Greeshma-10/nutriVision.git](https://github.com/Greeshma-10/nutriVision.git)
    cd nutriVision
    ```

2.  **Install dependencies:**
    Navigate to the YOLOv5 directory and install the required packages.
    ```bash
    cd yolov5
    pip install -r requirements.txt
    ```
    Return to the root directory: `cd ..`

3.  **Place Model Weights:**
    Ensure your trained model file, `nutrition_best.pt`, is located in the root `nutriVision/` directory.

### ▶️ Running Detection

Run the detection script from the **root directory** on any image:
```bash
python yolov5/detect.py --weights nutrition_best.pt --img 640 --conf 0.4 --source test_images/your_image.jpg
```
--weights: Path to your custom model.

--conf: The confidence threshold for detection (e.g., 0.4 for 40%).

--source: The directory or specific image you want to analyze.

The annotated output images will be saved automatically in the yolov5/runs/detect/ directory.

📁 Project Structure
```text
nutriVision/
│
├── yolov5/              # Cloned YOLOv5 official repository
├── test_images/         # Folder with sample images for testing
│
├── nutrition_best.pt    # Your trained model weights
├── requirements.txt     # Main project requirements
└── README.md            # This file
```
