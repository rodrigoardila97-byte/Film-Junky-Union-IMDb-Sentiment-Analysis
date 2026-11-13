# Film Junky Union IMDb Sentiment Analysis

IMDb sentiment classification with TF-IDF and scikit-learn. Compares logistic regression, linear SVM and Complement Naive Bayes; logistic regression test F1: 0.9046.

Academic project completed as part of the TripleTen Data Science program.

## Problem and objective

Classify English-language movie reviews as negative or positive. The project target is a test F1 score of at least 0.85.

## Data and preparation

The project uses the IMDb review dataset supplied with the course. I reviewed missing values and class balance, normalized review text, and audited duplicated and normalized texts.

Only review text is used as a predictor. Ratings and target-related metadata are excluded from the feature set. The official training and test partitions are preserved.

## My contribution and modeling decisions

- Developed the exploratory analysis, text preprocessing, model comparisons and evaluation.
- Built TF-IDF features and fitted the vocabulary using training data.
- Used internal validation for model selection, keeping the official test partition separate.
- Compared logistic regression, linear SVM and Complement Naive Bayes against a constant baseline.
- Evaluated both positive and negative classes and inspected prediction errors and manually written review examples.

## Recorded test results

The test set contained 23,535 reviews.

| Model | Positive-class F1 | ROC-AUC | Accuracy |
| --- | ---: | ---: | ---: |
| Logistic regression | 0.9046 | 0.9658 | 0.9048 |
| Linear SVM | 0.9028 | 0.9661 | 0.9033 |
| Complement Naive Bayes | 0.8691 | 0.9457 | 0.8727 |
| Constant baseline | 0.0000 | 0.5000 | 0.5015 |

All three trained classifiers exceeded the positive-class F1 target. These numbers summarize the recorded test evaluation; model selection was performed using validation data.

## Tools

Python, pandas, NumPy, Matplotlib, scikit-learn and Jupyter Notebook.

## How to review and run

1. Open the project's `.ipynb` file in this repository to read the code, saved outputs and conclusions.
2. To execute it, use Jupyter Notebook or Visual Studio Code with Python and the required libraries.
3. Place `imdb_reviews.tsv` beside the notebook, or configure the data path in the loading cell. The notebook also supports the course path `/datasets/imdb_reviews.tsv`.
4. Run the cells in order.

The original dataset is needed for execution and is not included with this README. The workflow uses TF-IDF and classical classifiers and can run on CPU.

## Limitations

The models were trained on English reviews. Performance on other languages or domains has not been established. Sarcasm, mixed opinions and unfamiliar vocabulary can produce errors. A small set of manually written reviews is illustrative and does not replace evaluation on a representative test set.

## Conclusion

TF-IDF classifiers exceeded the project's F1 target and provided a practical baseline for this dataset. The comparison supports discussion of predictive quality, computational cost and error patterns.

## Author

Rodrigo Andrés Ardila Reyes

[GitHub](https://github.com/rodrigoardila97-byte) | [LinkedIn](https://www.linkedin.com/in/rodrigo-andres-ardila-reyes-7ab8533a6)

