# Handwritten Digit Classification Using Singular Value Decomposition (SVD)

This repository contains an implementation of a classification algorithm for handwritten digits using Singular Value Decomposition (SVD). By decomposing digit images into their principal components, we create a robust classification method that balances efficiency and accuracy. 

## Project Overview

The project is divided into three main phases:

### 1. **Training Phase**
   - **Data Preparation**: Organize the training dataset of handwritten digits (e.g., MNIST) into class-specific matrices, where each matrix contains images corresponding to a single digit.
   - **SVD Decomposition**: Apply SVD to each class matrix, obtaining singular vectors and singular values. These vectors represent the key structural features of the digits in that class.
   - **Basis Selection**: Choose the top singular vectors (from 5 to 20) for each digit class to serve as basis vectors. These basis vectors will be used in the classification phase.

### 2. **Classification Phase**
   - **Representation and Residual Calculation**: For each test image, represent it as a linear combination of the basis vectors from each class and calculate the residual vector for each class.
   - **Class Assignment**: The test digit is assigned to the class whose basis vectors yield the smallest relative residual, indicating the best match between the test digit and the class.

### 3. **Performance Tuning and Analysis**
   - **Accuracy Optimization**: Test the accuracy of the algorithm with different numbers of basis vectors (e.g., 5 to 20) and identify the optimal number that maximizes accuracy while minimizing computational cost.
   - **Class Difficulty Assessment**: Analyze misclassified digits and identify which digits are difficult to classify, potentially due to poor handwriting or ambiguity.
   - **Singular Value Examination**: Analyze the decay rate of singular values for each digit class to determine if using different numbers of basis vectors for different classes could improve accuracy and efficiency.

## Algorithm Steps

1. **Training**: 
   - Organize the digit images into class-specific matrices.
   - Perform SVD on each class matrix to get singular vectors and values.
   - Select the top singular vectors as basis vectors for each class.

2. **Classification**:
   - For each test digit, represent it using the basis vectors of each class.
   - Calculate the residual error for each class.
   - Assign the digit to the class with the smallest residual.

3. **Optimization**:
   - Adjust the number of basis vectors and compare accuracy.
   - Analyze misclassifications and singular value decay rates to refine the algorithm.

## Dataset

You can use any standard dataset of handwritten digits, such as MNIST, for this project.

- [MNIST Dataset](http://yann.lecun.com/exdb/mnist/)

The training set should be divided into class-specific matrices, where each matrix contains images of a single digit (e.g., all images of the digit '0' form one matrix, and so on).




