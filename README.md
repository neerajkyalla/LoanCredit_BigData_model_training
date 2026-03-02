#  Loan/Credit Risk: End-to-End Big Data Project

This project is now mapped to a loan/credit classification dataset and runs an end-to-end Spark + ML workflow.

## Dataset used
Primary source (UCI):
- `[https://archive.ics.uci.edu/static/public/27/data.csv](https://microsoft.github.io/r-server-loan-credit-risk/input_data.html)`

Local sample copy used for reproducible runs:
- `data/raw/uci_credit_approval.csv`


## Run
```bash
python3 src/run_project.py
```



## Generated outputs
- `data/processed/fact_loans/` (validated parquet, partitioned)
- `data/processed/loan_features/` (feature parquet, partitioned)
- `data/models/spark_*` (Spark MLlib models)
- `data/models/*.pkl` (scikit-learn baselines)
- `data/outputs/project_summary.json` (run metadata + key metrics)
- `data/outputs/dashboard1_data_quality_pipeline_monitoring.csv`
- `data/outputs/dashboard2_model_performance_feature_importance.csv`
- `data/outputs/dashboard3_business_insights_recommendations.csv`
- `data/outputs/dashboard4_scalability_cost_analysis.csv`
- `data/outputs/test_predictions_for_storytelling.csv`
- `data/outputs/spark_ui/` (Spark event logs)

## Tableau dashboards (build from outputs)
1. Data quality and pipeline monitoring: dashboard 1 CSV
2. Model performance and runtime comparison: dashboard 2 CSV
3. Business metrics and recommendations: dashboard 3 CSV + predictions CSV
4. Scalability and cost analysis: dashboard 4 CSV

## Practical interpretation
- This is a loan/credit approval classification setup (`A16` mapped to binary target).
- Spark and sklearn models are compared on AUC/accuracy/training time.
- Business metrics use a simple lending economics proxy to translate confusion matrix into expected profit.
