# Gym Weight Goal Achievement Prediction using Logistic Regression

## Activity 2 – Regression and Classification Algorithms (CIE 2)

**Student Name:** Rudrapratap Therokar  
**Roll Number:** AD3343  
**Class/Division:** AIDS C  
**Submission GitHub ID:** https://github.com/complexiota

**PROJECT GITHUB LINK:** https://github.com/ftw-rudra/RCA-Activity-2-AD-3343-



## 1. Project Overview

This project uses **Logistic Regression** to predict whether a gym member achieves their fitness goal based on workout habits, calories burned, and sleep hours. The activity demonstrates binary classification using numerical input features.

## 2. Problem Statement

Predict whether a gym member achieves their fitness goal using:

- **Workouts per Week** – number of workout sessions in a week
- **Average Workout Minutes** – average duration of a workout
- **Daily Calories Burned** – estimated calories burned per day
- **Sleep Hours** – average hours of sleep

**Target:** `goal_achieved`

- `1` – Goal achieved
- `0` – Goal not achieved

## 3. Dataset

This activity uses a **synthetic dataset** created for learning and demonstration. It contains 500 records and five columns.

| Column | Description | Type |
|---|---|---|
| `workouts_per_week` | Number of workouts per week | Numerical input feature |
| `avg_workout_minutes` | Average duration of each workout in minutes | Numerical input feature |
| `daily_calories_burned` | Estimated calories burned per day | Numerical input feature |
| `sleep_hours` | Average hours of sleep | Numerical input feature |
| `goal_achieved` | Whether the member achieved the goal (0 or 1) | Binary target |

The dataset is provided in `Dataset_gym.csv` in this repository. Since the data is synthetic, it is intended for educational use only. It does not represent real gym members and should not be used for real health or fitness decisions.

## 4. Tools and Libraries

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 5. Activity Steps

1. Load the dataset and inspect sample records and dataset information.
2. Check for missing values and examine the distribution of the target classes.
3. Visualise class counts and feature correlations.
4. Understand the sigmoid function used in Logistic Regression.
5. Separate the input features and binary target.
6. Split the data into training and testing sets using stratification.
7. Standardise the features using `StandardScaler`, fitting the scaler only on the training data.
8. Train a Logistic Regression model and inspect its intercept and feature coefficients.
9. Generate predicted probabilities and class labels.
10. Compare decision thresholds of 0.3, 0.5, and 0.7 using accuracy, precision, recall, and F1-score.
11. Compare the model with a majority-class baseline.
12. Evaluate the model using a confusion matrix, classification report, specificity, ROC curve, and ROC-AUC.
13. Plot decision behaviour and make a prediction for a new gym-member example.

## 6. Logistic Regression Equation

The sigmoid function is:

`P(y = 1) = 1 / (1 + e^-(b0 + b1*x1 + b2*x2 + b3*x3 + b4*x4))`

Where:

- `P(y = 1)` = predicted probability that the goal is achieved
- `b0` = intercept
- `b1, b2, b3, b4` = feature coefficients
- `x1, x2, x3, x4` = input features

The model converts the linear combination of input features into a probability between 0 and 1. A decision threshold is then used to convert the probability into a predicted class. The fitted intercept and coefficients are obtained from the notebook.

## 7. Evaluation Metrics

- **Accuracy:** Proportion of all predictions that are correct.
- **Precision:** Proportion of predicted positive cases that are actually positive.
- **Recall:** Proportion of actual positive cases correctly identified.
- **F1-score:** Harmonic mean of precision and recall.
- **Specificity:** Proportion of actual negative cases correctly identified.
- **Confusion Matrix:** Shows true positives, true negatives, false positives, and false negatives.
- **ROC-AUC:** Measures how well the model distinguishes between the two classes across different thresholds.

The notebook also compares the results at thresholds **0.3, 0.5, and 0.7**, and checks the model against a majority-class baseline. Run the notebook to view the actual metric values; no evaluation values are assumed in this README.

## 8. New Prediction

The notebook tests the trained model using a new example gym-member record:

- Workouts per week: `5`
- Average workout minutes: `60`
- Daily calories burned: `400`
- Sleep hours: `8`

The notebook displays the predicted probability and the corresponding class. The result should be read as a model prediction based on synthetic training data, not as a reliable assessment of an individual's fitness outcome.

## 9. Conclusion

This activity demonstrates how Logistic Regression can be used for binary classification. The model uses workout frequency, workout duration, calories burned, and sleep hours to estimate the probability of achieving a fitness goal. Stratified splitting, feature scaling, threshold comparison, and classification metrics are used to understand model performance.

Because the dataset is synthetic, the model is suitable for learning the classification workflow only. Its predictions should not be interpreted as evidence of cause and effect or used for real-world health and fitness decisions.

## 10. Repository Files

- `Dataset_gym.csv` – synthetic dataset used for the activity
- `AD3343_RCA_Activity_2.ipynb` – notebook containing the code, visualisations, model training, evaluation, and new prediction
- `README.md` – project description and activity summary

## How to Run

1. Open `AD3343_RCA_Activity_2.ipynb` in Google Colab.
2. Upload `Dataset_gym.csv` to the Colab working directory.
3. Check that the filename in the notebook's `pd.read_csv()` statement matches `Dataset_gym.csv`.
4. Run all notebook cells from top to bottom.
5. Review the printed evaluation metrics, plots, and new prediction.

---

**Note:** Keep the notebook's CSV filename and the dataset filename in this repository the same. Add the notebook and CSV file to the public GitHub repository before submitting the repository URL.
