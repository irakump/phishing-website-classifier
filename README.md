# Phishing Website Classifier
A machine learning project for detecting phishing websites using Python and scikit-learn, based on the [Phishing Websites dataset](https://archive.ics.uci.edu/dataset/327/phishing+websites) from the UCI Machine Learning Repository.  

The project consists of two parts:  
1. **Decision Tree**: Build an interpretable classifier, evaluate its performance, visualize the decision tree, and translate its rules into practical instructions for identifying phishing websites.  
2. **Random Forest**: Train and evaluate a random forest classifier, experiment with hyperparameter tuning, and compare its performance with the decision tree.

The project follows the CRISP-DM process, focusing on developing and evaluating machine learning models. Deploying the models is beyond the scope of this project.

## Key Findings
 
- A small, human-readable decision tree (max depth 4) reaches 90.7 % accuracy on the test set.
- A random forest (100 trees) improves this to 96.5 % accuracy and identifies 94.6 % of phishing websites.
- Both models rely mostly on the same two features: `sslfinal_state` (SSL certificate state) and `url_of_anchor` (where the links on the page point to).
- The accuracy gap should be interpreted with care: the tree was deliberately limited to depth 4 for readability, while the forest's trees were not depth-limited.

The following table compares the performance of the two models on the test set. The test set consists of 2,764 websites (1,241 phishing, 1,523 legitimate).  

| Model | Accuracy | Phishing precision | Phishing recall |
|---|---|---|---|
| Decision tree (max depth 4) | 0.91 | 0.90 | 0.89 |
| Random forest (100 trees) | 0.96 | 0.97 | 0.95 |



## Project Notebook

View the complete project, including data analysis, model development, and evaluation, in the [Jupyter Notebook](https://github.com/irakump/phishing-website-classifier/blob/main/phishing-website-classifier.ipynb).
