# Airline Tweet Sentiment Analysis – Replication Study

## Original Paper

This project replicates and compares results with the following study:

M. T. H. K. Tusar and M. T. Islam (2021).  
*A Comparative Study of Sentiment Analysis Using NLP and Different Machine Learning Techniques on US Airline Twitter Data.*

Paper link (ArXiv):  
https://arxiv.org/abs/2110.00859

The authors use **Twitter US Airline Sentiment (CrowdFlower)** dataset and apply classic machine learning models such as Naive Bayes and SVM for sentiment classification.


---

## Project Goal
The goal of this project is to:
- Classify airline tweets as **negative**, **neutral**, or **positive**
- Compare simple machine learning models
- Check whether a simple changed methods improves the results

---

## Dataset
- Dataset name: **Twitter US Airline Sentiment (CrowdFlower)**
- Source: Kaggle  
  https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment
- Collected in February 2015
- About 14,600 tweets related to U.S. airlines
- Each tweet has a sentiment label (negative / neutral / positive)

This is the same datset used in the original paper.
While the dataset same, our implementation differs in preprocessing and methodology choices, evaluation using 10-fold cross-validation, and the use of Macro-F1 as the main metric.

---

## Methods
### Data Processing
- Converted text to lowercase
- Removed links and user mentions
- Removed special characters and numbers
- Created a cleaned text column

### Models Used
- Multinomial Naive Bayes
- Linear Support Vector Machine (SVM)
- Majority Vote model (Naive Bayes + SVM)

### Text Representation
- TF-IDF (Term Frequency–Inverse Document Frequency)

### Evaluation
- 10-fold stratified cross-validation
- Metrics used:
  - Accuracy
  - Macro-F1 score
- Confusion matrices were used to analyze errors

---

## Results
- **Linear SVM** performed best:
  - Accuracy: **78.64%**
  - Macro-F1: **0.7130**
- Naive Bayes performed weaker than SVM
- The majority vote model did not improve performance
- Most classification errors occurred between **neutral** and **negative** tweets

---

## Repository Structure
- `FCSS_Poster.ipynb` – Complete analysis and experiments
- `data/` – Raw and cleaned datasets
- `figures/` – Images used in the poster
- `results/` – Model results 
- `requirements.txt` – Required Python libraries
- `Poster` - poster preview

---


