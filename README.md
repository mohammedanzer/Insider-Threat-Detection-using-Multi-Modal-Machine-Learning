# Multi-Modal Insider Threat Detection

**Author:** Ann Mery Thomas | Student ID: 25111876  
**Module:** Data Mining and Machine Learning — National College of Ireland  
**Dataset:** [CERT Insider Threat Dataset r4.2](https://www.sei.cmu.edu/library/insider-threat-test-dataset/)

## Overview
An explainable multi-modal insider threat detection system that combines:
- Email sentiment analysis (VADER)
- Behavioral anomaly detection (LSTM Autoencoder)
- Peer-group baseline comparison (Big Five personality clustering + Z-score)
- Feature fusion classifier (Gradient Boosting)
- XAI explainability layer (SHAP)

## Research Questions
1. How does peer-group anomaly detection reduce false positives in insider 
   threat environments when combined with multimodal sentiment and sequence models?
2. To what extent does email sentiment analysis combined with temporal behavioral 
   logs improve detection on highly imbalanced datasets like CERT r4.2?

## Results (Cross-Validation)
| Model | F1 | Precision | Recall | AUC-ROC |
|---|---|---|---|---|
| Random Forest | 0.700 ± 0.079 | 0.766 ± 0.142 | 0.686 ± 0.147 | 0.982 ± 0.012 |
| **GBM (final)** | **0.833 ± 0.077** | **0.815 ± 0.128** | **0.886 ± 0.140** | **0.980 ± 0.027** |

## Pipeline
