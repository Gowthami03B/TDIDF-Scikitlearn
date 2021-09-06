# TDIDF-Scikitlearn
Calculate tf-idf scores using text data and the Python library scikit-learn
- The text analysis method Tf-idf tries to identify the most distinctively frequent or significant words in a document.
- We use the module TFIDF Vectorizer to achieve the same

### What is a TfidfVectorizer?
TF (Term Frequency): The number of times a word appears in a document is its Term Frequency. A higher value means a term appears more often than others, and so, the document is a good match when the term is part of the search terms.

term_frequency = number of times a given term appears in document

IDF (Inverse Document Frequency): Words that occur many times a document, but also occur many times in many others, may be irrelevant. IDF is a measure of how significant a term is in the entire corpus.

inverse_document_frequency = log(total number of documents / number of documents with term) + 1*****
- The reason we take the inverse, or flipped fraction, of document frequency is to boost the **rarer words that occur in relatively few documents**. Think about the inverse document frequency for the word “said” vs the word “pigeon.” The term “said” appears in 13 (document frequency) of 14 (total documents) Lost in the City stories (14 / 13 –> a smaller inverse document frequency) while the term “pigeons” only occurs in 2 (document frequency) of the 14 stories (total documents) (14 / 2 –> a bigger inverse document frequency, a bigger tf-idf boost).

The TfidfVectorizer converts a collection of raw documents into a matrix of TF-IDF features.

### Calculate tf–idf¶
To calculate tf–idf scores for every word, we’re going to use scikit-learn’s TfidfVectorizer.

tfidf_vectorizer = TfidfVectorizer(input='filename', stop_words='english')
