# CNN-Based-Image-Classification
Summary Analysis of CNN-Based Image Classification Code

1. Dataset Loading

The dataset is downloaded using kagglehub from salader/dogs-vs-cats.

The dataset path is determined, and its directory structure is checked using os.listdir(dataset_path).

2. Data Preprocessing & Generators

keras.utils.image_dataset_from_directory is used to load training and validation data from directories.

Image size is set to (256, 256) with a batch size of 32.

A preprocessing function normalizes images by scaling pixel values between 0 and 1.

The datasets are mapped to the normalization function to ensure consistent input.

3. Initial CNN Model Architecture

Conv2D layers are used to extract features, with ReLU activation.

MaxPooling2D layers reduce spatial dimensions and computational complexity.

Flatten layer converts the extracted features into a 1D vector.

Dense layers include:

128 neurons with ReLU activation

64 neurons with ReLU activation

1 neuron with Sigmoid activation (binary classification)

The model is compiled with:

Adam optimizer

Binary cross-entropy loss function

Accuracy as a performance metric

Model is trained for 10 epochs.

4. Model Performance Visualization

Training and validation accuracy/loss curves are plotted using Matplotlib to analyze performance.

The accuracy curve helps identify convergence and overfitting trends.

5. Overfitting Reduction Strategies

The following techniques are suggested to reduce overfitting:

More training data

Data augmentation

L1/L2 Regularization

Dropout layers

Batch Normalization

Reducing model complexity

A new CNN model is built incorporating Batch Normalization and Dropout (0.1 probability) to improve generalization.

6. Testing Model Predictions

Sample test images (cat.jpeg and dog.jpeg) are loaded using cv2.imread().

Images are resized to (256, 256) and reshaped before prediction.

The trained model is used to classify these images using model.predict().

7. Data Augmentation for Further Overfitting Reduction

ImageDataGenerator is used to apply augmentation techniques:

Rescaling (Normalization)

Zooming (0.2 factor)

Horizontal flipping

Shear transformation (0.2 factor)

Training and validation generators are created using flow_from_directory().

8. Final Model with Augmentation and Batch Normalization

The CNN model is enhanced with Batch Normalization after each convolutional layer.

Dropout is maintained to further reduce overfitting.

The model is compiled and trained using the augmented dataset.

Training performance is visualized again using accuracy/loss curves.

9. Conclusion

The model undergoes iterative improvements to enhance generalization.

Overfitting is addressed through Batch Normalization, Dropout, and Data Augmentation.

The final model is expected to perform better on unseen data due to these optimizations.


