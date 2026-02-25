# AI-Enhanced Litter Detection for Smart Park Management
**A YOLOv8 Implementation for Finlay Park, Columbia, SC**

## Project Overview
As Columbia, SC prepares for the reopening of Finlay Park, this project explores the use of Computer Vision to automate park maintenance. By implementing a YOLOv8 object detection model, this system identifies litter in urban green spaces to assist maintenance crews and provide a foundation for future autonomous cleanup robotics.

## Key Features
* **YOLOv8 Architecture:** Utilizes state-of-the-art real-time object detection.
* **Optimized Pipeline:** Developed in Google Colab using NVIDIA L4 GPU acceleration.
* **Data Iteration:** Comparative analysis of model performance across three dataset variants (Initial, Modified, and Cleaned).

## Project Assets
* **[Final Technical Report](./docs/final-project-report.pdf):** Detailed analysis of hyperparameter tuning (Adam optimizer, weight decay) and performance bottlenecks.
* **[Technical Notebook](./analysis/litter-detection-final.ipynb):** The full training and evaluation pipeline.
* **[Model Weights (External Link)]:** Due to file size limits, the `.pt` weights for the optimal model runs are hosted on Google Drive. 
  * 🔗 **[Download Best Model Weights Here](https://drive.google.com/drive/folders/1qblkHTL7nrIr_CUAgvHIaXIqZEy6LrUD?usp=sharing)**

## Technical Usage
The included notebook is set up for both training and immediate inference. To test the model without re-training:

1. **Download the Weights:** Get the `best.pt` file from the [Google Drive Link](https://drive.google.com/drive/folders/1qblkHTL7nrIr_CUAgvHIaXIqZEy6LrUD?usp=sharing).
2. **Open the Notebook:** Launch `analysis/litter-detection-final.ipynb` in Google Colab.
3. **Run the "Quick Start" Cell:** Navigate to the final cell in the notebook. Upload the `best.pt` file to the Colab sidebar and run the cell to see the model detect litter in real-time.
