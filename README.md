# IPL_match
📌 Project Overview

This project focuses on exploratory data analysis (EDA) and machine learning-based prediction using historical data from the Indian Premier League dataset.

The system analyzes team and player performances, uncovers key cricket patterns, and builds predictive models to estimate match outcomes.

📂 Dataset Description

The project uses two main datasets:

1. Matches Dataset

Contains match-level information:

Match ID
Season
Teams
Toss winner
Match winner
Venue
Result details
2. Deliveries Dataset

Ball-by-ball data:

Match ID
Batsman
Bowler
Runs scored
Wickets
Extras
Over details
🧹 Data Preprocessing Steps
1. Handling Missing Values
Removed or filled missing values in:
winner
city
player_of_match
Replaced NaN in categorical fields with "Unknown"
2. Data Cleaning
Standardized team names (e.g., DD → Delhi Capitals, if required)
Removed inconsistent or duplicate records
Ensured correct mapping between match_id in both datasets
3. Feature Engineering

Created new features:

Total runs per match
Wickets per bowler
Strike rate = runs / balls × 100
Team wins per season
Toss impact feature
4. Merging Datasets
deliveries = deliveries.merge(matches[['id','season']], left_on='match_id', right_on='id')
📊 Exploratory Data Analysis (EDA)
🏆 Team Performance Analysis
Total matches played per team
Win percentage per team
Toss vs match win correlation
🏏 Batting Analysis
Top run scorers
Strike rate comparisons
Boundaries (4s & 6s) distribution
Batsman consistency trends
🎯 Bowling Analysis
Top wicket takers per season (Purple Cap analysis)
Economy rate analysis
Death over bowling performance
📅 Season-wise Insights
Total runs per season
High-scoring matches (200+ runs)
Match intensity over years
📌 Key Insights
Some teams show strong dominance in specific seasons
High scoring matches are increasing over time
Certain bowlers consistently perform in death overs
Toss decision has a moderate impact on winning probability
🤖 Predictive Modeling Approach
🎯 Objective

Predict whether a team will win a match based on match conditions.

🧠 Algorithms Used
1. Logistic Regression
Used for binary classification (Win/Loss)
Works well for interpretable outcomes
Outputs probability of winning
2. Random Forest Classifier
Ensemble method using multiple decision trees
Handles non-linear relationships
Reduces overfitting
Higher accuracy than logistic regression
📌 Features Used for Prediction
Team1
Team2
Toss winner
Toss decision (bat/field)
Venue
Season
Previous win rate
⚙️ Model Workflow
Encode categorical variables (Label Encoding / One-Hot Encoding)
Split dataset into train/test sets
Train models:
Logistic Regression
Random Forest
Evaluate using:
Accuracy score
Confusion matrix
Precision & Recall
📈 Model Evaluation
Model	Accuracy
Logistic Regression	~70–75%
Random Forest	~75–85%
📊 Visualization Tools Used
Matplotlib → basic plots
Seaborn → statistical plots
Plotly → interactive dashboards

Examples:

Team wins bar chart
Purple cap visualization
Strike rate comparison plots
Season-wise trend analysis
🧠 Key Findings
Teams with strong batting depth perform better in high-scoring matches
Winning toss provides slight advantage when choosing to field
Consistent bowlers significantly influence match outcomes
IPL has become more batting-friendly over the years
🚀 Future Improvements
Add deep learning model (LSTM for match sequence prediction)
Player form tracking system
Real-time match prediction dashboard
Integration with live IPL API data
🏁 Conclusion

This project demonstrates how data science techniques can be applied to cricket analytics to:

Understand team and player performance
Identify hidden patterns in IPL matches
Predict match outcomes using machine learning
