# Groundwater Time-Series Forecasting Using AI

**Industry Partner:** Microsoft  
**Program:** Break Through Tech AI Studio | Fall 2026  
**Project:** Microsoft 4A – Groundwater Level Prediction


---

### 👥 **Team Members**


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
Groundwater is an essential resource for drinking water, agriculture, and ecosystems. Predicting changes in groundwater levels is challenging because measurements vary over time and across geographic locations.
Through Break Through Tech AI Studio, our team partnered with Microsoft to explore how machine learning can improve groundwater-level forecasting.
Using the GROW groundwater dataset, we investigated time-series patterns and developed forecasting approaches to predict groundwater levels seven days into the future.
Our project explores LSTM neural networks, XGBoost, and baseline forecasting methods, with an emphasis on exploratory data analysis, preprocessing, temporal feature engineering, and model evaluation.
The broader goal is to understand how AI-based forecasting can support more informed groundwater monitoring and environmental decision-making.

---



## 📊 **Data Exploration**

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





## 🧠 Model Development

We developed and evaluated multiple forecasting approaches to investigate how effectively machine learning can predict groundwater levels **7 days ahead**. 
Our initial experiments focused on a single groundwater well, establishing a foundation for future evaluations across additional wells and environmental conditions.

### Forecasting Models

**LSTM (Long Short-Term Memory)**

We implemented an LSTM neural network to capture temporal dependencies in groundwater observations. The model uses **30 days of historical measurements** to predict groundwater levels for the following seven days.

The architecture includes:
- An LSTM layer with 32 units
- A dense layer with 16 units and ReLU activation
- An output layer producing seven daily predictions

**XGBoost**

We implemented XGBoost, a gradient-boosted decision tree algorithm, as an alternative forecasting method. Using the previous 30 groundwater observations as input features, separate regressors predict each of the next seven days.

We also investigated **predicting changes in groundwater levels rather than absolute elevations**, exploring whether an alternative target formulation could improve accuracy.

**Persistence Baseline**

We established a persistence baseline that assumes the most recently observed groundwater level remains unchanged throughout the next seven days. 
This provides a reference for determining whether more complex models deliver meaningful improvements.

### Feature Engineering and Selection

- Applied a **30-day sliding window** to create training examples with seven-day prediction targets.
- Analyzed temporal trends, potential seasonal patterns, and groundwater variability through exploratory analysis and rolling statistics.
- Examined **XGBoost feature importance** to identify which historical observations contributed most to predictions.
- Initially focused on groundwater-level history as the primary input, providing a baseline for future experiments with additional environmental features.

### Training Setup and Hyperparameters

We divided forecasting examples chronologically into approximately **70% training, 15% validation, and 15% testing**, with gaps between splits to prevent overlapping forecast targets.

For the LSTM, groundwater measurements were standardized using training-set statistics to prevent information leakage.

| Parameter | LSTM | XGBoost |
|---|---|---|
| Input window | 30 days | 30 days |
| Forecast horizon | 7 days | 7 days |
| Architecture / configuration | 32 LSTM units, 16-unit dense layer | 200 trees, maximum depth 3 |
| Learning settings | Adam optimizer, MSE loss | Learning rate: 0.05 |
| Additional settings | Batch size: 32, up to 40 epochs | Subsample: 0.9, column sample: 0.9 |
| Training control | Early stopping (patience: 6) | Fixed initial configuration |

These configurations represent our initial experiments rather than the results of an exhaustive hyperparameter search.

### Model Evaluation

We assessed forecasting accuracy using:

- **Root Mean Squared Error (RMSE):** Measures the magnitude of prediction errors, penalizing larger errors more strongly.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between predicted and observed groundwater levels.

Additional evaluation included:
- Comparing LSTM and XGBoost against the persistence baseline.
- Examining prediction errors across each of the seven forecast days.
- Visualizing **actual versus predicted groundwater levels**.
- Monitoring LSTM training and validation loss.
- Analyzing XGBoost feature importance and alternative prediction targets.

These experiments helped identify promising forecasting approaches and areas for further improvement.




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

## 🚀 Next Steps

Our initial experiments highlight both the potential of machine learning for groundwater forecasting and several opportunities to improve model accuracy, generalization, and reliability.

### Current Limitations

- **Limited geographic coverage:** Initial forecasting experiments focused on one groundwater well. Performance may vary across other wells, regions, and environmental conditions.
- **Limited input features:** Current forecasting models primarily rely on historical groundwater levels without fully incorporating additional environmental variables.
- **Missing observations:** Forecasting windows containing missing groundwater measurements were excluded, reducing the available training data.
- **Model generalization:** Models have been evaluated using chronological splits from one well; additional testing is needed to assess performance across independent locations and time periods.
- **Baseline performance:** The persistence baseline outperformed the original LSTM and XGBoost models on the initial test comparison, highlighting the importance of evaluating complex approaches against simpler alternatives.

### Planned Improvements

- **Expand to multiple wells:** Evaluate forecasting performance across different groundwater locations to investigate geographic generalization.
- **Incorporate environmental features:** Explore vegetation indicators such as NDVI and other available environmental variables to determine whether they improve predictions.
- **Optimize model configurations:** Experiment with LSTM architectures, XGBoost hyperparameters, and alternative forecasting techniques.
- **Improve preprocessing:** Investigate missing-data strategies while minimizing the risk of information leakage.
- **Strengthen evaluation:** Compare RMSE and MAE across different wells, forecast horizons, and time periods to better understand model reliability.

### Future Research Directions

With additional time and resources, we would explore **multivariate forecasting models** that combine groundwater history with environmental predictors,
assess approaches that generalize across multiple wells, and investigate longer forecast horizons.
We also aim to evaluate our predictions against **Microsoft's challenge goal of achieving predictions within 30% of ground truth**, with a stretch goal of 20%.
Ultimately, these improvements could contribute to a more reliable and transferable AI-based forecasting framework for groundwater monitoring and environmental decision-making.


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


