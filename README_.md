
# 📄 README: Cancer Type Classification Hackathon Submission

## 📌 About This Notebook
This notebook is submitted for the IITG.ai Cancer Type Prediction Hackathon. It builds a robust multi-class classification model to predict cancer types based on high-dimensional RNA sequencing expression profiles.

The pipeline demonstrates standard good practices:
- Clean and reproducible code
- Proper handling of missing values
- Model-based feature selection
- Stratified K-Fold cross-validation
- Soft voting ensemble of LightGBM models
- Evaluation using Macro F1-Score

## ⚙️ Key Details
- **Model:** LightGBM (gradient boosting trees)
- **Feature Selection:** Top 200 features by LightGBM importance
- **Cross-Validation:** 5-fold Stratified K-Fold to handle class imbalance
- **Ensemble:** Averaged probabilities for robust final prediction
- **Metric:** Macro F1-Score (aligns with competition evaluation)

## 📁 Files Included
- `train.csv`: Training features
- `train_labels.csv`: Corresponding labels for training data
- `test.csv`: Test features for final prediction
- `submission_final.csv`: Output file with `Id` and predicted `Class`
- `ML_ai_hackathon.ipynb`: The full, annotated notebook implementing the pipeline

## ✅ Assumptions & Good Practices
- No data leakage: The test set is only used for prediction, never for training or validation.
- Random seeds fixed (`random_state=42`) for reproducibility.
- The solution does not copy private code; only standard open-source libraries are used.

## 🚀 How to Run
1. Open `ML_ai_hackathon.ipynb` in Google Colab or Jupyter.
2. Upload the provided `train.csv`, `train_labels.csv`, and `test.csv`.
3. Run all cells.
4. The notebook will generate `submission_final.csv` ready for upload.

## 📊 Evaluation
The notebook prints:
- Macro F1 score for each fold
- Mean, min, max, and std of the CV F1 scores

This provides transparency for your model’s expected generalization.

## 📬 Author
Submitted by: **Ayush Kumar**  
Branch: **Chemical Engineering**  
For: IITG.ai Cancer Type Prediction Hackathon

---

**Good luck to all participants!**

---
