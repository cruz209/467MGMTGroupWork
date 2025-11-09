Flight Diversion Prediction Model B – Summary
Nayan Nair

What I Learned
This project built two logistic regression models in BigQuery ML to predict U.S. flight diversions using 2015 data. The first model used basic features (delay, distance, carrier, origin, destination), while the improved version added route combinations, delay categories, and time-based features. Key lessons included using proper CTE structure, setting up 80/20 train-test splits with RAND(), and evaluating results with both ML.EVALUATE and custom confusion matrices. The engineered model slightly improved ROC AUC (0.72 → 0.75) and reached perfect precision (1.0) but had very low recall (0.19%), showing the tradeoff between precision and recall in imbalanced data.

Where the Model Failed
The models failed to detect diverted flights due to extreme class imbalance (only 0.27% diverted). Both had ~99.7% accuracy, mostly predicting “no diversion” and missing nearly all true diversions. The available features lacked useful signals—real diversions are often caused by weather, mechanical, or air traffic issues not captured in the dataset. Technical hurdles included CTE placement errors and schema mismatches during evaluation. At higher thresholds (0.75), the model made no positive predictions at all.

Recommended Deployment Threshold
This model should be used for research or monitoring a lower threshold (0.15–0.25) that could improve recall to 5–15%, helping flag higher-risk flights for review. In aviation, missing diversions (false negatives) are far riskier than false alarms. For future improvement, the model needs better class balancing, new features (weather, maintenance, airport data), and possibly ensemble or anomaly detection methods—aiming for at least 40% recall and 10% precision with human oversight.