# Machine Learning Projects

A collection of hands-on machine learning projects developed using Python and Jupyter Notebook. The repository covers image classification, natural language processing, email spam detection, and predictive modelling on structured data.

## Author

**Himanshu Gupt**  
BS-MS Mathematics and Data Science  
GitHub: [Himanshugupt4570](https://github.com/Himanshugupt4570)

---

## Projects

### 1. MNIST Handwritten Digit Classification

**Notebook:** `MNIST.ipynb`

**Objective:** Classify handwritten digits (0–9) from grayscale images.

**Dataset**
- 70,000 images, each 28 × 28 pixels.
- 784 pixel features per image.
- Standard split: 60,000 training images and 10,000 test images.

**Methods explored**
- Stochastic Gradient Descent (SGD)
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Stratified cross-validation
- Confusion matrix, precision, recall, F1-score and ROC/AUC analysis
- Hyperparameter search and image-shifting augmentation
- Multiclass and multilabel classification experiments

**Reported results**

| Evaluation | Result |
|---|---:|
| Best cross-validation accuracy (KNN) | 97.03% |
| Test accuracy after augmentation | 97.63% |
| Multilabel macro F1-score | 0.9764 |
| Multilabel weighted F1-score | 0.9778 |

The macro and weighted F1-scores refer to the separate multilabel experiment; they are not the ten-class digit-classification scores.

### 2. Sentiment Analysis

**Notebook:** `Sentiment_Analysis.ipynb`

**Objective:** Classify text reviews as positive or negative using natural language processing and supervised machine learning.

**Methods documented**
- Text preprocessing
- TF-IDF feature extraction
- Logistic Regression
- Hyperparameter optimization and model evaluation

**Reported results**

| Evaluation | Result |
|---|---:|
| Cross-validation accuracy | 89.7% |
| Test accuracy | 89.9% |

### 3. Titanic Survival Prediction

**Notebook:** `Titanic_Dataset.ipynb`

**Objective:** Predict passenger survival using passenger and travel information.

**Dataset and preprocessing**
- 891 labelled passenger records in the training data.
- Numeric features: `Age`, `SibSp`, `Parch`, and `Fare`.
- Categorical features: `Pclass`, `Sex`, and `Embarked`.
- Missing numeric values filled using the median.
- Numeric features standardized using `StandardScaler`.
- Missing categorical values filled using the most frequent value.
- Categorical features encoded using `OneHotEncoder`.

**Models and 10-fold cross-validation**

| Model | Mean accuracy |
|---|---:|
| Support Vector Machine (SVC) | 82.49% |
| Random Forest (100 trees) | 81.38% |

The notebook also generates predictions for the separate Titanic test dataset. That dataset has no survival labels, so a test-set accuracy is not reported.

**Additional exploration**
- Survival rates across age groups.
- Relationship between family members aboard and survival.

### 4. Email Spam Classification

**Notebook:** `Spam_Classifier.ipynb`

**Objective:** Classify email messages as spam or ham (legitimate email).

**Dataset**
- SpamAssassin public email corpus.
- 2,500 ham emails.
- 500 spam emails.
- 3,000 emails in total.
- 80:20 train-test split with `random_state=42`.

**Preprocessing and feature engineering**
- Parse email messages and inspect MIME structures.
- Extract plain text from text/plain and text/html messages.
- Remove HTML markup and decode HTML entities.
- Normalize text, remove punctuation and process numbers and URLs.
- Apply Porter stemming.
- Convert emails into word-count features.
- Build a sparse feature matrix using a custom transformer and a vocabulary of up to 1,000 words.
- Combine preprocessing stages using a Scikit-learn pipeline.

**Model:** Logistic Regression (`max_iter=1000`, `random_state=42`)

**Reported evaluation results**

| Metric | Result |
|---|---:|
| Mean 3-fold cross-validation accuracy | 98.33% |
| Test precision | 92.08% |
| Test recall | 97.89% |

Precision and recall are reported from the notebook's held-out test split. Test accuracy and F1-score are not reported in the notebook.

---

## Technical Skills Demonstrated

- Python programming and Jupyter Notebook
- Supervised machine learning and classification
- Natural Language Processing (NLP)
- Image classification
- Data cleaning and preprocessing
- Feature engineering and feature extraction
- Scikit-learn pipelines and custom transformers
- Model selection and cross-validation
- Hyperparameter optimization
- Classification metrics and model evaluation
- Data visualization

## Technologies and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- NLTK
- `urlextract`
- Python email parsing utilities

## Repository Structure

```text
Machine_Learning/
├── MNIST.ipynb
├── Sentiment_Analysis.ipynb
├── Titanic_Dataset.ipynb
├── Spam_Classifier.ipynb
└── README.md
```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Himanshugupt4570/Machine_Learning.git
   ```

2. Enter the project directory:

   ```bash
   cd Machine_Learning
   ```

3. Install the libraries required by the notebook you want to run. For example:

   ```bash
   pip install numpy pandas matplotlib scikit-learn nltk urlextract jupyter
   ```

4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open a notebook and execute its cells in order.

**Dataset note:** Some notebooks download datasets from external sources. Internet access may be required on the first run. Check each notebook's dataset path and dependencies before execution.

## Learning Outcomes

These projects provided practical experience in building classification workflows from data loading and preprocessing through feature engineering, model training, validation, and evaluation. They also provided experience working with different data types, including images, email messages, reviews, and structured passenger records.

## Future Improvements

- Add reproducible dependency and environment files.
- Add confusion matrices and classification reports consistently across projects.
- Compare additional baseline and advanced models.
- Improve experiment tracking and documentation.
- Add clear dataset setup instructions and reproducible train-test evaluation.

---

*This repository documents my practical learning and experimentation in machine learning as a BS-MS Mathematics and Data Science student.*
