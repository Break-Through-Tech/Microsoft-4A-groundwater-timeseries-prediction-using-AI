# Groundwater Time-Series Forecasting Using AI

**Industry Partner:** Microsoft  
**Program:** Break Through Tech AI Studio | Fall 2026  
**Project:** Microsoft 4A – Groundwater Level Prediction


---

### 👥 **Team Members**

**Example:**

| Name             | GitHub Handle        | Contribution                                                             |
|------------------|----------------------|--------------------------------------------------------------------------|
| Ashton Shen      | @xxashtonshen        | Data exploration, visualization, overall project coordination            |
| Sahara Smith     | @saharadoesdev       | Data collection, exploratory data analysis (EDA), dataset documentation  |
| Aanya Bharti     | @aanyabharti101      | Time-series EDA, 30-/90-day rolling statistics, visualization, LSTM/XGBoost experiments, model evaluation |
| Hafsa Akhter     | @hafsaakhter-creator | Model selection, hyperparameter tuning, model training and optimization  |

---

## 🎯 **Project Highlights**

Developed and compared LSTM and XGBoost models to forecast groundwater levels 7 days ahead as part of Microsoft's industry-sponsored challenge through Break Through Tech AI Studio.
Improved XGBoost test RMSE from 2.4070 m to 0.7938 m in one experiment, demonstrating how different forecasting approaches can improve predictive performance.
Identified groundwater trends, seasonality, and variability through temporal data analysis, generating insights that could support environmental monitoring and data-driven decision-making.
Applied temporal feature engineering, chronological data splitting, and baseline model comparisons to evaluate forecasting reliability and address the challenges of real-world groundwater time-series data.

---

## 🧑‍💻 Setup and Installation

### Clone the Repository

```bash
git clone https://github.com/Break-Through-Tech/Microsoft-4A-groundwater-timeseries-prediction-using-AI.git
cd Microsoft-4A-groundwater-timeseries-prediction-using-AI
```

### Create a Python Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows, activate the environment using:

```powershell
.venv\Scripts\Activate.ps1
```

### Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### Run the Notebook

Open the project notebook:

`notebooks/Microsoft_4A.ipynb`

Execute the cells in order to reproduce the data exploration, forecasting experiments, and available evaluation results.

### Data

The repository's `data/` directory contains regional GROW dataset subsets used in the project.

Confirm that notebook data paths point to the appropriate files before executing the analysis.

---

## 🏗️ **Project Overview**

**Describe:**
Groundwater is an essential resource for drinking water, agriculture, and ecosystems. Predicting changes in groundwater levels is challenging because measurements vary over time and across geographic locations.
Through Break Through Tech AI Studio, our team partnered with Microsoft to explore how machine learning can improve groundwater-level forecasting.
Using the GROW groundwater dataset, we investigated time-series patterns and developed forecasting approaches to predict groundwater levels seven days into the future.
Our project explores LSTM neural networks, XGBoost, and baseline forecasting methods, with an emphasis on exploratory data analysis, preprocessing, temporal feature engineering, and model evaluation.
The broader goal is to understand how AI-based forecasting can support more informed groundwater monitoring and environmental decision-making.

---

## 📊 **Data Exploration**

**You might consider describing the following (as applicable):**
We use regional subsets of the GROW groundwater dataset, which contains time-series observations of groundwater depth and elevation.

Source: https://zenodo.org/records/15149480

Data files in this repository include:
- `nld_regional_105_wells_2012_2022.csv`
- `svn_regional_53_wells_daily_2019_2023.csv`
- `preprocessed_daily_dataset.csv`

### Exploratory Data Analysis

Our exploratory analysis investigated groundwater-level behavior across time and geographic regions.

Methods included:
- Visualizing groundwater levels over time
- Calculating 30-day and 90-day rolling means
- Examining rolling standard deviations
- Comparing temporal patterns between groundwater wells
- Investigating trends, seasonality, and variability

These analyses helped us understand the structure of the data and prepare for forecasting experiments.

### Visualizations

Exploratory plots and model visualizations are available in our [project notebook](notebooks/Microsoft_4A.ipynb)
---

## 🧠 **Model Development**

**You might consider describing the following (as applicable):**

* Model(s) used (e.g., CNN with transfer learning, regression models)
* Feature selection and Hyperparameter tuning strategies
* Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)

We experimented with multiple approaches for forecasting groundwater levels.

### Forecasting Models

**LSTM (Long Short-Term Memory)**
A recurrent neural network architecture designed to model temporal dependencies in sequential observations.

**XGBoost**
A gradient-boosted decision tree model used to investigate an alternative approach to groundwater forecasting.

**Persistence Baseline**
A simple forecasting reference used to evaluate whether more complex models provide meaningful improvements.

### Forecasting Setup
- Input: 30 days of historical groundwater observations
- Forecast horizon: 7 days
- Evaluation: RMSE and MAE
- Data splitting: Chronological training, validation, and test sets

We also experimented with predicting changes in groundwater levels rather than absolute elevations, allowing us to compare different target formulations.

---

## 📈 **Results & Key Findings**

**You might consider describing the following (as applicable):**

* Performance metrics (e.g., Accuracy, F1 score, RMSE)
* How your model performed
* Insights from evaluating model fairness

**Potential visualizations to include:**

* Confusion matrix, precision-recall curve, feature importance plot, prediction distribution, outputs from fairness or explainability tools

### XGBoost Experiment

| Prediction Approach | Test RMSE |
|---|---|
| Absolute groundwater elevation | 2.4070 m |
| Groundwater-level changes | 0.7938 m |

Predicting changes in groundwater levels reduced test RMSE in this experiment.


### Key Findings
- Groundwater observations exhibit temporal trends and varying levels of short-term variability.
- Rolling statistics help visualize changes in groundwater behavior.
- Forecasting performance can depend strongly on how the prediction target is formulated.
- Comparing LSTM, XGBoost, and persistence approaches provides a basis for evaluating different forecasting strategies.

### Model Visualizations
The project notebook includes model evaluation and visualization work, including prediction comparisons and training diagnostics.

See [Microsoft_4A.ipynb](notebooks/Microsoft_4A.ipynb).



---

## 🚀 **Next Steps**
**You might consider addressing the following (as applicable):**

* What are some of the limitations of your model?
* What would you do differently with more time/resources?
* What additional datasets or techniques would you explore?

---

## 📝 **License**

A project license has not yet been finalized. Reuse and redistribution permissions should be confirmed with the Challenge Advisor before a license is added.

## 📄 References

- [GROW Dataset](https://zenodo.org/records/15149480)
- [Groundwater Dataset Research Paper](https://www.nature.com/articles/s41597-026-06966-1)
- [LSTM Background Reading](https://arxiv.org/pdf/1909.09586)

## 🙏 Acknowledgements

We thank Microsoft and Break Through Tech AI Studio for providing the opportunity to work on this industry-sponsored groundwater forecasting challenge.

Special thanks to our Microsoft Challenge Advisor, Aarti Dwivedi, and Break Through Tech AI Coach, Alexandra Ladyzhensky, for their guidance and support.


