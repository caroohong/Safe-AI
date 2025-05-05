# Credit Card Fraud Detection Project

## Dataset
The dataset used for this project is sourced from Kaggle:  
[Credit Card Fraud Detection Dataset (2023)](https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023/data)

## Models Used
The following machine learning models were trained and evaluated:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

## Model Performance

Below are the results for each model, including key metrics such as **Accuracy**, **Precision**, **Recall**, **F1-Score**, **ROC-AUC**, and **Inference Time**.

---

### Logistic Regression
| Metric                  | Value          |
|-------------------------|----------------|
| Accuracy                | 0.9649         |
| Precision               | 0.9770         |
| Recall                  | 0.9523         |
| Inference Time (Total)  | 0.013712 sec   |
| Inference Time (Per Sample) | ~0.000000 sec |

---

### Adam Optimizer Variations

#### Adam lr=0.001
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9091  |
| Precision    | 0.9879  |
| Recall       | 0.8283  |
| F1-Score     | 0.9011  |
| ROC-AUC      | 0.9628  |

#### Adam lr=0.01
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9508  |
| Precision    | 0.9849  |
| Recall       | 0.9157  |
| F1-Score     | 0.9491  |
| ROC-AUC      | 0.9898  |

#### Adam with Weight Decay
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.8969  |
| Precision    | 0.9954  |
| Recall       | 0.7976  |
| F1-Score     | 0.8856  |
| ROC-AUC      | 0.9411  |

---

### SGD Optimizer Variations

#### SGD lr=0.001
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9171  |
| Precision    | 0.9979  |
| Recall       | 0.8359  |
| F1-Score     | 0.9097  |
| ROC-AUC      | 0.9787  |

#### SGD lr=0.01
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9478  |
| Precision    | 0.9884  |
| Recall       | 0.9063  |
| F1-Score     | 0.9456  |
| ROC-AUC      | 0.9896  |

#### SGD lr=0.05
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9565  |
| Precision    | 0.9830  |
| Recall       | 0.9291  |
| F1-Score     | 0.9553  |
| ROC-AUC      | 0.9915  |

#### SGD lr=0.1
| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.9590  |
| Precision    | 0.9829  |
| Recall       | 0.9342  |
| F1-Score     | 0.9579  |
| ROC-AUC      | 0.9921  |

---

### Random Forest
| Metric                  | Value          |
|-------------------------|----------------|
| Accuracy                | 0.9998         |
| Precision               | 0.9997         |
| Recall                  | 1.0000         |
| F1-Score                | 0.9998         |
| ROC-AUC                 | 0.9998         |
| Inference Time (Total)  | 1.034978 sec   |
| Inference Time (Per Sample) | ~0.000009 sec |

---

### Support Vector Machine (SVM)
| Metric                  | Value             |
|-------------------------|-------------------|
| Accuracy                | 0.9971            |
| Precision               | 0.9963            |
| Recall                  | 0.9979            |
| F1-Score                | 0.9971            |
| ROC-AUC                 | 0.9971            |
| Inference Time (Total)  | 104.024427 sec    |
| Inference Time (Per Sample) | ~0.000915 sec |
