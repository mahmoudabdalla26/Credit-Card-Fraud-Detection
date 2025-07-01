# Credit Card Fraud Detection – Meta Algorithms Focus

This project explores credit card fraud detection, not with the primary goal of deploying a model, but to deeply understand and apply **Meta Algorithms** in machine learning.

## 💡 Objective

Rather than building a single classifier, the goal was to experiment with ensemble methods (meta-algorithms) to evaluate how combining models can improve performance, especially with complex and imbalanced data.

## 📌 What are Meta Algorithms?

Meta-algorithms are techniques that combine multiple base models instead of relying on a single one. They're especially useful when:

- Data is noisy or imbalanced
- Individual models underfit or overfit
- We want to boost generalization and reduce variance

We focused on three major types:

- **Bagging**: BaggingClassifier, RandomForestClassifier  
- **Boosting**: GradientBoostingClassifier, XGBoost  
- **Stacking**: Combining all above into one final learner

## 🔍 Workflow

1. **Baseline**: Trained a Logistic Regression model to establish a simple performance benchmark.
2. **Phase 1**: Trained all models on the original imbalanced dataset.
3. **Phase 2**: Applied SMOTE to balance the dataset, then retrained all models to observe the effect.

## 📈 Key Observations

- Before handling imbalance, **RandomForestClassifier** achieved the best F1 score with strong precision and recall.
- After applying SMOTE, **RandomForest** improved its recall while maintaining precision — resulting in the highest F1 overall.
- Models like **Logistic Regression** and **XGBoost** became highly sensitive after SMOTE (high recall, low precision), which harmed overall F1 performance.
- **Meta Algorithms** clearly helped mitigate individual model weaknesses and performed better than any single classifier.

## ✅ Conclusion

Ensemble methods, especially **Random Forest**, provided consistent and balanced performance before and after handling imbalance.  
Meta-algorithms proved useful in boosting recall without sacrificing too much precision — critical for real-world fraud detection.

> Check the full notebook for code and detailed comparison.
