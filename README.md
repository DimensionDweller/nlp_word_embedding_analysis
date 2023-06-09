# NLP Word Embedding Analysis

This project uses Word2Vec embeddings and t-SNE to perform comparative analysis of news articles from different sources.

## Overview

The data used in this project was fetched and cleaned in a previous project. You can find the details about that process [here](https://github.com/DimensionDweller/news_sentiment_analysis_viz).

The main focus of this project is to train Word2Vec models on text data from various news sources, and use these models to analyze and visualize the semantic relationships between words.

## About Word Embeddings

Word embeddings are a type of word representation that allows words with similar meaning to have a similar representation. They are a distributed representation for text that is perhaps one of the key breakthroughs for the impressive performance of deep learning methods on challenging natural language processing problems.

Word2Vec is a popular algorithm used for generating dense vector representations of words in large corpora using unsupervised learning. The resulting vectors have been found to exhibit interesting semantic properties, such as clustering of similar words and the ability to answer analogy questions, e.g., "man is to woman as king is to queen".

## Project Structure

Here's a brief overview of the Python scripts in this project:

1. `train_embedding.py`: This script contains functions to load and preprocess the data, and train Word2Vec models.

2. `reduce_n_plot.py`: This script contains functions to reduce the dimensionality of the word embeddings using t-SNE, and visualize them using matplotlib and Plotly.

3. `main.py`: This is the main script that ties everything together. It loads and preprocesses the data, trains the Word2Vec models, loads the models, retrieves and plots similar words and word analogies.

## Getting Started

1. Clone the repository: `git clone https://github.com/yourusername/nlp_word_embedding_analysis.git`

2. Install the requirements: `pip install -r requirements.txt`

3. Run the main script: `python main.py`


## Output

The output of the project is primarily visual in the form of plots, which represent the relationships between words in a two-dimensional space. These plots are created using the word embeddings generated by the Word2Vec models trained on the news articles.

1. **Similar Words Plot:** The first plot shows the similar words to a given input word. For each news source, the Word2Vec model is used to find the top N most similar words to the input word. These words, along with their embeddings, are then plotted in a 2D space. The similarity of words in this context is based on the context in which they appear in the articles.

    This plot is useful for comparing how different news sources use language and frame discussions. For example, if the input word is 'economy', the similar words plot might show that one news source often discusses the economy in relation to 'growth' and 'investment', while another often discusses it in relation to 'unemployment' and 'debt'.

2. **Word Analogy Plot:** The second plot shows a word analogy in a 2D space. Given three words, A, B, and C, the Word2Vec model is used to find the word D such that the analogy "A is to B as C is to D" holds true. For example, if the words A, B, and C are 'king', 'man', and 'queen' respectively, the word D would likely be 'woman'.

    This plot is useful for visualizing the semantic relationships between words as understood by the Word2Vec model. It's a fun and intuitive way to see how the model has learned to represent the meaning of words based on their usage in the articles.

## Interpretation

The interpretation of these plots depends on the specific words and news sources being analyzed. It's important to remember that the Word2Vec models are not perfect and their understanding of language is purely statistical and based on the specific corpus of text they were trained on.

In general, these plots can provide interesting insights into the language used by different news sources and how they frame discussions on various topics. They can also serve as a starting point for further analysis or research.

## Further Work

This is just the beginning of what can be done with word embeddings and NLP. Potential extensions of this project could involve comparing more news sources, experimenting with different word embedding algorithms, or using the word embeddings as input to a machine learning model to perform tasks such as text classification or sentiment analysis.
