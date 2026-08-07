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
In this project, you will use GROW dataset and LSTM to forecast the water level in a particular groundwater well. The output will be a 7 day time series. The focus will be on United States because of the quality and density of data. The data is available at https://zenodo.org/records/15149480. The paper is available at https://www.nature.com/articles/s41597-026-06966-1

### Success Criteria
1. A basic understanding of how to process time series data.
2. An understanding of the fundamentals of LSTM.
3. An understanding of how to approach large data sets.
4. A prediction that is within 30% of the ground truth.

### Stretch Goal
Prediction within 20% of the ground truth.
   
### Project Milestones

Use these milestones to guide your work. Your team will create a **GitHub Projects board** to track tasks within each milestone.

| Month | Milestone | Key Activities |
|---|---|---|
| September | Exploratory Data Analysis | • Load the database<br>• visualize temporal trends<br>• use rolling statistics to detect trends and seasonality<br>• use autocorrelation and partial autocorrelation plots<br>• impute missing values using interpolation |
| October | LSTM Foundations & Feature Selection | • Learn the basics of LSTM and use toy datasets to develop an understanding of the method<br>• start training LSTM on the main dataset and identify 10 features that are most relevant to the feature (water level) that we are trying to predict. |
| November | Model Refinement & Visualization | • Continue experimenting with the model and produce visualizations. |

> **Note for the team:** Please create a GitHub Projects board in this repository to break these milestones into weekly tasks. Go to the **Projects** tab → **New project** → Choose **Board** → Add columns for each month.

---

## 📊 Dataset

**Name and Source:** GROW dataset containing groundwater well data  
**Format:** CSV/TSV, JSON, Parquet  
**Size:** 1gb to 5gb  
**Location:** https://zenodo.org/records/15149480

### Key Details
- [Brief description of what's in the data]
- [Any known limitations or preprocessing needed]
- [Link to data dictionary or documentation, if available]

---

## 🛠️ Suggested Approach

**ML Problem Type:** Time Series Analysis

**Recommended Libraries:**
- [e.g., pandas, scikit-learn, TensorFlow, Hugging Face]

**Evaluation Metrics:**
- [e.g., Accuracy, Precision/Recall, RMSE, BLEU score]

---

## 📚 Resources to Get Started

The following resources will help your team understand the problem space and potential technical approaches for this project:

**Background Reading:**
- [e.g., Link to an article or blog post about the problem domain]
- [e.g., Link to an industry report or case study]

**Technical Tutorials:**
- [e.g., Link to a free tutorial on the ML technique(s) involved]
- [e.g., Link to documentation for a key library or tool]

**Code Examples:**
- [e.g., Link to a relevant GitHub repo]
- [e.g., Link to a sample implementation or starter code]

**Other:**
- [Links to any additional resources — e.g., papers, videos, podcasts, etc.]

*Feel free to explore beyond these, and share anything interesting you find with me!*


---

## 🤝 How We'll Work Together

**Official check-ins:** During our biweekly 45-minute AI Studio Lab Section meeting block (2nd and 4th week of every month)

 **Other ways to reach out to me with questions:** 
* [e.g., Your team's channel within Break Through Tech’s Discord space]
* [e.g., Email; please copy your teammates and AI Studio Coach]
* [e.g., Request a team check-in on Zoom]
* [Note: I will aim to respond within 48 hours. Please reach out to your AI Studio Coach with urgent questions.]

> 💡 **Challenge Advisor: Please update the above based on your availability and preference. If you are not able to answer questions or meet with fellows outside of the biweekly Lab Section check-ins, simply write in "N/A (only available during the official check-in times)"**

**Recommended free coding / collaboration tools**
* […]
* […]

---

## 🚀 Getting Started

1. **Review this overview document** and note any questions for our first meeting
2. **Begin reviewing the dataset** using the link above
3. **Read the GitHub Projects documentation** [here](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)

I’m excited to work with you!

---

## ❓ Questions?

Please bring any questions to our first meeting during the week of August 24th (Break Through Tech’s Bridge to Studio - Session C). 
