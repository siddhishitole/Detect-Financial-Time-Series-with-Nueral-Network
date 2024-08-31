# Neural-Net-with-Financial-Time-Series-Data

**Neural-Net-with-Financial-Time-Series-Data** is an open-source software project designed to predict the daily log return of any financial asset using a Long Short-Term Memory (LSTM) neural network. The project incorporates several technical indicators and a parsimonious rule-based model for sentiment analysis from the New York Times to improve prediction accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technical Indicators](#technical-indicators)
- [Sentiment Analysis Model](#sentiment-analysis-model)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project leverages advanced deep learning techniques to predict the daily log returns of financial assets. It integrates various technical indicators (e.g., Stochastics, Moving Average Convergence/Divergence oscillator) and a rule-based sentiment analysis model derived from the New York Times data. The neural network is trained using a robust optimizer, **Stochastic Gradient Descent with Warm Restarts (SGDR)** and **Cosine Annealing**, to enhance convergence and model performance.

## Features

- Predicts daily log returns of financial assets using an LSTM neural network.
- Implements technical indicators like **Stochastics** and **Moving Average Convergence/Divergence (MACD) Oscillator**.
- Includes a parsimonious rule-based sentiment analysis model for text data from the New York Times.
- Uses **SGDR (Stochastic Gradient Descent with Warm Restarts)** and **Cosine Annealing** for optimizing the LSTM model.
- Supports deployment with **NVIDIA CuDNN** computation without the need to rewrite code.
- Highly customizable and scalable for different financial time series data.

## Technical Indicators

The following technical indicators are used to enrich the feature set for training the LSTM model:

- **Stochastics**: Used to determine overbought or oversold conditions in the market.
- **Moving Average Convergence/Divergence (MACD) Oscillator**: Helps in identifying momentum changes and trend reversals.
- **Relative Strength Index (RSI)**: Indicates overbought or oversold conditions based on price movements.
- **Bollinger Bands**: Provides a relative definition of high and low that can be used to compare price actions.
- **Exponential Moving Average (EMA)**: A type of moving average that gives more weight to recent prices.

## Sentiment Analysis Model

The sentiment analysis component utilizes New York Times data to extract sentiment scores based on a rule-based model. This sentiment score is then used as an additional feature to improve the predictive capability of the neural network.

- **Data Source**: New York Times articles.
- **Methodology**: Rule-based approach that classifies sentiments as positive, negative, or neutral.
- **Output**: Sentiment scores are integrated into the financial data for enhanced predictions.

## Installation

To run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Neural-Net-with-Financial-Time-Series-Data.git
