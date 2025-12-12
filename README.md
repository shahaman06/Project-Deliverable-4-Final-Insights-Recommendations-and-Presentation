# Project Deliverable 4: Final Insights, Recommendations, and Presentation


---

## Project Overview
This project explored the Wine Quality (Red Wine) dataset to demonstrate the full data mining process: data preprocessing, exploratory analysis, feature engineering, regression and classification modeling, clustering, and association rule mining.  

The goal was to derive meaningful insights, evaluate predictive models, identify patterns, and provide actionable recommendations based on real-world data.

---

## Dataset Summary
- **Name:** Wine Quality (Red)  
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)  
- **Instances:** 1,598 (after cleaning)  
- **Attributes:** 11 physicochemical features + quality score  
- **Justification for Selection:**  
  - Rich numeric dataset suitable for regression and classification.  
  - Adequate size (>500 records) for statistical analysis and modeling.  
  - Features reflect real-world wine characteristics relevant to quality assessment.

---

## Data Preparation and Feature Engineering
- **Cleaning:** Removed duplicates and outliers using Z-score thresholding.  
- **Exploratory Analysis:**  
  - Investigated distributions, correlations, and feature relationships.  
  - Identified skewed variables and potential outliers.  
- **Feature Engineering:**  
  - Interaction: `alcohol * citric acid`  
  - Ratio: `free sulfur dioxide / total sulfur dioxide`  
  - Polynomial: `volatile acidity²`  
- **Insight:** Engineered features improved model predictive performance and captured non-linear relationships.

---

## Regression Modeling
- **Models:** Linear Regression, Ridge, Lasso  
- **Evaluation Metrics:** RMSE, MSE, R², cross-validation  
- **Key Observations:**  
  - Ridge regression performed best (R² ≈ 0.37, RMSE ≈ 0.64).  
  - Alcohol and volatile acidity are strong predictors of wine quality.  
  - Feature engineering contributed to better predictive accuracy.  

---

## Classification Modeling
- **Models:** Decision Tree, KNN, Tuned KNN  
- **Evaluation Metrics:** Accuracy, F1 score, Confusion Matrix, ROC Curve  
- **Key Findings:**  
  - Tuned KNN achieved highest accuracy (~0.75) and F1 score (~0.73).  
  - Decision Tree prone to overfitting but provides interpretability.  
  - Normalization improved KNN performance significantly.

---

## Clustering Analysis
- **Model:** K-Means (3 clusters)  
- **Insights:**  
  - Natural clusters largely defined by alcohol and volatile acidity.  
  - Higher alcohol wines tended to cluster together, aligning with higher quality.  
  - Clustering complements predictive models by revealing natural groupings.

---

## Association Rule Mining
- **Method:** Apriori algorithm on quantile-binned features  
- **Findings:**  
  - Wines with high alcohol frequently coincide with low volatile acidity.  
  - Certain acidity and sulfur dioxide combinations strongly associated with quality.  
  - Real-world application: guides production, quality control, and process adjustments.

---

## Practical Recommendations
1. Monitor alcohol and volatile acidity levels to maintain quality.  
2. Use predictive models to automate quality assessment during production.  
3. Apply clustering insights for product segmentation and targeted marketing.  
4. Utilize association rules to optimize chemical composition for desired wine characteristics.

---

## Ethical Considerations
- **Data Privacy:** Dataset contains no personal or sensitive information.  
- **Fairness & Bias:** Dataset may reflect regional production or chemical constraints, introducing implicit biases.  
- **Mitigation Steps:**  
  - Transparent reporting of model limitations.  
  - Avoided overfitting and ensured cross-validation for generalization.  

---

## Visualizations
- Feature distributions, boxplots, and correlation heatmaps from EDA.  
- Actual vs Predicted plots for regression models.  
- Confusion matrices and ROC curves for classification models.  
- K-Means cluster scatterplots for alcohol vs volatile acidity.  
- Top association rules visualized with lift and support metrics.  

---

## Key Takeaways
- Data preprocessing and feature engineering are critical for improving predictive accuracy.  
- Ridge regression and tuned KNN models provide strong predictive performance.  
- Clustering and association rule mining offer actionable insights beyond standard modeling.  
- Predictive and descriptive analytics combined enable informed production and quality decisions.  

---

## Next Steps / Future Improvements
- Explore more advanced predictive models: Random Forest, Gradient Boosting.  
- Consider classification of wine quality into multiple categories for more granular insights.  
- Conduct further feature selection or dimensionality reduction (PCA) to improve model efficiency.  
- Validate findings with additional datasets from other wine regions for generalizability.

---

## References
- [UCI Machine Learning Repository — Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)  
- Pedregosa et al., *Scikit-learn: Machine Learning in Python*, 2011  
- Tan, Steinbach, Kumar, *Introduction to Data Mining*, 2nd Edition  
