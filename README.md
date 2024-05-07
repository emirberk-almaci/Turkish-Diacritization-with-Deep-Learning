# Turkish Diacritization with Deep Learning

This project aims to diacritize Turkish text using deep learning techniques. Diacritization is the process of adding diacritical marks to text. In Turkish, these marks can change the meaning of words, so accurate diacritization is important for understanding the text correctly.

## Project Structure

- `main.ipynb`: The main notebook for the project. It contains all the code for data preprocessing, model training, and prediction.

- `train.csv`: Training data.
- `random_data.txt`: Additional training data.
- `test.csv`: Test data.
- `test_result.csv`: Result files.

## Diacritization Process

The diacritization process in this project involves the following steps:

1. **Data Preprocessing**: The input text is preprocessed to convert it into a format that can be fed into the model. This involves tokenizing the text into individual characters, mapping each character to a unique integer (character index), and padding the sequences to ensure they all have the same length.

2. **Model Training**: The preprocessed data is used to train a Recurrent Neural Network (RNN). The RNN takes a sequence of character indices as input and outputs a sequence of indices that represent the diacritized characters. The model is trained using the CrossEntropyLoss function, which measures the difference between the predicted output sequence and the actual output sequence. The model parameters are updated using the Adam optimizer.

3. **Prediction**: Once the model is trained, it can be used to diacritize new text. The new text is preprocessed in the same way as the training data, and then fed into the model. The model outputs a sequence of indices, which are then mapped back to characters to get the diacritized text.

## Model Details

The model used in this project is a Recurrent Neural Network (RNN) built with PyTorch. The RNN is particularly suited for sequence prediction problems. This model takes a sequence of characters as input and outputs a sequence of diacritized characters.

The RNN processes the input sequence one character at a time, maintaining an internal state that encodes information about the characters it has seen so far. The output at each time step is dependent on the previous outputs and the current input.

The model is trained using a loss function that measures the difference between the predicted output sequence and the actual output sequence. The model parameters are updated using the Adam optimizer.

## Getting Started

1. Clone the repository.
2. Install the requirements by running `pip install -r requirements.txt` in your terminal.
3. Open the `main.ipynb` notebook.
4. Run all cells to train the model and make predictions.

## Requirements

- Python 3
- Pandas
- Numpy
- PyTorch

## Authors

- Emirberk Almacı
- Furkan Öztürk
