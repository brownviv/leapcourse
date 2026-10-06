# MNIST CNN Classification and Error Analysis

## Project

This project uses a convolutional neural network (CNN) to classify handwritten digits from the MNIST data set.

The main question is not only how accurate the model is, but also which digits it confuses most often and whether one small change to the network changes those mistakes.

## Data

MNIST contains 70,000 grayscale images of handwritten digits from 0 to 9. Each image is 28 × 28 pixels.

The pixel values were scaled to the range 0–1. The data were then split into training and test sets.

## Model 1

The first CNN contains:

- one convolutional layer with 32 filters
- max pooling
- dropout
- a dense hidden layer
- a softmax output layer with 10 classes

The model uses the Adam optimiser and sparse categorical cross-entropy loss. Early stopping is used during training.

## Error analysis

After training, the model is evaluated on the test set. A confusion matrix is used to see which digit pairs are confused most often.

The notebook prints the two largest off-diagonal errors so they can be compared directly.

## Model 2

For the second model I made one controlled change: I added a second convolutional layer with 64 filters followed by max pooling.

Everything else was kept the same so the comparison would be fair.

## Evaluation

The two models are compared using:

- test accuracy
- confusion matrices
- the before-and-after counts for the two main errors from Model 1

The exact results are shown in the executed notebook.

## Reflection

The confusion matrix was useful because overall accuracy does not show what kinds of mistakes the model makes. A possible next step would be to test the models on handwriting that is different from the MNIST training data and check whether performance stays consistent.
