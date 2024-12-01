# Speech Commands Recognition Project

This project aims to develop a machine learning model capable of recognizing spoken commands from a dataset of audio recordings. The model is trained on a subset of the Google Speech Commands dataset, consisting of ten distinct commands spoken by multiple speakers.

## Features

* **Data Augmentation:** To improve the model's robustness and generalization ability, background noise is added to the audio samples at different signal-to-noise ratios (SNRs).
* **Data Normalization:** All audio samples are normalized to have a consistent amplitude range.
* **Feature Extraction:** Mel-frequency cepstral coefficients (MFCCs) are extracted from each audio sample to represent its spectral characteristics using librosa library.
* **Model Architecture:** Two different models are trained and compared: an artificial neural network (ANN) and a convolutional neural network (CNN).
* **Training and Validation:** The dataset is split into training and validation sets for model development and evaluation.
* **Early Stopping and Learning Rate Reduction:** Early stopping is used to prevent overfitting and learning rate reduction is applied to fine-tune the learning process.

## Dataset Information

The Google Speech Commands dataset consists of 105,829 audio samples of spoken commands from 35 speakers. The commands are divided into 35 classes, with each class containing approximately 3,000 samples. For this project, a subset of the dataset containing only ten commands is used: 'zero', 'one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', and 'nine'.

## Results

The ANN model achieves a training accuracy of 0.7911 and a validation accuracy of 0.7034, while the CNN model achieves a training accuracy of 0.8799 and a validation accuracy of 0.7499.

## How it Works

1. **Data Loading and Preprocessing:** The audio files are loaded, and background noise is added for data augmentation. The audio data is then normalized to a consistent amplitude range.
2. **Feature Extraction:** MFCCs are extracted from each audio sample to capture its spectral characteristics.
3. **Model Training:** The ANN and CNN models are trained using the extracted features and the corresponding labels.
4. **Model Evaluation:** The trained models are evaluated on a validation set to assess their performance.
5. **Visualization:** Training and validation accuracy and loss are plotted to visualize the model's learning progress.

## Conclusion

The developed models demonstrate promising performance in recognizing spoken commands from the Google Speech Commands dataset. The CNN model achieves slightly better accuracy than the ANN model, suggesting its potential for more robust and accurate command recognition.
