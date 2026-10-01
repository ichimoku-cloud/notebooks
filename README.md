# My Notebooks

A set of notebooks I use as a reference for analysis across games, SaaS, tech and medicine. Each one works through a real business question from raw data to a decision, and explains the reasoning along the way.

## Getting started

```bash
pip install -r requirements.txt
jupyter notebook
```

Every notebook runs top to bottom with nothing to download, and they're saved with their outputs so you can read them on GitHub without running anything.

## The notebooks

If you're new to this, start with the two foundations notebooks. The rest can be read in any order.

**Foundations**
- `statistics_for_analysts` covers averages vs. medians, confidence intervals, p-values and Simpson's paradox.
- `ml_foundations_overfitting` shows how models overfit, and how cross-validation and regularisation catch it.

**SaaS**
- `saas_metrics_and_cohorts` builds MRR, churn, cohort retention and unit economics from billing data.
- `saas_churn_prediction` predicts which accounts will cancel and decides who to target by expected profit.

**Games**
- `game_engagement_and_retention` covers DAU, retention, the onboarding funnel and monetisation.
- `game_ab_testing` analyses a feature test properly, including sample sizes and the peeking problem.
- `game_player_segmentation` groups players by behaviour with clustering.

**Medicine**
- `medicine_diagnosis_classifier` builds a cancer classifier and chooses a threshold the way a clinician would.
- `medicine_clinical_trial_survival` covers survival curves and hazard ratios for a two-arm trial.

**Tech**
- `tech_traffic_forecasting` forecasts website traffic and backtests the forecast.
- `tech_anomaly_detection` catches incidents in server metrics without drowning the on-call team in false alarms.

## About the data

Real data from games, SaaS companies and clinical trials is rarely public, so most notebooks use simulated data from `sample_data.py`. Each dataset has a few known effects built in, like one acquisition channel churning twice as fast. That's useful for learning: you can check whether the analysis finds the truth.

Two notebooks use real data. The diagnosis classifier uses the Wisconsin breast cancer dataset that ships with scikit-learn, and the statistics notebook uses published results from a 1986 kidney stone study.
