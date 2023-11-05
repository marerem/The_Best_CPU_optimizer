# The Best CPU optimizer


This readme provides an overview of the performance of various optimizers when training a simple neural network model on the FashionMNIST dataset for 10 epochs using only CPU resources. The model consists of two fully connected layers, and we evaluate different optimizers with two different initial learning rates, discarding those with an initial accuracy below 82% and an average accuracy below 86.7% over the 10 epochs. The optimizers that meet these criteria are then presented for you to choose based on your specific needs.

## Dataset and Model

- **Dataset:** We use the FashionMNIST dataset, which consists of 28x28 grayscale images of 10 different fashion items. It's commonly used for image classification tasks.

- **Model:** The neural network model used for training is a simple architecture with two fully connected layers.

## Optimizers

We evaluate the following optimizers with two initial learning rates (0.01 and 0.001):

1. **SGD (Stochastic Gradient Descent):**
   - SGD with default parameters
   - SGD with weight decay (L2 regularization) of 0.1
   - SGD with momentum (0.9)
   - SGD with Nesterov momentum (0.9)
2. **ASGD (Averaged Stochastic Gradient Descent)**
3. **Adagrad**
4. **Rprop (Resilient Backpropagation)**
5. **RAdam (Rectified Adam)**
6. **Adadelta**
7. **RMSprop**
   - RMSprop with a smoothing parameter (alpha) of 0.9
   - RMSprop with default parameters
8. **Adam**
   - Adam with default parameters
   - Adam with AMSGrad enabled
9. **AdamW (Adam with Weight Decay)**
10. **Adamax**
11. **NAdam (Nesterov-accelerated Adaptive Moment Estimation)**

## Selection Criteria

We have applied two filtering criteria to select the best-performing optimizers:

1. **Initial Accuracy:** We discarded optimizers that did not achieve an accuracy of at least 82% after the first epoch.

2. **Mean Accuracy:** We discarded optimizers that did not achieve a mean accuracy of at least 86.7% over the 10 epochs.

## Results

After applying the selection criteria, the remaining optimizers are presented in the results table. You can choose the best optimizer based on your specific needs:
<img width="1192" alt="Screenshot 2023-11-05 at 19 20 49" src="https://github.com/marerem/The_Best_CPU_optimizer/assets/101661237/c09468da-18d4-4456-8131-242b503f5aac">

Please select an optimizer based on your preference, whether it's the highest mean accuracy, faster training times, or other specific requirements. Experimenting with different optimizers and learning rates is encouraged to find the best fit for your particular use case.
