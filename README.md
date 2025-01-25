# RecurrentNeuralNetwork

###### Recurrent Neural Networks (RNN) for IMDB Review Classification

This project explores the use of Recurrent Neural Networks (RNNs) to classify reviews from the IMDB dataset as either positive or negative. Various RNN architectures, including Simple RNN, LSTM, GRU, and Bidirectional RNN, are implemented and evaluated. The results of each model are compared to draw meaningful conclusions.

## Project Overview

The project uses the Keras library to:
- Load and preprocess the IMDB dataset.
- Build and train multiple RNN-based models.
- Visualize training and validation metrics.
- Evaluate model performance on test data.
- Compare different RNN architectures.

## Features

- **Dataset:** IMDB dataset with preprocessed reviews limited to the top 10,000 most frequent words.
- **Models Implemented:**
  - Simple RNN
  - Long Short-Term Memory (LSTM)
  - Gated Recurrent Unit (GRU)
  - Bidirectional RNN (BRNN) with stacked LSTM layers
- **Metrics:**
  - Accuracy
  - Loss
- **Visualization:**
  - Training and validation loss over epochs.
  - Training and validation accuracy over epochs.

---

## Conda (Setup and Environment)

To make the project reproducible and ensure smooth package management, this project uses Conda as a package and environment manager. Below are the steps to set up the environment:


1. **Install Conda**:
If you haven't installed Conda yet, you can download it from the official [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) websites. Anaconda is a larger distribution with more pre-installed packages, while Miniconda is a smaller, minimal version. Choose whichever suits your needs.

2. **Create a new environment:** Open your terminal and run the following command to create a new Conda environment with Python 3.7:

    ```bash
    conda create --name new_conda_env python=3.7
    ```

3. **Activate the environment:** Once the environment is created, activate it by running:

    ```bash
    conda activate new_conda_env
    ```

4. **Install required packages (Jupyter, NumPy, MatPlotLib,Tensorflow and Keras)**

    ```bash
    conda install jupyter numpy matplotlib tensorflow keras
    ```

5. **Run Jupyter Notebook**

    ```bash
    jupyter notebook
    ```
---

## Code Structure

1. **Hyperparameter Setup:**
   - Vocabulary size: 10,000
   - Review length (padded): 500
2. **Dataset Loading and Preprocessing:**
   - Load IMDB dataset from Keras.
   - Pad sequences to ensure consistent input length.
3. **Model Architectures:**
   - **Simple RNN:** Uses `SimpleRNN` layer for sequential data processing.
   - **LSTM:** Utilizes `LSTM` for handling long-term dependencies.
   - **GRU:** Implements `GRU` for an efficient alternative to LSTM.
   - **Bidirectional RNN:** Stacks `Bidirectional LSTM` layers for better context understanding.
4. **Training and Evaluation:**
   - Models trained for 6 epochs with a batch size of 128.
   - Evaluation includes accuracy and loss on the test dataset.
5. **Visualization:**
   - Loss and accuracy plotted for training and validation phases.

## Example Results

### Simple RNN
- **Validation Accuracy:** ~85.5%
- **Test Accuracy:** ~85.0%

### LSTM
- **Validation Accuracy:** ~87.7%
- **Test Accuracy:** ~86.1%

### GRU
- **Validation Accuracy:** ~87.4%
- **Test Accuracy:** ~86.0%

### Bidirectional RNN
- **Validation Accuracy:** ~88.0%
- **Test Accuracy:** ~87.6%


## Conclusion

This project demonstrates the potential of RNN-based models for text classification tasks. Each architecture brings unique strengths, with Bidirectional RNNs generally providing the best results for this task.

## Future Work

- Extend experiments with different embedding dimensions and RNN units.
- Experiment with additional preprocessing techniques (e.g., lemmatization, stopword removal).
- Compare RNN performance with transformer-based models (e.g., BERT).