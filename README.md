# Chatbot
A Chatbot or a Virtual Assistant for https://doj.gov.in/.

# Query Classification Model for Legal Documents

This repository contains a trained model designed to classify user queries related to legal documents and provide an appropriate numerical label. The label can be used to generate responses based on predefined queries in a database.

## Overview

The model is designed to match user prompts to the most relevant query in our database. It does not directly return answers but instead provides a numeric label representing the closest match. This label can then be used to generate a response to the user's query.

## Training Data

The model has been trained on a dataset compiled from the following sources:

1. [List of Supreme Court Judges](https://cdnbbsr.s3waas.gov.in/s35d6646aad9bcc0be55b2c82f69750387/uploads/2024/08/20240801417686651.pdf)
2. [List of Rajasthan High Court Judges](https://cdnbbsr.s3waas.gov.in/s35d6646aad9bcc0be55b2c82f69750387/uploads/2024/08/202408011995230619.pdf)
3. [Vacancies in Supreme Court](https://doj.gov.in/supreme-court-3/)
4. [Vacancies in High Court](https://cdnbbsr.s3waas.gov.in/s35d6646aad9bcc0be55b2c82f69750387/uploads/2024/08/20240801994943198.pdf)

The training dataset is organized as follows:

- **text_dataset**: Contains the initial queries in text format, separated into folders corresponding to each source document.
- **csv_dataset**: Contains the same queries in CSV format, labeled with a class number representing the query number.

## Model Performance

The current accuracy of the model is **13.64%**. This result was achieved on the first training attempt, and with further tweaking of the model’s hyperparameters, we anticipate improvements in accuracy.

### Confusion Matrix

Below is the confusion matrix generated after the model's evaluation:

![Confusion Matrix](path_to_confusion_matrix_image.png)

## Model Export

The trained model is saved in the `results` folder and can be integrated into a website or application. The model accepts user queries, classifies them, and returns a numeric label corresponding to the best-matching query.

## Future Improvements

- Fine-tuning the model with better hyperparameters.
- Expanding the training dataset for improved accuracy.
- Enhancing the model's ability to generalize to unseen queries.
