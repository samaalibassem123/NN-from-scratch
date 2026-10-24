# 🧠 Neural Network From Scratch Using NumPy

A simple implementation of a **neural network built from scratch using NumPy** and trained on the MNIST dataset to recognize handwritten digits from 0 to 9.

The goal of this project is to understand the mathematical foundations of neural networks by implementing forward propagation, backpropagation, gradient descent, and the learning process without using deep learning frameworks such as TensorFlow or PyTorch.

## 🚀 Project Overview

This project implements a fully connected neural network that learns to classify handwritten digits using the MNIST dataset.

The network learns by making predictions, calculating the loss, computing gradients through backpropagation, and updating its weights and biases using gradient descent.

### Architecture

```text
Input Layer          Hidden Layer          Output Layer
  784 neurons   →    10 neurons       →    10 neurons
  (28 × 28)          (ReLU)                 (Softmax)
```

- **Input layer:** 784 features representing the pixels of a 28 × 28 grayscale image.
- **Hidden layer:** 10 neurons with ReLU activation.
- **Output layer:** 10 neurons representing the probabilities of digits 0–9 using Softmax.

## ✨ Features

- Forward propagation
- ReLU activation function
- Softmax activation function
- Cross-entropy loss
- Backpropagation using the chain rule
- Gradient descent optimization
- Weight and bias updates
- Training and evaluation on MNIST
- Prediction and accuracy evaluation

## 🛠️ Technologies

- **Python**
- **NumPy** — matrix operations and numerical computation
- **Matplotlib** — training visualization
- **MNIST** — handwritten digit classification dataset
- **Jupyter Notebook** — experimentation and development

## 📦 Installation

Clone the repository:

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install numpy matplotlib jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook containing the neural network implementation and run the cells.

## 📊 Dataset: MNIST

The MNIST dataset contains 70,000 grayscale images of handwritten digits:

- **60,000 training images**
- **10,000 test images**
- **Image dimensions:** 28 × 28 pixels
- **Classes:** 10 digits, from 0 to 9

Each image is flattened into a vector of 784 features before being passed to the neural network.

The pixel values are normalized to improve training stability.

## ⚙️ How It Works

### 1. Forward Propagation

The input data passes through the network to produce predictions.

For the hidden layer:

\[
Z^{[1]} = XW^{[1]} + b^{[1]}
\]

\[
A^{[1]} = \operatorname{ReLU}(Z^{[1]})
\]

For the output layer:

\[
Z^{[2]} = A^{[1]}W^{[2]} + b^{[2]}
\]

\[
A^{[2]} = \operatorname{Softmax}(Z^{[2]})
\]

### 2. Loss Calculation

Cross-entropy loss measures the difference between the predicted probabilities and the true labels.

\[
\mathcal{L} =
-\frac{1}{m}\sum_{i=1}^{m}
\sum_{j=1}^{10}
Y_{ij}\log(A^{[2]}_{ij})
\]

Where \(m\) is the number of training examples.

### 3. Backpropagation

Using the chain rule, gradients are calculated for each weight and bias to determine how they contribute to the loss.

### 4. Gradient Descent

The network updates its parameters to reduce the loss:

\[
W \leftarrow W-\alpha\frac{\partial\mathcal{L}}{\partial W}
\]

\[
b \leftarrow b-\alpha\frac{\partial\mathcal{L}}{\partial b}
\]

Where \(\alpha\) is the learning rate.

These steps are repeated over multiple training iterations until the network learns useful patterns from the data.

## 📈 Results

The model is evaluated on the MNIST test dataset using classification accuracy and training loss.

| Metric | Result |
|---|---|
| Training dataset | 60,000 images |
| Test dataset | 10,000 images |
| Hidden neurons | 10 |
| Output classes | 10 |
| Test accuracy | Add your measured result |
| Final training loss | Add your measured result |

*Replace the placeholders with the actual results from your training run.*

## 🎯 Learning Objectives

Through this project, I explored:

- How neural networks process input data.
- How activation functions introduce non-linearity.
- How loss functions measure prediction errors.
- How backpropagation applies the chain rule.
- How gradients update model parameters.
- How a neural network learns to classify real image data.

## 🔮 Future Improvements

- Experiment with different hidden-layer sizes.
- Compare different learning rates.
- Add more hidden layers.
- Implement mini-batch training.
- Improve numerical stability and training speed.
- Compare the NumPy implementation against a PyTorch model.

## 👨‍💻 Author

**Bassem Samaali**

- LinkedIn: [linkedin.com/in/bassem-samaali](https://www.linkedin.com/in/bassem-samaali/)
- Portfolio: [bs-portfolio-liard.vercel.app](https://bs-portfolio-liard.vercel.app/)

---

*Built to understand the mathematics behind neural networks, one operation at a time.*
