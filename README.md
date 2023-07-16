# Sentiment Analysis of Rotten Tomatoes Reviews
Rotten Tomatoes is a popular website for rating and reviewing movies and TV shows.
The goal of this project is to train a model that is able to classify the reviews into 5 different sentiment categories
(negative, somewhat negative, neutral, somewhat positive, positive) using sentiment analysis.

## Table of Contents:
1. Overview
2. Problem Statement
3. Metrics
4. Methodology
5. Implementation
6. Usage

## Overview
Rotten Tomatoes is a well-known website for rating and reviewing movies and TV shows,
and many people rely on it to pick a movie for the night. Sentiment Analysis is the process of analyzing a text
or response to determine if the text is negative or positive and to understand the emotions of whoever wrote the text.

## Problem Statement
The goal is to train a model that is able to classify the review into 5 different categories
(negative, somewhat negative, neutral, somewhat positive, positive).

## Metrics
There are many metrics to consider for a classification problem, such as:
accuracy, precision, recall, f1-score, etc. But the Rotten Tomatoes data have imbalanced classes,
so the F1-score is a good option to calculate for each class,
then the weighted average of the f1-scores can be used to get a final metric to track.

## Methodology
Data preprocessing was done to normalize the phrases, tokenize them, lemmatize the words,
get rid of stop words, and convert the phrases into a matrix of token counts.
TF-IDF was applied to the matrix to help understand how relevant a certain word is to the document
using the frequency of the word in all of the data.

The modeling step used Scikit-learn Pipelines to create a pipeline of three steps: Count Vectorizer,
TF-IDF Transformer, and model fitting. Two algorithms were experimented with: XGB Classifier and Random Forest Classifier.
A class weight was used to give a weight to each class based on the amount of data for that class to solve the imbalanced data problem.

## Implementation
After the preprocessing step, now we arrive at the modeling step.
I used Scikit-learn Pipelines to create a pipeline of three steps: Count Vectorizer, TF-IDF Transformer,
and model fitting. For the algorithms, I experimented with 2 algorithms: XGB Classifier and Random Forest Classifier.

## Usage
You only need to run the notebook, no other thing is required
