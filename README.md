# Conference Recommendation System (ProjectTCNER)
Final project for Data Science, module IENLP+DM - University of Twente 2023/2024

This repository contains the code and documentation for the Conference Recommendation System project, developed as part of a Data Science course. The project aims to recommend conferences to researchers based on the titles of their new articles using text classification techniques.

## Project Motivation
This project addresses the challenge of recommending appropriate academic conferences based on the titles of research articles. By leveraging natural language processing (NLP) techniques and machine learning algorithms, the project aims to facilitate researchers in selecting conferences that align with their work, thereby enhancing academic dissemination and networking.

## Source Data
The datasets used in this project include:

* Training Set: Contains 21,643 samples with titles labeled by the corresponding conference.
* Test Set: Used for evaluating the final model's performance.

### Data Quality Considerations
* Class Imbalance: The dataset showed significant class imbalance, particularly with the "ISCAS" category being overly prevalent.
* No Missing Values: Verified and ensured that there were no missing values in the dataset.

## Methodology
### Vectorization
We utilized the TfIdfVectorizer from scikit-learn to convert text data into feature vectors. The TF.IDF approach was chosen for its ability to highlight significant terms in the context of academic titles, making it suitable for our classification task.

### Preprocessing
Key preprocessing steps included:

* Lowercasing: Standardizing text by converting to lowercase.
* Stop Words Removal: Excluding common but irrelevant terms.
* N-gram Range: Capturing phrases of varying lengths to improve feature richness.

### Models
We evaluated several machine learning models:

* Complement Naive Bayes: Effective for class imbalance and high-dimensional data.
* K-Nearest Neighbors (K-NN): Simple and robust for multiclass problems.
* Support Vector Machines (SVM): Versatile and powerful for high-dimensional spaces.
* Random Forest: Resistant to overfitting and suitable for high-dimensional data.

### Hyperparameter Tuning
Hyperparameters were fine-tuned using nested cross-validation. Specific parameters adjusted for each model include n-gram range, stop words, kernel types, and class weights, among others.

### Evaluation
Models were evaluated using 5-fold cross-validation and metrics such as micro-averaged precision, recall, and F1-score to handle class imbalance effectively.

![](https://github.com/GiuliaPais/ProjectTCNER/blob/main/figures/Slide7.jpeg)

![](https://github.com/GiuliaPais/ProjectTCNER/blob/main/figures/Slide9.jpeg)

## Advanced Techniques
We experimented with advanced approaches, including:

* BERT: Applied for enhanced contextual understanding.
* GloVe Pre-trained Vectors: Evaluated for document encoding with SVM.
* Stemming: Tested different stemmers to assess impact on performance.



