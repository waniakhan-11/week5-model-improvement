# Bank Marketing – Model Improvement for Imbalanced Classification

## Project Overview

This project focuses on improving a machine learning model for an imbalanced classification problem using the Bank Marketing dataset.

The project compares a baseline Random Forest model with different techniques, including class weighting, prediction threshold adjustment, and oversampling.

The main objective is to improve recall so that the model can identify more customers who subscribe to a bank term deposit.

## Dataset

- **Dataset:** Bank Marketing Dataset (bank-full.csv)
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Total records:** 45,211
- **Total original features:** 16
- **Target:** `y` (yes/no)

### Class Distribution

- No: 39,922 (88.3%)
- Yes: 5,289 (11.7%)

## Results

The baseline Random Forest achieved 35.46% recall on the validation set.

After testing different techniques, a prediction threshold of 0.1 achieved 93.74% recall on the validation set.

The final model achieved 91.59% recall on the test set.

| Metric | Baseline Validation | Final Test |
|---|---:|---:|
| Accuracy | 90.30% | 80.38% |
| Precision | 65.79% | 36.51% |
| Recall | 35.46% | 91.59% |
| F1-score | 46.08% | 52.21% |

*Note: Baseline results are from validation data, while final results are from test data.*

## Project Structure

- `bank-marketing-model-improvement.ipynb` – Complete notebook containing data preparation, baseline model, error analysis, experiments, feature importance, and final evaluation.
- `README.md` – Project description and results.
- `requirements.txt` – Required Python libraries.

## How to Run

1. Clone or download this repository.
2. Install the required libraries:

   `pip install -r requirements.txt`

3. Open the notebook in Jupyter Notebook or Google Colab.
4. Run the notebook cells in order.
5. The dataset is downloaded directly from the UCI Machine Learning Repository.

## Techniques Used

- Data preprocessing and missing-value handling
- Stratified train-test split
- Dummy Classifier
- Random Forest Classifier
- Balanced class weights
- Prediction threshold adjustment
- Random oversampling
- Feature importance analysis
- Precision, Recall, F1-score, and Confusion Matrix

## Conclusion

Lowering the prediction threshold improved the model's ability to identify potential subscribers. The final model achieved 91.59% recall on the test set, although precision decreased due to more false positives.
