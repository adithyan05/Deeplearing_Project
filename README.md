# Handwritten Digit Recognition Using CNN

A deep learning project that recognizes handwritten digits (0–9) using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. The project includes an interactive drawing interface using Gradio, allowing users to draw a digit and receive the model's prediction with confidence scores.

## Project Overview

Handwritten digit recognition is a computer vision task that involves identifying numerical digits from images. This project uses the MNIST dataset to train a CNN capable of classifying grayscale handwritten digit images into ten classes, from 0 to 9.

Users can interact with the trained model through a web-based drawing canvas, making the project easy to demonstrate and test.

## Features

- Handwritten digit classification from 0 to 9.
- CNN architecture for automatic feature extraction.
- MNIST dataset loading and preprocessing.
- Image normalization and resizing.
- Model training using backpropagation and the Adam optimizer.
- Training and validation accuracy/loss visualization.
- Model evaluation using test accuracy and a confusion matrix.
- Interactive drawing canvas using Gradio.
- Prediction confidence scores for digit recognition.
- Trained model export in Keras format.

## Technologies Used

- **Python** — Programming language
- **TensorFlow and Keras** — Deep learning model development
- **NumPy** — Numerical computations and image preprocessing
- **Matplotlib** — Data visualization
- **Scikit-learn** — Classification metrics and confusion matrix
- **Pillow (PIL)** — Image processing
- **Gradio** — Interactive web interface
- **Google Colab** — Cloud-based development and training environment

## Dataset

The project uses the MNIST handwritten digit dataset.

| Property | Description |
|---|---|
| Total images | 70,000 |
| Training images | 60,000 |
| Testing images | 10,000 |
| Image dimensions | 28 × 28 pixels |
| Image format | Grayscale |
| Number of classes | 10 (digits 0–9) |

The dataset is loaded directly through `tensorflow.keras.datasets.mnist`, so manual downloading is unnecessary.

## CNN Architecture

The model consists of the following layers:

1. **Input Layer:** Accepts 28 × 28 grayscale images.
2. **Convolutional Layer:** Extracts visual features using 32 filters and ReLU activation.
3. **Max Pooling Layer:** Reduces spatial dimensions.
4. **Convolutional Layer:** Extracts higher-level features using 64 filters.
5. **Max Pooling Layer:** Further reduces feature-map dimensions.
6. **Flatten Layer:** Converts feature maps into a one-dimensional vector.
7. **Dense Layer:** Learns patterns for digit classification.
8. **Dropout Layer:** Helps reduce overfitting during training.
9. **Output Layer:** Uses softmax to produce probabilities for the ten digit classes.

### Training Configuration

- Optimizer: Adam
- Loss function: Sparse categorical cross-entropy
- Batch size: 128
- Epochs: 5
- Validation split: 10%
- Evaluation metric: Accuracy

## Installation and Execution

### Option 1: Run in Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new Python notebook.
3. Copy the project code into the notebook in the correct order.
4. Install Gradio:

   ```python
   !pip install gradio
   ```

5. Load the MNIST dataset and preprocess the images.
6. Build and train the CNN model.
7. Evaluate the model and generate visualizations.
8. Launch the Gradio interface using:

   ```python
   demo.launch(share=True)
   ```

9. Open the generated public URL to test the application.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/handwritten-digit-recognition-cnn.git
cd handwritten-digit-recognition-cnn
```

Install the dependencies:

```bash
pip install tensorflow numpy matplotlib scikit-learn pillow gradio
```

Open the notebook in Jupyter or upload it to Google Colab and execute the cells in order.

**Note:** If you run the notebook locally, ensure the required Python packages are installed and that the notebook contains the complete training and interface code.

## How to Use the Application

1. Launch the Gradio interface.
2. Draw a handwritten digit between 0 and 9 using the mouse.
3. Click the **Submit** button.
4. The trained CNN processes the drawing and predicts the digit.
5. View the predicted class and its confidence score.

The model works best with clear, centered digits that resemble the MNIST training images.

## Results and Evaluation

The model is evaluated on the MNIST test dataset, which is separate from the training data.

Evaluation includes:

- Test accuracy and loss.
- Training and validation accuracy curves.
- Training and validation loss curves.
- Classification report.
- Confusion matrix.
- Predictions from the interactive drawing interface.

**Test accuracy:** Add the actual accuracy obtained after running the notebook.

## Applications

- Automated digit recognition
- Postal code recognition
- Bank cheque processing
- Digit extraction from scanned forms
- Document digitization
- Educational handwriting recognition

## Limitations

- The model is trained on small, centered grayscale images.
- Unusual handwriting styles may result in incorrect predictions.
- Photographs with complex backgrounds may require additional preprocessing.
- Confidence scores indicate the model's estimated probabilities and do not guarantee correctness.

## Future Enhancements

- Add handwritten digit image upload support.
- Deploy the application as a permanent web application.
- Compare CNN performance with a basic artificial neural network.
- Experiment with data augmentation and deeper CNN architectures.
- Extend the system to recognize letters or multi-digit numbers.

## Learning Outcomes

This project demonstrates practical implementation of the following deep learning concepts:

- Convolutional Neural Networks
- Activation functions: ReLU and softmax
- Pooling and feature extraction
- Feedforward neural networks
- Backpropagation and gradient-based optimization
- Multiclass classification
- Model evaluation and visualization
- Interactive deployment using Gradio

## Course Information

**Course:** CSM422 – Deep Learning  
**Project:** Handwritten Digit Recognition Using CNN  
**Environment:** Google Colab  
**Domain:** Deep Learning and Computer Vision

## Author

**Adithyan S Pillai**

Developed as an academic project to demonstrate the practical application of Convolutional Neural Networks for image classification.

## License

This project is intended for educational and academic purposes. You may add an MIT License if you want to publish and distribute the source code under that license.
