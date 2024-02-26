# Deep-Learning-high-frequency-price-changes

## Overview

This project leverages deep learning to predict high-frequency price changes of two US stocks. Utilizing a dataset devoid of temporal dependencies allows for the application of simpler models such as Feedforward Neural Networks (FNNs), enhancing the training process and statistical analysis efficiency.

## Data Preparation

### Dataset

- **Data A**: A 200,000×22 matrix, with the first column indicating midprice direction changes and the remaining columns representing features.
- **Data B (No Labels)**: A 20,000×21 matrix used for validation, following the same structure as Data A but without labels.

### Preprocessing

- **Standardization**: Applied to normalize feature values to zero mean and unit variance, facilitating faster convergence and improved model performance.
- **Validation Split**: Used to evaluate model generalization and tune hyperparameters.

## Model Architecture

- **Output Layer**: Utilizes the sigmoid activation function, suitable for binary classification tasks.
- **Hidden Layers**: Employs ReLU (Rectified Linear Unit) to introduce non-linearity and avoid the saturation problem, despite potential issues with "Dead ReLU" syndrome.
- **Architecture Comparison**: Explores both two-layer and three-layer networks to balance complexity, efficiency, and risk of overfitting.

## Optimization and Training

- **Optimizer**: Adam, chosen for its adaptive learning rate capabilities, proving effective for large datasets.
- **Learning Rate**: Fine-tuned to 0.001 after evaluating loss over training epochs to balance learning speed and model stability.
- **Batch Size**: Set to 500, balancing efficiency with generalization.
- **Epochs**: Limited to 5 to prevent underfitting or overfitting while maintaining computational efficiency.

## Conclusion

The project demonstrates that a Feedforward Neural Network, with carefully selected hyperparameters and preprocessing techniques, can effectively predict stock price direction changes with an accuracy range of 73% to 75%.

## References

- Bengio, Y. (2012). "Practical recommendations for gradient-based training of deep architectures."
