# Team30_Amazon_Review_Summarizer

## Overview
This project builds a pipeline to automate the collection, summarization, sentiment analysis, and classification of Amazon product reviews, helping users make informed purchase decisions quickly.

## Problem Statement
Manually reading hundreds of Amazon reviews is time-consuming and inefficient. This project aims to summarize reviews, extract sentiments and aspects, and classify product usefulness to improve user experience.

## Objectives

    Scrape Amazon reviews while bypassing login restrictions.

    Summarize reviews using NLP models.

    Perform sentiment and aspect-based analysis.

    Classify products based on review usefulness.

## Pipeline Stages

    Cookie Authentication
    Save login cookies using Selenium and undetected_chromedriver to maintain Amazon session across scraping runs.

    Review URL Collection
    Visit product pages, navigate to review sections, and extract review page URLs (only if review count ≥ 500).

    Data Collection
    Scrape individual reviews, ratings, and metadata (up to 500 per product) using Selenium. Store in CSV format.

    Review Summarization
    Summarize long review texts using the BART transformer model to create concise product-level summaries.

    Sentiment & Aspect Mining
    Analyze reviews using VADER and TextBlob to extract sentiment polarity and identify common product-related aspects.

    Classification
    Classify products as “Useful” or “Not Useful” using features like review summaries, ratings, and sentiment scores.

## Tools & Technologies

    Language: Python

    Scraping: Selenium, undetected_chromedriver, BeautifulSoup

    NLP: BART, TextBlob, VADER, NLTK

    Data Handling: Pandas, NumPy

    Modeling: Scikit-learn


## Results

    Reviews scraped: ~50 products × 500 reviews

    Summary accuracy: High-quality summaries using BART

    Sentiment analysis: Positive, neutral, and negative trends extracted

    Classification: Products labeled as Useful/Not Useful with reasonable accuracy
