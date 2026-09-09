# stopwords_dataset
# 📚 NLTK Stopwords in Python

## 📌 Overview

This project demonstrates how to **download, access, and work with stopwords using NLTK (Natural Language Toolkit)** in a Jupyter Notebook.

Stopwords are common words such as **"the", "is", "a", "an", "and", "in"**, etc., that usually carry less meaningful information in text analysis. Removing these words is a common preprocessing step in **Natural Language Processing (NLP)**.

## 🎯 Objective

The main objectives of this project are:

* Install and import the NLTK library.
* Download the NLTK stopwords dataset.
* Obtain stopwords for different languages.
* Display the available stopwords.
* Understand how stopwords can be used in NLP preprocessing.

## 🛠️ Technologies Used

* **Python**
* **Jupyter Notebook**
* **NLTK (Natural Language Toolkit)**

## ⚙️ Installation

Install NLTK using pip:

```bash
pip install nltk
```

## 🚀 Implementation

Import NLTK and download the stopwords corpus:

```python
import nltk

nltk.download('stopwords')
```

Then import the stopwords corpus:

```python
from nltk.corpus import stopwords

stop_words = stopwords.words('english')
print(stop_words)
```

To check all languages available in the NLTK stopwords corpus:

```python
print(stopwords.fileids())
```

This returns the language identifiers for which stopwords are available.

## 🔍 Example

```python
from nltk.corpus import stopwords

english_stopwords = stopwords.words('english')

print("Total Stopwords:", len(english_stopwords))
print(english_stopwords)
```

### Example Output

```text
Total Stopwords: 179

['a', 'about', 'above', 'after', 'again', 'against', ...]
```

The exact number and contents may vary depending on the NLTK corpus version.

## 🧹 Using Stopwords for Text Preprocessing

Stopwords can be removed from a sentence using a simple list comprehension:

```python
text = "This is an example of text preprocessing using NLTK"

words = text.split()

filtered_words = [
    word for word in words
    if word.lower() not in stop_words
]

print(filtered_words)
```

### Output

```text
['example', 'text', 'preprocessing', 'using', 'NLTK']
```

## 🌍 Supported Languages

NLTK provides stopword lists for multiple languages, which can be viewed using:

```python
stopwords.fileids()
```

For example:

```text
arabic
azerbaijani
danish
dutch
english
finnish
french
german
greek
italian
kazakh
nepali
norwegian
portuguese
romanian
russian
slovene
spanish
swedish
tajik
turkish
```

## 📁 Project Structure

```text
NLTK-Stopwords/
│
├── NLTK_Stopwords.ipynb
└── README.md
```

## 🎓 Learning Outcome

Through this project, we learn how to use **NLTK stopwords for text preprocessing**, retrieve stopword lists for different languages, and prepare textual data for further NLP tasks such as **text classification, sentiment analysis, and text mining**.

## 🔮 Future Scope

This basic implementation can be extended to:

* Build a complete NLP preprocessing pipeline.
* Perform tokenization and stemming.
* Apply lemmatization.
* Remove punctuation and special characters.
* Use stopword removal in sentiment-analysis or classification projects.

## 👨‍💻 Author

**Lucky**

B.Tech Engineering Student | AI & Generative AI Enthusiast
