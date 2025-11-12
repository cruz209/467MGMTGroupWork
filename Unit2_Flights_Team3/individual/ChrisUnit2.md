Flight Diversion Prediction Model – Summary
What I Learned
This project involved building and evaluating two logistic regression models in BigQuery ML to predict U.S. flight diversions. The baseline model used fundamental features like dep_delay, distance, carrier, origin, and dest. The engineered model, built with TRANSFORM, introduced more sophisticated features such as route (origin-dest combination), day_of_week, and dep_delay_bucket (categorized departure delays). Key lessons included correctly structuring WITH clauses for BigQuery ML models, implementing data splits using RAND(), and comprehensively evaluating model performance using ML.EVALUATE and custom confusion matrices based on cost analysis. The engineered model demonstrated an improved ROC AUC of 0.759 compared to the baseline's 0.713, indicating better overall discriminative power.

Where the Model Failed
Both models struggled significantly with detecting actual diverted flights due to extreme class imbalance in the dataset. At the default 0.5 threshold, the baseline model achieved ~99.7% accuracy but had 0 precision and 0 recall for the positive class (diverted flights), effectively predicting 'no diversion' for every flight. While the engineered model showed some improvement, achieving a precision of 0.295 and a recall of 0.007 (0.7%) at the 0.5 threshold, it still missed the vast majority of actual diversions. The features available in the dataset likely lack the crucial signals (e.g., real-time weather, mechanical issues, air traffic control congestion) that are primary causes of diversions. Technical hurdles encountered during development included persistent SQL syntax errors related to WITH clause placement, incorrect RAND() function usage, and column name mismatches in the canonical SQL mapping.

Recommended Deployment Threshold and Operational Policy
Based on the cost analysis, an optimal operating threshold of 0.55 was chosen to minimize total expected costs, given that False Negatives (missed diversions, costing  6,000)aresignificantlymoreexpensivethanFalsePositives(unnecessaryalerts,costing 1,000). At this threshold, the engineered model results in:

True Positives (TP): 24
False Positives (FP): 49
False Negatives (FN): 2969
True Negatives (TN): 1,143,762
This threshold provides $8,000.00 in cost savings compared to the default 0.5 threshold. The rationale is to prioritize avoiding the severe consequences and higher costs associated with failing to predict a necessary diversion, accepting a small increase in 'false alarms' as a trade-off for overall cost efficiency and safety.

Post-Deployment Monitoring: To ensure sustained performance and business impact, key metrics should be continuously monitored:

Actual vs. Predicted Diversion Rates: Track to detect drift in underlying patterns.
Precision and Recall (at 0.55 threshold): Continuously assess the model's ability to identify diversions (recall) while minimizing false alarms (precision).
Total Cost over Time: Monitor actualized total cost to directly assess economic impact.
Performance by Carrier/Route: Segment metrics to identify localized performance issues.
Feature Importance Drift: Keep an eye on input features' relevance and distribution for data quality or operational changes.
