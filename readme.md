# Baldness Classification

This project focuses on classifying images to determine whether a person is bald or has a bald spot using machine learning techniques. The dataset used for training and testing is the [Bald Classification 200K Images CelebA Dataset](https://www.kaggle.com/datasets/ashishjangra27/bald-classification-200k-images-celeba) from Kaggle.

## Dataset

The dataset contains a large collection of celebrity images, annotated with labels indicating whether the person in the image is bald or not. It provides a diverse set of images to train and evaluate the baldness classification model. To save time, we only use a total of 2,000 photos, as calculations can quickly become very time-consuming.

## Model Training

The code in this repository performs the following steps:

1. Loads the training data from the provided dataset, specifically from the `Dataset/Train` directory.
2. Reshapes and normalizes the image data.
3. Uses a Support Vector Machine (SVM) classifier with a pipeline that includes standard scaling for feature normalization.
4. Trains the model using the training data.
5. Evaluates the trained model's performance using the confusion matrix and calculates the accuracy score.

## `training-save` File

The `training-save` file is the serialized form of the trained classifier model. It is created using the `joblib` library's `dump` function. This file can be loaded and used later for making predictions on new or unseen data without the need for retraining the model.

## Testing the Model

After training and saving the model, you can test it by running the provided code. It selects a random image from the `Dataset/Test` directory, predicts whether the person in the image is bald or not, and displays the result along with the image.

Feel free to explore and modify the code as necessary in your rating process.