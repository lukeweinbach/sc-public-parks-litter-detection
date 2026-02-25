# AI-Enhanced Litter Detection for Smart Park Management
**A YOLOv8 Implementation for Finlay Park, Columbia, SC**

## 📌 Project Overview
As Columbia, SC prepares for the reopening of Finlay Park, this project explores the use of Computer Vision to automate park maintenance. By implementing a YOLOv8 object detection model, this system identifies litter in urban green spaces to assist maintenance crews and provide a foundation for future autonomous cleanup robotics.

## 🚀 Key Features
* **YOLOv8 Architecture:** Utilizes state-of-the-art real-time object detection.
* **Optimized Pipeline:** Developed in Google Colab using NVIDIA L4 GPU acceleration.
* **Data Iteration:** Comparative analysis of model performance across three dataset variants (Initial, Modified, and Cleaned).

## 📂 Project Assets
* **[Final Technical Report](./docs/final-project-report.pdf):** Detailed analysis of hyperparameter tuning (Adam optimizer, weight decay) and performance bottlenecks.
* **[Technical Notebook](./analysis/litter-detection-final.ipynb):** The full training and evaluation pipeline.
* **[Model Weights (External Link)]:** Due to file size limits, the `.pt` weights for the optimal model runs are hosted on Google Drive. 
  * 🔗 **[Download Best Model Weights Here](PASTE_YOUR_GOOGLE_DRIVE_LINK_HERE)**

## 💻 Technical Usage
To use the pre-trained weights without re-running the entire training pipeline, ensure you have the `ultralytics` library installed and use the following snippet:

```python
from ultralytics import YOLO

# Load the best-performing weights from the Cleaned Dataset run
model = YOLO('path/to/downloaded/best.pt')

# Run inference on a local image or video
results = model.predict(source='park_sample.jpg', conf=0.25)

# View results
results[0].show()
