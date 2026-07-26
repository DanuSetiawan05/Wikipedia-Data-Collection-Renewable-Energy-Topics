# Wikipedia Data Collection - Renewable Energy Topics

A Python tool that collects Indonesian-language Wikipedia articles about renewable energy ("Energi Terbarukan"), saves them into a structured CSV file, and performs basic text analysis (word count per article and most frequent words) as preparation data for a further NLP project.

> This project was completed as a coursework assignment for NLP in semester 7, developed as an individual project.

## Tech Stack

- Python
- wikipedia / wikipedia-api - Wikipedia content retrieval
- csv (standard library) - structured data export
- re, collections.Counter - text analysis

## Getting Started

### Prerequisites
- Python 3.x

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/DanuSetiawan05/Wikipedia-Data-Collection-Renewable-Energy-Topics.git
cd Wikipedia-Data-Collection-Renewable-Energy-Topics

# 2. Install dependencies
pip install wikipedia wikipedia-api

# 3. Run the notebook
jupyter notebook wikipedia_renewable_energy_collector.ipynb
```

## What It Does

1. Searches Wikipedia (Indonesian language) for articles related to "Energi Terbarukan", handling disambiguation pages and missing pages gracefully
2. Saves the collected articles (title, URL, full content, summary) into a semicolon-delimited CSV file
3. Reads the exported CSV back to verify integrity, then counts the number of words per article
4. Identifies the 10 most frequently occurring words across all articles (after removing Indonesian stopwords)

## Dataset

The dataset consists of 10 Indonesian Wikipedia articles related to renewable energy, including the main "Energi terbarukan" article and related topics (non-renewable energy, specific energy sources, etc.). Wikipedia content is licensed under CC BY-SA, so collecting and reusing this data (with attribution to Wikipedia) is permitted.

## Project Structure

```
wikipedia_renewable_energy_collector.ipynb   - Main analysis notebook
artikel_energi_terbarukan.csv                - Collected dataset
```

## Next Steps for NLP Analysis

1. Text preprocessing - cleaning, tokenization, stopword removal
2. Keyword extraction / TF-IDF analysis
3. Topic modeling (LDA or BERTopic) to identify subtopics
4. Word cloud visualization
5. Text summarization or classification experiments

## Author

Muhammad Danu Setiawan

## License

This project is open source and available for learning purposes. The collected Wikipedia content remains licensed under CC BY-SA; please attribute Wikipedia when reusing the dataset.
