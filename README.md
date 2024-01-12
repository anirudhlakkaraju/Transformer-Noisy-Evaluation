
# Robustness of State-of-the-Art Transformer Models to Noisy Data

This is the final project of the graduate level course **COMPSCI 685 - Advanced Natural Language Processing** (Spring 2023) at University of Massachusetts Amherst. 

For more information about the course, visit the [course homepage](https://people.cs.umass.edu/~miyyer/cs685/).


## Table of Contents

- [Abstract](#abstract)
- [Approach](#approach)
- [Adding Noise](#adding-noise)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Results](#results)

## Abstract

In recent years, there has been significant progress in the development of powerful language models based on deep learning techniques such as transformers. This study investigates the performance of state-of-the-art NLP models (BERT, ELECTRA, T5, and XLNet) when dealing with intentionally corrupted datasets, simulating real-world scenarios. The evaluation focuses on the models' ability to generalize and provide reliable results in the context of Question Answering (QA) and Sentiment Analysis (SA), essential tasks in many applications. The findings aim to have practical implications for industries relying on NLP models for customer feedback analysis, social media monitoring, and chatbots.

## Approach

Real-world data often contains inherent imperfections and noise, challenging machine learning models to achieve optimal performance. This research assesses the performance of diverse models subjected to incremental levels of added noise. The primary objective is to evaluate the robustness of these models and conduct a comparative analysis between different models and downstream tasks. This empirical investigation aims to shed light on the efficacy of models under varying noise conditions and provide insights into their adaptability for real-world applications. The research process is divided into four main sections: Data Setup, Adding Noise, Fine-tuning, and Testing.

## Adding Noise

To enhance the Sentiment Analysis (SA) and Question Answering (QA) tasks, we employed a variety of noise functions sourced from the NLP Aug library. These noise functions encompass both character-level and word-level perturbations, reflecting real-world scenarios. Specifically, the character-level noises include KeyBoardAug, OCRAug, RandomAug(Char), SplitAug, SpellingAug, and RandomAug(word).

## Project Structure

- `notebooks/`: Contains all Jupyter notebooks, including the code for data setup, model training, and evaluation.
- `report/`: Contains the detailed project report in PDF format.


## Results

In Sentiment Analysis, top-performing models BERT10% and ELECTRA10% achieved high F1 scores of 0.9112 and 0.9122 on clean datasets, maintaining robust performance (F1 scores of 0.8672 and 0.8675) on noisy datasets. 

For Question Answering, BERTclean and ELECTRA15% excelled with F1 scores of 0.6844 and 0.79 on clean data, maintaining resilience with scores of 0.6991 and 0.7738 in noisy conditions. 

For detailed comparisons and findings about all model performances, please refer to the full report in `report/` directory.

## Usage

The study can be replicated using the respective Jupyter notebooks within `notebooks/` directory. 
