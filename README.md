# Project Title: Quizbowl Question Type Classifier using Deep Averaging Network (DAN) 🤖📚

## Overview 🌐

This project implements a Deep Averaging Network (DAN) for classifying quizbowl questions into categories such as Literature, History, and Science. The model is built using PyTorch, a popular deep learning library, and utilizes word embeddings for enhanced performance. The dataset consists of quizbowl bonus questions, and the goal is to predict the category of each question.

## Table of Contents 📜

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Implementation](#implementation)
   - [Data Loading and Preprocessing](#data-loading-and-preprocessing)
   - [Model Architecture](#model-architecture)
   - [Training](#training)
   - [Evaluation](#evaluation)
4. [Results](#results)
5. [Usage](#usage)
6. [Future Improvements](#future-improvements)
7. [Contributing](#contributing)
8. [License](#license)

## Introduction 🚀

This project aims to showcase the implementation of a deep learning model, specifically a Deep Averaging Network, for classifying quizbowl questions. The model takes advantage of PyTorch's capabilities for efficient training and evaluation. The project also explores the impact of different word embeddings, such as Word2Vec or GloVe, on the model's performance.

## Dataset 📊

The dataset used in this project is sampled from quizbowl bonus questions. Each example includes the tokenized question text and the corresponding label (0 for Literature, 1 for History, and 2 for Science). The dataset is split into training, development (dev), and test sets.

## Implementation 💻

### Data Loading and Preprocessing 📝

The data loading and preprocessing steps involve tokenizing the question text and creating a vocabulary. The provided functions `load_data` and `load_words` handle loading the dataset and building the vocabulary.

### Model Architecture 🏗️

The DAN model consists of an embedding layer, a hidden linear layer, and an output linear layer. The architecture is designed to efficiently process variable-length input sequences. The model is implemented in the `DanModel` class using PyTorch's `nn.Module`.

### Training 🚂

The training process involves iterating through the training data, computing the loss, and updating the model parameters. The Adamax optimizer and cross-entropy loss are used for training. Gradient clipping is applied to prevent exploding gradients.

### Evaluation 📈

The evaluation function calculates the accuracy of the model on the development and test sets. The trained model is loaded for evaluation, and the accuracy is reported.

## Results 📊

The model achieves a high accuracy, easily surpassing 0.8 for category prediction. The performance on answer prediction is also discussed in the analysis report.

### Analysis Report 📑

The analysis report discusses the model's accuracy on the test set, strategies employed for answer prediction, and provides examples of incorrectly predicted instances in the dev set. Additionally, the impact of different word representations (Word2Vec, GloVe) on the model's performance is explored.

## Usage 🚀

To run the code, follow these steps:

1. Install the required dependencies:

   ```bash
   pip install torch numpy nltk gensim

2. Run the provided Python script:
   ```bash
   python dan_classifier.py

3. Adjust the script's arguments for file paths, batch size, number of epochs, etc., as needed.
 
## Future Improvements 🚧

- Experiment with different hyperparameters to further optimize the model.
- Explore additional word embeddings and their impact on performance.
- Conduct error analysis to understand and address misclassifications.

## Contributing 🤝

Contributions are welcome! If you have ideas for improvements or find issues, feel free to open a GitHub issue or submit a pull request.

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
