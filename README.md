# HandwritingRecognition
This repository contains a convolutional recurrent neural network (CRNN) model designed to convert images of handwritten text into machine-readable text. It was built as part of a personal project to deepen my understanding of computer vision and sequence modeling techniques.

## Overview

### Problem Statement

In the digital age, converting handwritten documents into machine-readable text remains a significant challenge, particularly for automating tasks in education, healthcare, and data entry. Handwriting varies greatly between individuals, and this variability poses difficulties for accurate recognition by traditional methods. The goal of this project is to develop a system that efficiently converts images of handwritten text into digital text using computer vision techniques, enabling faster and more accurate data processing across different handwriting styles.

### Those Affected

Handwriting recognition has broad implications across multiple sectors. In education, it can automate grading or digitize handwritten notes. In healthcare, it enables the extraction of critical information from handwritten prescriptions or medical records. In logistics and data entry, it streamlines the processing of handwritten forms and labels. By automating the transcription of handwriting, organizations can significantly reduce manual effort, minimize errors, and improve data accessibility and efficiency.

### Proposed Data Science Solution

This project proposes a deep learning-based approach to recognizing handwritten text using a Convolutional Recurrent Neural Network (CRNN) with CTC (Connectionist Temporal Classification) loss. The solution involves preprocessing handwritten word images, training a model to map image features to character sequences, and decoding the output into readable text. The pipeline is designed to generalize across different handwriting styles, providing a scalable and accurate solution for digitizing handwritten content.



## Dataset

For this project, we will be working with the dataset available on Kaggle titled:  
[Handwriting Recognition Dataset](https://www.kaggle.com/datasets/landlord/handwriting-recognition)

This dataset contains over **400,000** handwritten names collected through charity projects. It is specifically designed to address the challenge of character recognition in handwritten text, where the wide variation in individual writing styles makes the task significantly more difficult than recognizing machine-printed characters.

The data is split into three sets:

| Set          | Samples |
|--------------|---------|
| Training     | 331,059 |
| Validation   | 41,382  |
| Test         | 41,382  |
| **Total**    | 413,823 |


## Project Organization

## Project Organization

This project is organized into several key stages, from exploring and cleaning the data to preparing it for training the handwriting recognition model.

### 1. Data Exploration


- **Distribution Insight**: Analyzed the frequency of unique labels and character lengths to assess label diversity and guide model design.
- **Initial Cleaning**: Removed entries with missing labels or ambiguous tags such as `"EMPTY"` and `"UNREADABLE"`, which were inconsistently used in the dataset.
- **Label Analysis**: Examined the length of each word (i.e., number of characters) to understand label complexity.



### 2. Data Preprocessing

- **Image Formatting**: Standardized all images to a fixed size and converted them to grayscale to ensure consistent input dimensions for the model.
- **Label Encoding**: Transformed each label (word) into a sequence of numerical indices, where each character corresponds to a unique integer. Padding was added for shorter sequences.
- **Dataset Construction**: Built the training and validation datasets by pairing processed image arrays with their encoded label sequences, including input and label length metadata needed for CTC loss during training.


### 3. Model building 

### 4. Evaluation 

## Findings & Conclusion