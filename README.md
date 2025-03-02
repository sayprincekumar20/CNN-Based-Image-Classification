## CNN Image Classification with Overfitting Reduction

 ### Overview

This project implements a Convolutional Neural Network (CNN) for classifying images of cats and dogs using TensorFlow and Keras. It explores techniques to reduce overfitting and improve model accuracy.

Dataset

The dataset is downloaded from Kaggle using kagglehub and consists of training and validation images of cats and dogs.

Model Architectures

. Three different CNN architectures were implemented to analyze and mitigate overfitting:

1. Basic CNN Model

Trained on the dataset without any regularization.

Used convolutional layers followed by max pooling and fully connected layers.

Evaluated using training loss and accuracy.

2. CNN Model with Batch Normalization

Introduced Batch Normalization layers to normalize activations and reduce internal covariate shift.

Helped stabilize training and improve generalization.

Improved accuracy compared to the basic model.

3. CNN Model with Data Augmentation

Implemented data augmentation using ImageDataGenerator to generate more diverse training samples.

Applied transformations like rescaling, zooming, horizontal flipping, and shear transformations.

Further reduced overfitting and improved model robustness.

Training & Evaluation

Models were compiled using the Adam optimizer and binary cross-entropy loss.

Accuracy and loss curves were plotted for both training and validation datasets.

The best-performing model incorporated both batch normalization and data augmentation.

Testing

The trained model was tested using sample images of cats and dogs.

Predictions were made using OpenCV for image preprocessing.

Techniques to Reduce Overfitting

Adding more data

Data Augmentation

L1/L2 Regularization

Dropout layers

Batch Normalization

Reducing model complexity

Results

The model with both batch normalization and data augmentation achieved the highest accuracy.

Overfitting was significantly reduced compared to the basic CNN model.

Conclusion

This project demonstrated the effectiveness of batch normalization and data augmentation in improving CNN performance and reducing overfitting. These techniques help in building more generalizable models for image classification tasks.
