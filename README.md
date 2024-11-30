# News Article Categorization using Naive Bayes

This project is designed to scrape and categorize news articles from an online newspaper into four categories: **sports**, **politics**, **business**, and **science/technology**. It utilizes the `newspaper3k` library for web scraping and a Naive Bayes classifier for text classification.

---

## Features

1. **Web Scraping**: Collects news articles from the specified website (`bdnews24.com`) across multiple categories.
2. **Data Cleaning**: Removes duplicates, stopwords, and punctuation for better text processing.
3. **Category Merging**: Merges subcategories into broader categories for simplified classification.
4. **Text Classification**: Uses a Naive Bayes classifier to predict the category of each article.
5. **Model Evaluation**: Provides accuracy and classification reports for model performance.

---

## Tools and Libraries

- **Web Scraping**: `newspaper3k`, `BeautifulSoup`
- **Text Processing**: `nltk`
- **Machine Learning**: `scikit-learn`
- **Data Handling**: `pandas`, `numpy`
- **Visualization**: Classification reports

---

## Workflow

1. **Data Collection**:
   - Scrapes articles from `bdnews24.com` across categories: `politics`, `business`, `economy`, `science`, `technology`, `cricket`, and `sport`.
   - Merges related subcategories into broader groups: `sport`, `business`, `science_technology`.

2. **Data Preprocessing**:
   - Removes duplicates.
   - Cleans text by removing stopwords and punctuation.
   - Tokenizes text and converts it to lowercase.

3. **Model Training**:
   - Splits data into training and testing sets (80/20 split).
   - Converts text data into TF-IDF vectors.
   - Trains a Naive Bayes classifier.

4. **Evaluation**:
   - Evaluates the model's accuracy and generates a detailed classification report.

---

## Project Output

### Model Accuracy: 
83.33%

### Classification Report:

| Category             | Precision | Recall | F1-Score |
|-----------------------|-----------|--------|----------|
| Business             | 0.75      | 1.00   | 0.86     |
| Politics             | 1.00      | 0.44   | 0.62     |
| Science/Technology   | 0.94      | 0.73   | 0.82     |
| Sport                | 0.82      | 1.00   | 0.90     |

---


## Installation

Follow these steps to set up the project on your local machine:

### 1. Clone the Repository
Clone the project repository to your local machine and navigate to the project directory:

```bash
git clone https://github.com/SultanaTania/news_classification.git
cd news_classification
```

### 2. Set up a Virtual Environment (Optional)
It is recommended to use a virtual environment to manage dependencies:

```bash
python -m venv env
env\Scripts\activate     # For Windows
```

### 3. Install Dependencies
Install the required Python libraries using the requirements.txt file:

```bash
pip install -r requirements.txt     # For Windows
```

### 5. Run the Notebook
Open the Jupyter Notebook (dswf_project_final.ipynb) in your preferred IDE (e.g., Jupyter, Colab) and execute the cells sequentially.