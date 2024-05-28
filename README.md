# Project README
# Building a Deep Learning Model for Contextual Advertising
# Predicting Health and Wellness News Articles

![Health and Wellness](readme_image.webp)


## Overview

This project aims to classify news articles as either "wellness" or "not wellness" using word embeddings from OpenAI and a RandomForest classifier. The workflow is consistent across all the provided notebooks and involves the following steps:

- Data Loading and Preprocessing
- Embedding Generation
- Model Training and Evaluation

## Detailed Workflow

### 1. Data Loading and Preprocessing

- **Data Source**: The data is loaded from a predefined source, typically in CSV format.
- **Data Cleaning**: The text data is cleaned and prepared for processing. This includes:
  - Lowercasing the text
  - Removing punctuation and special characters
  - Tokenization

### 2. Embedding Generation

- **Embedding Model**: OpenAI's embedding models (e.g., ADA embeddings, BERT, DistilBERT) are used to convert text data into numerical embeddings.
- **API Integration**: The OpenAI API is used to obtain embeddings for each text input. The function `get_embedding(client, text)` interacts with the API to retrieve these embeddings.
- **Batch Processing**: Text data is processed in batches to generate embeddings efficiently.

### 3. Model Training and Evaluation

- **Classifier**: A RandomForest classifier is used for the binary classification task.
- **Training**: The model is trained using the embeddings generated from the training dataset.
- **Evaluation**: The model's performance is evaluated using a test dataset. Metrics such as accuracy, precision, recall, and F1-score are calculated and displayed.
