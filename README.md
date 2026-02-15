# NBA Game Outcome Predictor

A machine learning projects that predicts the outcome of NBA games (home win or loss) using historical game data.
The model is trained on **26,651 NBA games** from the 2004–2018 seasons with a focus on a subset of home team statistics.  
This project applies **Logistic Regression** to determine whether the **home team** wins or loses.

**Model Accuracy:** ~76%  
**Key Insight**: *Field Goal (%)* happened to be the strongest predictor of a win, while assists contributed the least.

## Overview
- Data exploration - inital analysis of the dataset
- Preprocessing - handling missing values 
- Feature selection - choosing relevant statistics for prediction 
- Model training & evaluation - apply logistic regression
- Visualization of results - plotting and interpretation of results

## Workflow
1. **Data**  
   - Loaded 26,651 games from (2004-2018 season) using a CSV dataset.
2. **Define Targets and Features**  
   - Target: HOME_TEAM_WINS (1=Win, 0=Loss)
   - Selected relevant home team features (PTS, REB, AST, FG%, FT%, 3PT%).  
3. **Data Cleaning**  
   - Handled 99 missing values with mean imputation
   - Restored DataFrame structure
4. **Train/Test Split**  
   - 80% training (21,320 games)
   - 20% testing (5,331 games)
5. **Model Training and Prediction**  
   - Trained logistic regression
   - Made predictions on test set
6. **Performance Evaluation**
   - Calculated the models accuracy using the test data (76.08%)
   - Generated detailed metrics

## Results
- **Accuracy:** The logistic regreession model achieved approximately 76% accuracy in predicting game outcomes on the test set.  
- **Insights:**  
  - Field Goal % (FG%) was the most important/influential feature for predicting a home win.  
  - Assists (AST) contributed the least in other words the least predictive feature in the model.

## ⚙️ Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/cwinglai/NBA-Game-Outcome-Predictor.git
cd NBA-Game-Outcome-Predictor
```
### 2. Create Virtual Environment
```bash
conda create -n nba-ml python=3.10
conda activate nba-ml
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```
### 5. Open the Notebook
Using the jupyter interface, open the notebook @ notebooks/nba_win_predictor.ipynb to view the analysis and run the code cells.

## 🙏 Credits
- **Dataset:** NBA Games (2004–2018) dataset by [Nathan Lauga on Kaggle](https://www.kaggle.com/datasets/nathanlauga/nba-games).  
- **Libraries:** [pandas](https://pandas.pydata.org/), [numpy](https://numpy.org/), [matplotlib](https://matplotlib.org/), [scikit-learn](https://scikit-learn.org/). 
