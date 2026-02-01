# Kaggle-st
This repository contains my solution for a Kaggle regression competition focused on predicting student exam scores using academic, behavioral, and environmental features.

The project covers the complete machine learning pipeline:

Data preprocessing

Feature engineering

Categorical encoding

Gradient boosting models (LightGBM, XGBoost)

Model ensembling

Submission generation

This was my first Kaggle competition, and the main goal was to gain hands-on experience with real-world ML workflows.

📂 Dataset

The dataset consists of student-level information.

Features

Numerical

age

study_hours

class_attendance

sleep_hours

Categorical

gender

course

study_method

sleep_quality

facility_rating

internet_access

exam_difficulty

Target

exam_score

🛠 Feature Engineering

To improve model performance, additional features were created:

🔹 Environment Score

Represents overall learning conditions:

environment_score =
study_method_mean +
sleep_quality_mean +
facility_rating_mean

🔹 Interaction Feature

Captures nonlinear relationships between study behavior and environment:

attendance_sleep_env_study_score =
class_attendance × sleep_hours × environment_score × study_hours


Correlation analysis showed this feature had a strong relationship with the target.

🔄 Encoding Techniques

Target Encoding

study_method

sleep_quality

facility_rating

course

Ordinal Encoding

gender

internet_access

exam_difficulty

These encodings were applied consistently to both train and test datasets.

🤖 Models

LightGBM Regressor

XGBoost Regressor (experiments)

🔁 Ensembling

Trained multiple LightGBM models with different hyperparameters

Final predictions obtained by averaging model outputs

This reduced variance and improved stability

📈 Evaluation

Metric used: RMSE

Public and private leaderboard scores were analyzed to understand generalization.

Final Result

Top ~27% on the leaderboard
