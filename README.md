# Dataset
https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023/data

# Models used
- Logistic Regression
- Random Forest
- Support Vector Machine

# Training models
Results for Logistic Regression:
  Accuracy: 0.9649,
  Precision: 0.9770,
  Recall: 0.9523,
  Inference Time (Total): 0.013712 seconds,
  Inference Time (Per Sample): 0.000000 seconds

  Results for Adam lr=0.001:
  Accuracy: 0.9091,
  Precision: 0.9879,
  Recall: 0.8283,
  F1-Score: 0.9011,
  ROC-AUC: 0.9628
  
  Results for Adam lr=0.01:
  Accuracy: 0.9508,
  Precision: 0.9849,
  Recall: 0.9157,
  F1-Score: 0.9491,
  ROC-AUC: 0.9898
  
  Results for Adam with Weight Decay:
  Accuracy: 0.8969,
  Precision: 0.9954,
  Recall: 0.7976,
  F1-Score: 0.8856,
  ROC-AUC: 0.9411
  
  Results for SGD lr=0.001:
  Accuracy: 0.9171,
  Precision: 0.9979,
  Recall: 0.8359,
  F1-Score: 0.9097,
  ROC-AUC: 0.9787
  
  Results for SGD lr=0.01:
  Accuracy: 0.9478,
  Precision: 0.9884,
  Recall: 0.9063,
  F1-Score: 0.9456,
  ROC-AUC: 0.9896
  
  Results for SGD lr=0.05:
  Accuracy: 0.9565,
  Precision: 0.9830,
  Recall: 0.9291,
  F1-Score: 0.9553,
  ROC-AUC: 0.9915
  
  Results for SGD lr=0.1:
  Accuracy: 0.9590,
  Precision: 0.9829,
  Recall: 0.9342,
  F1-Score: 0.9579,
  ROC-AUC: 0.9921

Results for Random Forest:
  Accuracy: 0.9998,
  Precision: 0.9997,
  Recall: 1.0000,
  Inference Time (Total): 1.034978 seconds,
  Inference Time (Per Sample): 0.000009 seconds

Results for SVM:
  Accuracy: 0.9971,
  Precision: 0.9963,
  Recall: 0.9979,
  Inference Time (Total): 104.024427 seconds,
  Inference Time (Per Sample): 0.000915 seconds
