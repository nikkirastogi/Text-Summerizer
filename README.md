# Text Summarizer with LSTM Attention Mechanism

## Group 3 Members
- Alluri Ratna Anvesh
- Ashish Rogannagari
- Deepak Reddy Guda
- Nikki Rastogi

## Introduction
Text summarization generates concise summaries from lengthy text while retaining key information. Unlike extractive models like TextRank, abstractive summarization creates new sentences, offering more fluent and human-like summaries. Our project focuses on building an **Abstractive Text Summarizer** for the **Amazon Fine Foods Reviews** dataset using a **Long Short-Term Memory (LSTM)** model combined with an **Attention Mechanism**.

## Abstractive Summarization
Abstractive summarization focuses on the vital information of the original text and generates new sentences for the summary. This is in contrast to extractive summarization, which selects exact sentences from the original text.

## Problem Statement
Companies like Amazon receive millions of customer reviews daily, making manual analysis impractical. Identifying trends, sentiments, and insights from this vast amount of feedback is challenging. Our project aims to:
- Generate concise, human-like summaries of Amazon Fine Foods reviews using an LSTM model with an Attention Mechanism.
- Classify customer reviews as positive, neutral, or negative to enhance business understanding.

## Who Will Benefit?
- **Business Analysts**: Quickly identify trends and actionable insights from large volumes of customer feedback.
- **Product Managers**: Understand product performance and customer sentiment to guide product development.
- **Executives and Decision-Makers**: Leverage summarized insights and sentiment classifications to make strategic business decisions efficiently.

## Data Source
The dataset consists of reviews of fine foods from Amazon, spanning over 10 years, including ~500,000 reviews. The dataset was sourced from [Stanford's Snap Dataset](https://snap.stanford.edu/data/web-FineFoods.html) and converted into a CSV file for easier processing.

### Dataset Details
- **Number of reviews**: 568,454
- **Number of users**: 256,059
- **Number of products**: 74,258
- **Memory**: 377 MB

## Research Questions
1. Can we accurately classify customer reviews as positive, neutral, or negative?
2. Can we generate concise summaries of reviews using sequence models?
3. How does an LSTM with Attention Mechanism perform in terms of efficiency and accuracy?

## Why LSTM with Attention Mechanism?
- **Handles sequential data and long-term dependencies**: LSTMs are well-suited for text data.
- **Attention mechanism**: Ensures the model focuses on the most relevant parts of the input.
- **Resource-efficient**: Compared to transformer models like BART or PEGASUS, LSTMs are more suitable for moderate-scale applications.

## Approach
1. **Data Extraction**: Load the dataset from the provided GitHub link.
2. **Data Preparation**: Clean and preprocess the data, including handling contractions, tokenization, and removing unnecessary columns.
3. **Exploratory Data Analysis (EDA)**: Analyze the dataset to understand the distribution of review lengths, sentiment, and word frequencies.
4. **Data Preprocessing**: Prepare the data for model training by vectorizing text and splitting it into training and testing sets.
5. **Model Building**:
   - **Classification Models**: Naive Bayes and XGBoost for sentiment classification.
   - **Summarization Model**: LSTM with Attention Mechanism for abstractive text summarization.

## Model Performance
### Naive Bayes Model
- **Accuracy**: 89%
- **Precision**: 0.89 (weighted average)
- **Recall**: 0.89 (weighted average)
- **F1-Score**: 0.84 (weighted average)

### XGBoost Model
- **Accuracy**: 94%
- **Precision**: 0.94 (weighted average)
- **Recall**: 0.94 (weighted average)
- **F1-Score**: 0.93 (weighted average)

### LSTM with Attention Mechanism
- **Training Accuracy**: 83.08%
- **Validation Accuracy**: 80.87%
- **Loss**: 0.9202 (training), 1.4306 (validation)

## Challenges
- **Computational Power**: Due to the large dataset, we faced computational challenges while training the LSTM model. To address this, we sampled a subset of the data for training.

## Results
- **Sentiment Classification**: XGBoost outperformed Naive Bayes with higher accuracy and better class balance.
- **Text Summarization**: The LSTM with Attention Mechanism successfully generated concise summaries of long reviews with an accuracy of 84.3%.
