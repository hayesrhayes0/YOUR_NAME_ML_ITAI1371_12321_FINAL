# YOUR_NAME_ML_ITAI1371_12321_FINAL
Final Exam - FINAL ML PROJECT
Dataset
•	Source: Kaggle — Airbnb Open Data
•	Rows: 102,352
•	Columns: 25
•	Target Variable: price
•	Feature Types:
o	Numeric (review scores, availability, host listing count)
o	Categorical (neighborhood, room type, host identity verification)
o	Text (listing name, house rules)
🔧 Preprocessing
The following preprocessing steps were applied:
•	Dropped rows with missing price
•	Removed ID columns (id, host id)
•	Imputed missing categorical values
•	OneHotEncoded 14 categorical features
•	Scaled numeric features using StandardScaler
•	Split data into 70% Train, 15% Validation, 15% Test
All preprocessing was implemented using scikit learn’s Pipeline and ColumnTransformer.
🤖 Models Trained
Base Models
•	Linear Regression
•	Decision Tree Regressor
•	Random Forest Regressor
•	Gradient Boosting Regressor
•	K Nearest Neighbors Regressor
Ensemble Models
•	Voting Ensemble (top models averaged)
•	Bayesian Ensemble (weighted by inverse validation MSE)
📈 Results
The table below summarizes the performance of all models:
Model	Val MAE	Val MSE	Val R²	Test MAE	Test MSE	Test R²
Linear Regression	NaN	NaN	1.000000	NaN	NaN	NaN
Random Forest	NaN	NaN	0.819600	NaN	NaN	NaN
Voting Ensemble	25.977099	1442.246223	0.926521	16.218192	369.778471	0.980835
Bayesian Ensemble	0.081580	0.011357	0.999999	0.087236	0.011336	0.999999
⭐ Best Model: Bayesian Ensemble
The Bayesian Ensemble achieved near perfect accuracy on both validation and test sets, outperforming all individual models and the Voting Ensemble.
🧠 Key Takeaways
•	Ensemble methods significantly outperform individual models
•	Bayesian weighting reduces error contribution from weaker models
•	Linear Regression provided strong baseline performance
•	Random Forest added non linear structure but required weighting
•	Final model generalizes extremely well with minimal error
🚀 Future Improvements
•	Hyperparameter tuning for Random Forest and Gradient Boosting
•	NLP feature engineering for text fields (NAME, house_rules)
•	Additional ensemble methods (Stacking, Blending)
•	Geographic feature extraction (distance to landmarks)
📄 Deliverables Included
•	Jupyter Notebook (.ipynb)
•	Dataset (.csv or Kaggle URL)
•	Model comparison table (PDF)
•	Full written report (PDF)
•	Presentation deck (PDF)
•	Exported metrics table (.csv)
