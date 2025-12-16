# Predicting Credit Card Fraud

**Vijay Bhore**

## Executive Summary

This project investigates the use of modern machine learning techniques to identify fraudulent credit card transactions. The analysis is based on a publicly available Kaggle dataset containing transaction records from European cardholders ([https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)). Multiple classification models—including Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost—are implemented to distinguish fraudulent transactions from legitimate ones. The primary objective is to improve fraud detection performance and contribute to safer and more reliable credit card usage.

## Results

This study evaluated the performance of several machine learning models for credit card fraud detection, using both baseline and tuned configurations. The models examined were Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost.

While all models achieved high overall accuracy—many approaching perfect training accuracy—their effectiveness varied substantially when assessed using metrics more appropriate for imbalanced classification problems, particularly precision-recall area under the curve (PR AUC) and recall. These metrics are especially important in fraud detection, where failing to identify fraudulent transactions can carry significant costs.

Among the models tested, the optimized Random Forest and CatBoost models demonstrated the strongest overall performance. They achieved the highest PR AUC scores of 0.8724 and 0.8931, respectively, while maintaining a favorable balance between precision and recall. This balance suggests that both models are well-suited for real-world fraud detection scenarios.

In contrast, the LightGBM model performed poorly in its baseline configuration, yielding the lowest PR AUC score of 0.2606 and relatively weak recall. However, after optimization, its performance improved markedly, reaching a PR AUC of 0.8699, underscoring the impact of effective hyperparameter tuning.

XGBoost emerged as the fastest model to train, with its base implementation completing in just 1.1569 seconds. Despite its computational efficiency, its precision and recall did not match those of the top-performing ensemble models, highlighting a trade-off between training speed and predictive effectiveness.

Overall, the optimized versions of all models outperformed their baseline counterparts, reinforcing the importance of model tuning. The results strongly support the use of ensemble-based approaches—particularly Random Forest and CatBoost—for credit card fraud detection, as they effectively balance computational efficiency with high predictive performance and recall.
