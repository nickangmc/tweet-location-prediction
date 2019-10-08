# Short Text Location Prediction
Program written and developed in the language **Python** along with **sklearn** as the final project for the subject COMP30027: Machine Learning at the University of Melbourne - Semester 1, 2019. 

### Goal: 
To build and critically analyse some supervised Machine Learning methods, with the aim of automatically identifying the location from which a textual message was sent, as one of four Australian cities. Although this is a simplification of the more general problem of **geotagging**, it is still a very difficult problem, which has been well-studied, but a solution remains elusive.

This aims to reinforce the largely theoretical concepts surrounding learners, data representation, and evaluation, by applying them to a sophisticated problem. 

---

### Datasets:
The data were collected from Twitter (https://www.twitter.com), specifically for this Project. According to Twitter’s **Terms of Service**, this data cannot share for any other purpose, or reproduce it in any form, other than as _isolated examples_.Please note that the dataset is a sample of actual data posted to the World Wide Web. As such, it may contain information that is in _poor taste, or that could be construed as offensive_. The opinions expressed within the data are those of the (anonymised) authors, and in no way express the official views of the University of Melbourne or any of its employees; using the data in an educative capacity does not consitute endorsement of the content contained therein.

#### With that in mind, the following samples show the data looks like: 
  ![text-example](https://raw.githubusercontent.com/nickangmc/tweet-location-prediction/master/readme-images/text-example.png)

---

### Classifications
This project will be looking at two classification techniques:

- **Multi-variate Bernoulli Naïve Bayes Classifier (BNB)**

    The model is based on Bernoulli probabilistic models where every outcome only has two scenarios. In the case of the project, every token (word) in the feature vector of a document (instance) is associated with a value of 0 or 1. The value of 1 means that the token occurs in that particular document; the value of 0 indicates the token does not occurs in the document.
    
- **Multinomial Naïve Bayes Classifier (MNB)**

    This model takes an alternative approach to represent the documents, that is unlike binary values, it associates each token with a term frequency. For a given term, its number of its occurrence in a document is counted and assigned to the term.

--- 

### Feature Engineering
There are several popular feature engineering methods used in this project:

- _Count_ vectorizer 

    It is used to break the string of text down to individual words (tokenization), which then the frequency of each individual word is counted and recorded to be use as the features.
    
- _Term Frequency - Inverse Document Frequency_ vectorizer 

    Similarly it extracts individual words from the text, and counts the frequencies of words, however it normalizes the overall words frequencies to minimize the weight of common words.
    
--- 

###  Hyperparameter Optimization
Additive Smoothing, as known as Laplace Smoothing was used in both classifiers. The following graph shows how different values of smoothing value affect the accuracies of the classifiers: 

  ![additive-smoothing](https://raw.githubusercontent.com/nickangmc/tweet-location-prediction/master/readme-images/additive-smoothing.png)

---

### Result
The following table shows the metrics for both classifiers trained and tested with optimum hyperparameters for both feature sets on _development dataset_. More specifically, the metrics include weighted accuracy, weighted precision, weighted recall, and weighted f- score.

![result](https://raw.githubusercontent.com/nickangmc/tweet-location-prediction/master/readme-images/result.png)

When evaluated against _testing dataset_, it obtained a higher accuracy of 0.35997 within top 10% of all submissions on a [Kaggle Competition](https://www.kaggle.com/c/machine-learning-project-2/).

---

### Project Outcome
All the tasks and challenges within the scope of this project were completed. For more details and in-depth analysis, feel free to have a look at the [_report_](https://github.com/nickangmc/tweet-location-prediction/blob/master/report.pdf) file in this repo.



