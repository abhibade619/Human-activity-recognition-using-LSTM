# Human Activity Recognition using CNN and LSTM

This project focuses on recognizing human activities from video data using advanced machine learning models including Convolutional LSTM (ConvLSTM) and Long-term Recurrent Convolutional Network (LRCN). The goal is to accurately classify and predict different human actions by processing video frames.

---

## Table of Contents
1. [Preprocessing the Dataset](#preprocessing-the-dataset)
2. [Splitting Data](#splitting-data)
3. [Model Construction](#model-construction)
4. [Model Evaluation and Visualization](#model-evaluation-and-visualization)
5. [Application on New Data](#application-on-new-data)
6. [License](#license)

---

## Preprocessing the Dataset
The video files are initially processed using OpenCV to convert each video into frames. These frames are resized to fixed dimensions and the pixel values are normalized to the range [0-1] to facilitate faster training convergence.

---

## Splitting Data
The processed frames (features) and one-hot encoded class labels (labels) are divided into training and testing sets, ensuring that the split represents the overall distribution of the data accurately through shuffling.

---

## Model Construction
### ConvLSTM Model Setup
- Utilizes Keras's ConvLSTM2D layers, suitable for spatial-temporal data.
- Incorporates MaxPooling3D and Dropout layers to reduce dimensionality and prevent overfitting.

![LSTM_images](https://github.com/user-attachments/assets/ec76d2df-d068-469f-9887-c2a965199033)

### LRCN Model Setup
- Employs the Long-term Recurrent Convolutional Network model, effective for visual input sequence prediction tasks.
![LRCN_Architecture](https://github.com/user-attachments/assets/40d69e40-1b0d-4f9d-a51f-f7af7c3c6fd4)

### Model Visualization
- Both models are visualized using the `plot_model()` function to ensure the correctness and integrity of the architectures.

---

## Model Evaluation and Visualization
### Evaluation
- Models are evaluated on the test set to determine accuracy and other relevant metrics (The test test is from real time data from Youtube.)

### Visualization of Loss and Accuracy
- Training and validation metrics for both models are visualized to assess performance across different epochs.
![Total VS Validation Accuracy](https://github.com/user-attachments/assets/d63254cc-e334-4ba5-a1c8-87c2363d8ed7)
![Total VS Validation Loss](https://github.com/user-attachments/assets/eb229a00-af1a-41ef-81f1-3dc39e8bd930)
---

## Application on New Data
### Downloading YouTube Videos
- A function is set up to download YouTube videos for testing the models.

### Action Recognition on New Videos
- Trained models are applied to downloaded YouTube videos to recognize human actions, with results displayed directly on the videos.

---

## License
This project is licensed under the MIT License. For more details, see the [LICENSE.md](LICENSE.md) file.

