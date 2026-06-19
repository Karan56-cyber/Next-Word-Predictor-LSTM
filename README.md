# Next-Word-Predictor-LSTM
LSTM-based Next Word Prediction model built using TensorFlow and Keras. The model learns word sequences from text data and predicts the most probable next word based on the input context.

## Problem Formulation

The original dataset consists of raw text without labels.

To train the model, the text is converted into input-output pairs:

Input: NLP
Output: can

Input: NLP can
Output: speed

Input: NLP can speed
Output: the

Input: NLP can speed the
Output: mining

This transforms the Next Word Prediction task into a supervised multi-class classification problem, where the model learns to predict the next word from the vocabulary based on the input sequence.

The target words are one-hot encoded and the model is trained using:
- Softmax activation
- Categorical Cross-Entropy Loss
- Adam Optimizer
## Dataset

- Source: IBM Think articles, NLP articles, machine learning educational content, and reference text
- Dataset Type: Raw Text Corpus
- Total Training Sequences: 12,636
- Vocabulary Size: 3,184 Words
- Maximum Sequence Length: 201 Tokens

## Model Architecture

- Embedding Layer (100 Dimensions)
- LSTM Layer (150 Units)
- Dense Output Layer (Softmax)

  
## Key Concepts Learned

- Text Tokenization
- Sequence Generation
- Word Embeddings
- Sequence Padding
- LSTM Networks
- Multi-Class Classification
- Next Word Prediction
- Supervised Learning from Text Data

## Results
<img width="1385" height="599" alt="Screenshot 2026-06-19 at 7 47 10 PM" src="https://github.com/user-attachments/assets/d8b21596-f2ce-4523-84d4-d95e3b45ed9e" />

Training Accuracy: ~97%

Example Prediction:

```text
Input: NLP

Generated:
NLP can speed the mining ...
```

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
