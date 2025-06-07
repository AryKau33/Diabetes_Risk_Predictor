# Diabetes_Risk_Predictor
This project is an attempt at using Ensemble Learning with models like Random Forest, Gradient Boosting, eXtreme Gradient Boosting(xgb) and Light Gradient Boosting Machine (LGBM), then cross-validating the final result to predict the risk class of a person(Normal,Overweight class-I/II etc.) which is a huge precursor in determining diabetes risk.
Source: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Obesity+Levels+Detection) This is the dataset.
- Target variable: `NObeyesdad` (obesity category)
- Features include:
  - Gender, Age, Height, Weight
  - Eating habits, activity level, family history, etc.

    Tech Stack used:-
    i)Python(NumPy,Pandas,MatPlotLib)
    ii)XGBoost,LightGBM(gradient boosting methods for ensemble learning)
    iii)Seaborn(for heatmap visualization)

    We preprocess the data, for labelling and encoding(converting unreadable strings to 0 and 1 for the models to process).
    Afterward, we train the data on Random Forest, XGBoost and LightGB models, which we then bring together using the Voting Classifier(soft, which gives us the average of all probabilities put forward by each model). Then we evaluate using confusion matrix and cross-validation(5-fold) to enhance the results.
