---

> ## Challenge Advisor: Update & Finalize Your Project Overview
>
> > 💡 **These grey text instructions are just for you, the team's Challenge Advisor; please delete them once you have completed the steps below.**
>
> We've pre-populated this Challenge Project Overview page — which is what will be shared with your Break Through Tech student team in August — using the details from your submission form. You should have received an email inviting you to join this repo as a Collaborator, enabling you to add files and make edits.
> 
> In order for your project to be finalized and assigned to a team, please:
> 1. **Review all sections below** and update or expand any content as needed, making sure to address the SME Feedback in the section immediately below. Look for square brackets to find the places below that require additional inputs from you (e.g., "About [Company / Org Name]").
> 2. **Add your dataset** to the [data folder](data) in this repo.
> 3. **Close the Issue assigned to you in this repo** to let us know that you have made your edits and the overview page is ready for final review. You can do this by going to the _Issues_ tab in the top left section of the menu above, add a comment that says "CA review complete", and click the button to Close the Issue. 
>
> If you're unfamiliar with how to edit a page like this in GitHub, check out [this tutorial](https://ubc-lib-geo.github.io/gis-workshop-waml-template/content/handson/edit-readme.html) for a quick overview (start with step 2 and only edit this page), and [this guide](https://ubc-lib-geo.github.io/gis-workshop-waml-template/content/markdown.html) on how to use Markdown to compose text.
>
>
> ❌ Remember that this is a public repo. Do NOT include: Proprietary data, PII, API keys, credentials, or anything confidential.

---
## 📋 BTT Internal Evaluation Notes
*(This section is for BTT staff only — remove before sharing with students)*

| Check | Status | Notes |
|-------|--------|-------|
| Python Compatibility | 🟢 | The project uses a Python-compatible tech stack and libraries for ML, including LSTM and time series analysis, in Google Colab, which supports Python execution. |
| Data Readiness | 🟡 | The GROW dataset requires cleaning and preprocessing, which could consume a significant amount of time (potentially 10 weeks) before analysis can begin. |
| Resource Check | 🟢 | Utilizes free-tier tools such as Google Colab, making it accessible for students without requiring specialized hardware. |

**Student Fit Score:** 6/10  
**Technical Depth Score:** 7/10  
**Overall Recommendation:** REVISE

**Advisor Feedback Draft:**
The project holds potential due to its real-world application, fostering relevant skills in time series analysis and machine learning. However, recommend addressing the complexity by introducing a more guided preprocessing framework (or simplifying the LSTM model). Ensure clear deliverables to help track progress against metrics without overwhelming the students. Encourage engagement with the GROW dataset ahead of the main project to identify challenges early.

---
# Native Garden Design using AI

**Company / Org:** Microsoft  
**Challenge Advisor:** Aarti Dwivedi, aartidwivedi@microsoft.com  
**AI Coach:** Alexandra Ladyzhensky, alexandra.ladyzhensky@breakthroughtech.org

**Program:** Break Through Tech AI Studio - Fall 2026

---

## 🏢 About Microsoft

Microsoft is a global technology leader, empowering individuals and organizations through innovative software, services, and solutions. Our focus spans various sectors, driving advancements in AI, cloud computing, and more.

---

## 🎯 The Challenge

### Project Summary
In this project, you will use the GROW dataset and LSTM to forecast the water level in a particular groundwater well. The output will be a 7-day time series. The focus will be on the United States due to the quality and density of its data.

### Success Criteria
A prediction that is within 20% to 30% of the ground truth.

### Project Milestones

Use these milestones to guide your work. Your team will create a **GitHub Projects board** to track tasks within each milestone.

| Month | Milestone | Key Activities |
| :--- | :--- | :--- |
| September | Data Ingestion, Preprocessing & Time-Series EDA | • Load the GROW dataset and filter for U.S. groundwater well locations.<br>• Visualize temporal trends and analyze rolling statistics for trend and seasonality.<br>• Plot autocorrelation (ACF) and partial autocorrelation (PACF) functions.<br>• Impute missing time-series values using interpolation methods. |
| October | LSTM Modeling & Feature Selection | • Learn time-series LSTM architecture fundamentals and train baseline models.<br>• Train an LSTM model on the GROW dataset to forecast 7-day groundwater levels.<br>• Identify and select the top 10 features most relevant to predicting water levels. |
| November / December | Model Optimization, Evaluation & Deliverables | • Fine-tune LSTM model performance and produce comparative trend visualizations.<br>• Benchmark model accuracy against ground truth thresholds (targeting within 30% error margin).<br>• Finalize reproducible GitHub repository, documentation, and stakeholder presentation. |

### Stretch Goals
* **High-Precision Target Threshold:** Optimize model architecture and hyperparameter tuning to achieve predictions within 20% of ground truth water levels.
* **Native Plant & Ecological Mapping Layer:** Link predicted groundwater levels with native flora datasets to generate site-specific native garden design recommendations based on water availability.

> **Note for the team:** Please create a GitHub Projects board in this repository to break these milestones into weekly tasks. Go to the **Projects** tab → **New project** → Choose **Board** → Add columns for each month.

---

## 📊 Dataset

**Name and Source:** GROW dataset containing groundwater well data  
**Format:** CSV/TSV, JSON, Parquet  
**Size:** 1gb to 5gb  
**Location:** [Link to dataset or instructions for accessing it](https://zenodo.org/records/15149480)

### Key Details
- GROW dataset containing groundwater well data. The data is available at https://zenodo.org/records/15149480 and documentation is available. It will require cleaning and preprocessing.
- The dataset may contain missing values and requires specific data transformation techniques.
- [Link to data dictionary or documentation, if available]

---

## 🛠️ Suggested Approach

**ML Problem Type:** Regression

**Recommended Libraries:**
- LSTM
- Time Series Analysis
- Google Colab
- CSV/TSV
- JSON
- Parquet

**Evaluation Metrics:**
- RMSE (Root Mean Square Error)

---

## 📚 Resources to Get Started

The following resources will help your team understand the problem space and potential technical approaches for this project:

**Background Reading:**
- [Introduction to Time Series Forecasting](https://towardsdatascience.com/introduction-to-time-series-forecasting-6ff7b6315b53)
- [How LSTM Works](https://towardsdatascience.com/lstm-works-quick-intro-and-walk-through-ea5dc7e3c53c)

**Technical Tutorials:**
- [Time Series Forecasting in Python](https://www.datacamp.com/community/tutorials/time-series-analysis-python)
- [LSTM Tutorial](https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/)

**Code Examples:**
- [LSTM Implementation Example](https://github.com/keras-team/keras/blob/v2.6.0/examples/lstm_text_generation.py)
- [Sample Time Series Forecasting](https://www.kaggle.com/code/sashashin/time-series-forecasting-in-python)

**Other:**
- [Time Series Analysis - Papers](https://arxiv.org/list/stat.ML/recent)

*Feel free to explore beyond these, and share anything interesting you find with me!*

---

## 🤝 How We'll Work Together

**Check-ins:** During our biweekly 60-min AI Studio Lab Section meeting block (2nd and 4th week of every month)  
**Communication:** Slack (Break Through Tech workspace)  
**Response time:** Within 48 hours on weekdays  

**Recommended Tools:**
- **Coding:** Google Colab
- **Collaboration:** GitHub, Notion
- **Virtual Meetings:** Zoom

---

## 🚀 Getting Started

1. **Review this overview document** and note any questions for our first meeting
2. **Begin reviewing the dataset** using the link above
3. **Read the GitHub Projects documentation** [here](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)

I'm excited to work with you!

---

## ❓ Questions?

Please bring any questions to our first meeting during the week of August 24th (Break Through Tech's Bridge to Studio - Session B).

---
