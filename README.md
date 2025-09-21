# NBA Game Outcome Predictor

A program that attempts to predict the outcome of NBA games using historical data and machine learning.
The model was trained on **26,651 NBA games** between 2004–2018 using a subset of home team statistics.  
This project applies **Logistic Regression** to determine whether the **home team** wins or loses.

**Accuracy of Program:** ~76%  
**Key Finding**: *Field Goal (%)* happened to be the strongest predictor of a win, while assists contributed the least.*

## Overview
- Data exploration  
- Preprocessing (handling missing values)  
- Feature selection  
- Model training & evaluation  
- Visualization of results

## Workflow
1. **Data**  
   - Load 26,651 games from CSV  
2. **Define Targets and Features**  
   - Target: HOME_TEAM_WINS (1=Win, 0=Loss)
   - Select relevant home team features (PTS, REB, AST, FG%, FT%, 3PT%).  
3. **Data Cleaning**  
  -Handle 99 missing values with mean imputation
  -Restore DataFrame structure
4. **Train/Test Split**  
  -80% training (21,320 games)
  -20% testing (5,331 games)
5. **Model Training and Prediction**  
  -Train logistic regression
  -Make predictions on test set
6. **Performance Evaluation**
   -Calculate 76.08% accuracy
  -Generate detailed metrics

## Results
- **Accuracy:** ~76%  
- **Insights:**  
  - Field Goal % (FG%) was the most important stat driving wins.  
  - Assists (AST) contributed the least.

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
Install all required packages from requirements.txt:
```bash
pip install -r requirements.txt
```
### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```
### 5. Open the notebook
notebooks/nba_win_predictor.ipynb
