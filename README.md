# Plant Disease Classification using Transfer Learning

## Overview
This project utilizes transfer learning with the VGG16 model to classify plant diseases based on images. The Convolutional Neural Network (CNN) is trained on a dataset containing images of healthy and diseased plants. The project is implemented using Python with Keras and TensorFlow libraries.

## Dataset
The dataset is stored in the "Plant Dataset" directory on Google Drive, consisting of separate training and testing sets. The training set includes images of healthy and diseased plants, organized into class subdirectories.

### Data Structure
- **Train:** Contains subdirectories for each plant class (e.g., Healthy, Diseased), with corresponding images for training.
  
- **Test:** Similar to the train directory, the test directory contains subdirectories for each plant class, with images for testing the model.

## Usage
1. **Environment Setup:**
   - Clone the repository.
   - Install required dependencies (numpy, pandas, matplotlib, keras, tensorflow, opencv, scikit-learn).

2. **Dataset Directory:**
   - Ensure the dataset is stored in the specified structure:
     ```
     /content/drive/MyDrive/Plant Dataset (1)
     ├── Train
     │   ├── Healthy
     │   └── Diseased
     ├── Test
     │   ├── Healthy
     │   └── Diseased
     ```

3. **Model Training:**
   - The CNN model is trained using transfer learning with the pre-trained VGG16 model.
   - Training data is augmented and normalized using ImageDataGenerator.
   - The model is compiled with Nadam optimizer and categorical cross-entropy loss.
   - After training for 30 epochs, the model is evaluated on the validation set.

4. **Fine-tuning:**
   - The VGG16 base layers are unfrozen for fine-tuning.
   - Fine-tuning is applied to specific layers to adapt the model for plant disease classification.

5. **Results Visualization:**
   - Training and validation accuracy, as well as loss, are visualized using Matplotlib.
   - Average validation accuracy and loss are displayed.

6. **Model Evaluation:**
   - The trained model is evaluated on the test dataset, and test accuracy is reported.

## Acknowledgments
- The VGG16 model is pre-trained on the ImageNet dataset, and credit goes to the original authors.

Feel free to explore the code and adapt it to your specific needs. If you encounter any issues or have questions, please refer to the documentation or seek support from relevant communities.
