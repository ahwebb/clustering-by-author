# Clustering By Author

## Introduction
This project attempts to classify authors based on their writing styles. I take a supervised approach via bag-of-words features as well as an unsupervised approach via clustering in order to achieve this goal.

## The Data
Database utilized for this project can be found here: https://www.kaggle.com/snapcrack/all-the-news. In order to keep the amount of data manageable and within the scope of my computational resources, I selected a subset of articles from the same genre to make clustering a bit more difficult. I chose the 10 most prolific authors of the film genre to train my model.

## Modeling Technique
As mentioned earlier, both a supervised and unsupervised approach were taken to modeling the film articles.

### Supervised
Documents were cleaned, and words within the document were tokenized and bagged with the 2000 most common words used to generate bag-of-words features. Random forest classification and Logistic Regression were utilized to distinguish authors based on these bag-of-word features.

### Unsupervised
Tfidf vectors were created for each of the documents, and the feature space was reduced using LSA. Articles were then clustered utilizing KMeans, MeanShift, and Spectral clustering techniques

## Conclusions
Unfortunately, neither the supervised nor unsupervised methods yielded results worth noting. Neither modeling technique performed particularly well, which could be attributed to several things. Of the supervised modeling techniques applied, Logistic Regression performed markedly better than Random Forest Classification (as determined by R2 values) though performed quite poorly overall. Similarly, clustering yielded one large globular cluster and several very small clusters - suggesting that most of the articles were, in fact, quite similar and indistinguishable between authors.

## Future Goals
* Fine tune supervised models and optimize paramters
* Feed more data into the clustering models to illuminate more nuanced differences between authors
* Apply to more genres outside of Film!
