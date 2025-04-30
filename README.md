# Key Point Iris Detection Using CNN

**Key Point Iris Detection** is a deep learning-based iris detedtion system that leverages Convolutional Neural Networks (CNNs) to identify critical anatomical landmarks in human eye images, such as the iris boundary and pupil center. This approach provides high accuracy in iris recognition even in the presence of occlusions, lighting variations, and other real-world challenges. 

Unlike traditional iris recognition techniques that rely on full iris texture analysis, the model emphasizes stable, localized features—ensuring faster and more robust iris detection. This system is particularly useful for applications in security, healthcare, surveillance, and personal device access.

---

## 🔍 What is Key Point Iris Detection?

Key Point Iris Detection is an advanced computer vision technique where the focus is on identifying and predicting the coordinates of specific features (key points) within an eye image, rather than analyzing the entire iris pattern.

---

## ✅ Benefits of Key Point-Based Iris Detection

- **Robustness Against Occlusion:** Accurate detection even when eyelids, eyelashes, or glasses partially obscure the eye.
- **Enhanced Speed & Accuracy:** Detecting fewer, meaningful points leads to faster processing and lower error rates.
- **Computational Efficiency:** Less data is needed for processing, which allows real-time predictions.
- **Versatile Applications:** Can be deployed in mobile phones, surveillance systems, healthcare setups, and public safety use cases.
- **Scalability:** Compatible with large-scale identification systems where fast authentication is essential.

---

## 🧠 Project Approach

Traditional iris recognition focuses on extracting and matching entire iris textures. This project departs from that paradigm by training a model to detect and regress only the most stable and meaningful iris landmarks. 

### How it Works:
1. **Data Collection & Annotation**: A large number of high-resolution eye images annotated with key points using the LabelMe tool.
2. **Preprocessing**: Applied normalization, resizing, and data augmentation (flips, rotations, brightness changes).
3. **Model Training**:
   - Used ResNet152v2 as a backbone for its deep spatial learning capabilities.
   - CNN outputs the (x, y) coordinates of iris landmarks using regression.
   - Loss function: Mean Squared Error (MSE).
   - Optimizer: Adam.
4. **Evaluation**: Measured prediction accuracy with visual validation and MSE, precision, and recall metrics.
5. **Result**: High training accuracy and resilience to variations in image quality, with convergence observed within 100 epochs.

---


## 💻 Prerequisites

- Python 3.7+
- TensorFlow / Keras
- OpenCV
- LabelMe (for dataset preparation)
- Pandas
- NumPy
- Matplotlib


## Installation
1. Install dependencies::
   ```sh
   pip install tensorflow opencv-python numpy pandas matplotlib labelme

2. Clone the repository:
   ```sh
    git clone https://github.com/<your-username>/key-point-iris-detection.git
3. Navigate to the project directory:
    ```sh
    cd key-point-iris-detection
