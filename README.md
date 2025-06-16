# Credit Card Fraud Detection Project

## Dataset
The dataset used for this project is sourced from Kaggle:  
[Credit Card Fraud]([https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023/data](https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud))
- **Size**: 1,000,000 records
- **Features**:
  - `distance_from_home`: Distance from home where the transaction occurred.
  - `distance_from_last_transaction`: Distance from the last transaction.
  - `ratio_to_median_purchase_price`: Ratio of the purchase price to the median purchase price.
  - `repeat_retailer`: Whether the transaction was made at a retailer where the user has shopped before.
  - `used_chip`: Whether the transaction used a chip-based payment method.
  - `used_pin_number`: Whether the transaction used a PIN number.
  - `online_order`: Whether the transaction was an online order.
  - `fraud`: Target variable indicating whether the transaction is fraudulent (`0` = Non-Fraud, `1` = Fraud).

### Preprocessing
- Checked for missing values (none found).
- Balanced the dataset using SMOTE to address class imbalance (fraudulent vs. non-fraudulent transactions).
- Split the dataset into training and testing sets (`80% train`, `20% test`) with stratification to preserve class distribution.

## Training Recipes

### Step 1: Data Preparation
- Loaded the dataset.
- Balanced the dataset using SMOTE to ensure equal representation of fraudulent and non-fraudulent transactions.

### Step 2: Feature Engineering
- Analyzed feature distributions and correlations using visualizations (e.g., histograms, boxplots, correlation heatmaps).
- Identified key features contributing to fraud detection.

### Step 3: Model Training
- Trained machine learning models on the balanced dataset:
  - Logistic Regression
  - Random Forest Classifier
- Evaluated models using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC and selected the model with SOTA performance.

### Step 4: Hyperparameter Tuning
- Used default hyperparameters for initial training.

### Step 5: Evaluation
- Compared performance on both retain and forget sets after applying machine unlearning.


## Models Used

### Logistic Regression
- **Performance**:
  - Accuracy: 93.60%
  - Precision: 92.91%
  - Recall: 94.41%
  - F1-Score: 93.65%
  - ROC-AUC: 93.60%

### Random Forest 
- **Performance**:
  - Accuracy: 99.99%
  - Precision: 99.98%
  - Recall: 99.99%
  - F1-Score: 99.99%
  - ROC-AUC: 99.99%

## Machine Unlearning

### Approach
- **Finetuning**:
  - Retrained the model only on the retain set (`online_order = 0`).
  - Achieved perfect performance on the retain set but degraded performance on the forget set.
### Implementation
- Split the dataset into:
  - **Retain Set**: Transactions with `online_order = 0`.
  - **Forget Set**: Transactions with `online_order = 1`.
- Applied finetuning techniques to "unlearn" the influence of the `online_order` feature.

## Results

### Original Model Performance
- **Retain Set**:
  - Accuracy: 99.99%
  - Precision: 99.94%
  - Recall: 100.00%
  - F1-Score: 99.97%
  - ROC-AUC: 99.99%
- **Forget Set**:
  - Accuracy: 99.99%
  - Precision: 100.00%
  - Recall: 99.99%
  - F1-Score: 99.99%
  - ROC-AUC: 99.99%

### After Machine Unlearning (Finetuning)
- **Retain Set**:
  - Accuracy: 100.00%
  - Precision: 100.00%
  - Recall: 100.00%
  - F1-Score: 100.00%
  - ROC-AUC: 100.00%
- **Forget Set**:
  - Accuracy: 46.05%
  - Precision: 99.98%
  - Recall: 10.55%
  - F1-Score: 19.09%
  - ROC-AUC: 55.27%
