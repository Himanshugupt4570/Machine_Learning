# Machine Learning Projects

**Author:** Himanshu Gupta  
**Academic Background:** BS-MS Mathematics and Data Science  
**GitHub:** [Himanshugupt4570](<https://github.com/Himanshugupt4570>)

## About This Repository

This repository contains two machine learning projects developed using Python and Jupyter Notebook. These projects demonstrate practical applications of machine learning, data preprocessing, classification, and model evaluation.

## Projects


### 1. MNIST Handwritten Digit Classification

**Notebook:** `MNIST.ipynb`

**Objective:** Implement machine learning algorithms to recognize handwritten digits (0–9) using the MNIST dataset.

**Dataset:**
- 70,000 grayscale handwritten digit images.
- Image dimensions: 28 × 28 pixels.
- 784 features per image.
- 60,000 training samples and 10,000 test samples.

**Algorithms Implemented:**
- Stochastic Gradient Descent (SGD) Classifier
- Random Forest Classifier
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

**Additional Techniques:**
- Stratified cross-validation
- GridSearchCV for hyperparameter optimization
- Confusion matrix analysis
- Precision-recall and ROC analysis
- Image data augmentation using pixel shifting
- Multilabel classification

**Best KNN Configuration:**

```python
KNeighborsClassifier(
    n_neighbors=4,
    weights='distance'
)
```

**Evaluation Results:**

| Metric | Result |
|---|---:|
| Best cross-validation accuracy | 97.03% |
| Test accuracy after data augmentation | 97.63% |
| Multilabel macro F1-score | 0.9764 |
| Multilabel weighted F1-score | 0.9778 |

*Note: F1 scores correspond to the auxiliary multilabel task (digit ≥ 7 and odd digit), not ten-class digit recognition. The reported test accuracy after augmentation is from the notebook's saved output.*

### 2\. Sentiment Analysis Using Natural Language Processing

**Notebook:** `Sentiment_Analysis.ipynb`

**Objective:** Develop a machine learning model to classify textual movie reviews into positive and negative sentiment categories.

**Dataset:**

- IMDb movie review dataset.
- Binary sentiment labels: Positive and Negative.
- Training and testing data.

**Workflow:**

- Loading and organizing textual data.
- Text preprocessing.
- Feature extraction and representation.
- Model training and sentiment classification.
- Model evaluation and performance analysis.

**Libraries:** Python, Pandas, tqdm and the NLP/ML libraries used in the notebook.

## Technical Skills Demonstrated

- Python Programming
- Machine Learning
- Natural Language Processing (NLP)
- Data Preprocessing
- Exploratory Data Analysis
- Classification Algorithms
- Model Training and Evaluation
- Data Visualization

## Repository Structure

``` text
Machine_Learning/
│
├── MNIST.ipynb
├── Sentiment_Analysis.ipynb
└── README.md
```

## How to Run the Projects

1. Clone this repository:

``` bash
git clone https://github.com/Himanshugupt4570/Machine_Learning.git
```

2. Navigate to the project directory:

``` bash
cd Machine_Learning
```

3. Install the required libraries used by the notebooks.
4. Open the notebooks using Jupyter Notebook or VS Code.
5. Execute the notebook cells sequentially.

**Note:** The Sentiment Analysis notebook requires the IMDb dataset. Configure its dataset path according to your local environment before execution.

## Learning Outcomes

Through these projects, I gained practical experience in applying machine learning techniques to image classification and natural language processing tasks. I also developed experience in data handling, model development, and performance evaluation.

## Future Improvements

- Experiment with different classification algorithms.
- Compare model performance using appropriate evaluation metrics.
- Improve preprocessing and feature extraction techniques.
- Explore deep learning approaches for image and text classification.

---

*These projects represent my learning and practical exploration of machine learning as a BS-MS Mathematics and Data Science student.*
