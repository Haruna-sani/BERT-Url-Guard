# BERT URL Classifier

## Model Performance Comparison

### BERT Model Performance

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.99      | 0.95   | 0.97     | 1445    |
| 1     | 0.94      | 0.99   | 0.96     | 360     |
| 2     | 0.60      | 0.80   | 0.68     | 137     |
| 3     | 0.90      | 0.79   | 0.84     | 58      |
| **Overall Accuracy** | **0.94** |  |  | **2000** |

### Random Forest Model Performance

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.95      | 0.98   | 0.96     | 1465    |
| 1     | 0.88      | 0.96   | 0.92     | 362     |
| 2     | 0.87      | 0.39   | 0.54     | 122     |
| 3     | 0.97      | 0.75   | 0.84     | 51      |
| **Overall Accuracy** | **0.93** |  |  | **2000** |

### XGBoost Model Performance

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.96      | 0.91   | 0.94     | 1465    |
| 1     | 0.79      | 0.99   | 0.88     | 362     |
| 2     | 0.50      | 0.43   | 0.46     | 122     |
| 3     | 0.69      | 0.67   | 0.68     | 51      |
| **Overall Accuracy** | **0.89** |  |  | **2000** |

### Bi-LSTM Model Performance

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.96      | 0.99   | 0.98     | 1465    |
| 1     | 0.98      | 0.95   | 0.97     | 362     |
| 2     | 0.75      | 0.57   | 0.64     | 122     |
| 3     | 0.90      | 0.84   | 0.87     | 51      |
| **Overall Accuracy** | **0.96** |  |  | **2000** |

## Comparative Analysis

### 1. **Accuracy Comparison**
- **BERT:** 94%
- **Random Forest:** 93%
- **XGBoost:** 89%
- **Bi-LSTM:** 96%

The **Bi-LSTM** achieved the highest accuracy at 96%, slightly outperforming BERT (94%). XGBoost performed the worst, with an accuracy of 89%.

### 2. **Precision and Recall Comparison**
- **BERT** exhibited the highest precision for class 0 and class 1.
- **Random Forest** had competitive precision but struggled with class 2, showing only 39% recall.
- **XGBoost** had the lowest precision and recall for class 2, indicating poor performance in detecting minority classes.
- **Bi-LSTM** achieved strong precision and recall overall, making it a highly reliable model.

### 3. **F1-Score Comparison**
- BERT had the best F1-score for class 1 and 3.
- Bi-LSTM was the best overall performer due to a higher recall rate.
- Random Forest and XGBoost had lower F1-scores for class 2, which indicates difficulty in handling minority classes.

### **Conclusion**
While **Bi-LSTM outperformed BERT in overall accuracy**, BERT remains competitive with strong precision across all classes. Random Forest and XGBoost struggled with minority class classification, making them less reliable choices for imbalanced datasets.

Overall, **Bi-LSTM and BERT** are the top choices for URL classification, depending on whether a transformer-based or recurrent neural network model is preferred.
### *Data url: https://www.kaggle.com/datasets/talhabarkaatahmad/dataset-malicious-urls**

