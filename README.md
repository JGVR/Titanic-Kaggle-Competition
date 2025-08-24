# Titanic Kaggle Competition 🚀
## Description 📝
- Please go to the following link for the description of the competition: [Titanic-Kaggle](www.kaggle.com/competitions/titanic/overview/description)
## Citation
- Cukierski, W. (2012). *Titanic — Machine Learning from Disaster* [Competition]. Kaggle. <https://www.kaggle.com/competitions/titanic>. Accessed 2025-08-24.

## Approach 🧠
- First step is to get familiar with the datasets provided, what are the dimensions of our dataset, which columns have missing values (NaNs).
- Second is to analyze the dataset in order to engineered features that can boost the accuracy of the model. I'm going to create the following features:
  1. Class_group: A categorical column with the following values: (upper, middle, lower) representing the socio-economic class of each passenger.
  2. Age_group: A categorical column with the following values: (young, middle, old) representing the age group a passenger belongs to
  3. Survival_rate: A probability stat representing the odds a passenger survived. This is calculated by utilizng class_group, age_group, and gender columns. I believe a passenger socio-economic class, age and gender played a major role in their survival.
  4. Group_size: The size of the group for which the survival_rate was calculated. The survival_rate by itself can be misleading because one group can be significantly smaller that others and hold a higher survival_rate.
- Third, I will normalize the features utilizing z-score normalization to ensure all features are close in range. This should prevent the model giving higher importance to features with higher range of values.
- Finally, I will create 2 different models to create the predictions:
  1. Fully Connected Neural Network (Dense)
  2. RandomForestClassifier - I haven't implemented this one as of yet, but I'm planning to do so later on.

## Results 📊
- My top submission puts me in the top 800 (789) of the leaderboard. This is a rolling leaderboard so it can change at any time.

## Tech Stack 💻
- Python
- Pandas, numpy, Matplotlib - for data analysis, transformation and visualization.
- Tensorflow & Keras - for the Neural Network model.
- Jupyter Lab

## Installation 🖥️
- ### Virtual Environment Set-up
1. Let's set-up a python virtual environment by running the command below:
   ```bash
   python3.12 -m venv /path/to/new/virtual/environment
   ```
2. Activate your virtual environment.
   ```bash
   source /path/to/new/virtual/environment/bin/activate
   ```
3. Run the following command to install all the packages inside the requirements.txt file:
   ```bash
   pip install -r requirements.txt
   ```

## Usage 🔥
- Everything was wrote with jupyter lab. To lunch jupyter lab and inspect the appropriate notebooks, please run the command below:
```bash
jupyter lab
```
- There are 2 notebooks:
    1. The dataset_analysis.ipynb - This notebook contains the initial Exploratory Data Analysis, and the creation of the engineered features
    2. The training_analysis.ipynb - This notebook contains all dataset transformation logic, plots, the ML models and predictions.
