# Content Refresh Prioritization Agent

## Overview

The Content Refresh Prioritization Agent is a machine learning project developed during the FlyRank ML Internship. It helps SEO specialists and content teams identify webpages that may require content updates by analyzing historical search-performance data.

The project compares a rule-based baseline with a machine learning model to prioritize pages that may benefit from a content refresh. The recommendations are intended to support human decision-making and are not used for automatic publishing.

---

## Intended Users

This project is designed for:

- SEO Specialists
- Content Managers
- Digital Marketing Teams
- Data Analysts
- Machine Learning Students

---

## What the Agent Does

The agent performs the following steps:

1. Loads historical content-performance data.
2. Cleans and prepares the dataset.
3. Creates a proxy target representing content that may require refreshing.
4. Detects and removes target-leakage features.
5. Trains a machine learning classification model.
6. Evaluates the model using multiple performance metrics.
7. Produces prioritized recommendations for content review.
8. Requires human review before any business decision is made.

---

## Project Structure

```text
Flyrank-ML-internship/
│
├── data/
│
├── outputs/
│
├── work/
│   └── notebooks/
│       └── capstone.ipynb
│
└── README.md
```

---

## Setup Instructions

### Option 1 – Google Colab

1. Open the repository.
2. Open `work/notebooks/capstone.ipynb`.
3. Launch the notebook in Google Colab.
4. Upload or connect the required dataset.
5. Run all notebook cells from top to bottom.
6. Review the evaluation results and recommendations.

### Option 2 – Local Setup

Clone the repository:

```bash
git clone https://github.com/Pujitha-pitta/Flyrank-ML-internship.git
```

Move into the repository:

```bash
cd Flyrank-ML-internship
```

Install dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
work/notebooks/capstone.ipynb
```

Run all notebook cells.

---

## Usage Example

### Input

Historical content-performance data containing features such as:

- Impressions
- Clicks
- Sessions
- Engagement rate
- Average position
- Content age
- Days since last update
- Word count
- Content type

### Output

The notebook produces:

- Cleaned dataset
- Engineered features
- Rule-based baseline
- Machine learning predictions
- Evaluation metrics
- Ranked content-refresh recommendations

---

## Architecture

```text
Historical Content Data
          │
          ▼
Data Cleaning & Validation
          │
          ▼
Feature Engineering
          │
          ▼
Proxy Target Creation
          │
          ▼
Leakage Detection
          │
          ▼
Rule-Based Baseline
          │
          ▼
Machine Learning Model
          │
          ▼
Model Evaluation
          │
          ▼
Prioritized Recommendations
          │
          ▼
Human Review
```

---

## Design Decision

One important design decision was to create a proxy target using declining content trends because verified refresh labels were not available.

Another important decision was to remove leakage-related variables such as `trend_direction` and `trend_pct` from the model features. Including these variables would artificially increase performance because they are directly related to the target.

The project also compares a rule-based approach with a machine learning model so that improvements can be evaluated fairly.

---

## V2 Evaluation Results



The final model was evaluated by comparing a Rule-Based Baseline with a Logistic Regression model.

| Metric | Rule Baseline | Logistic Regression |
|---------|--------------:|--------------------:|
| Accuracy | 0.515 | 0.534 |
| Precision | 0.628 | 0.548 |
| Recall | 0.124 | 0.511 |
| F1 Score | 0.206 | 0.529 |
| ROC-AUC | 0.524 | 0.541 |

The Logistic Regression model improved overall balance between precision and recall compared with the rule-based baseline. Although the improvement in accuracy was modest, the higher recall and F1 score make it more suitable for identifying pages that may need review.

## Limitations

- The target is a proxy rather than a confirmed content-refresh label.
- Historical trends do not always indicate poor content quality.
- Seasonality and search-engine algorithm updates are not modeled.
- Competitor activity may influence page performance.
- Results depend on the quality of the available dataset.
- The model has not been deployed in a production environment.
- Recommendations require human review before action.
- The project is intended for decision support rather than automation.

---

## Guardrails

The project includes several safeguards:

- Target-leakage features are removed before training.
- Missing information is not fabricated.
- Recommendations are intended for decision support only.
- Human review is required before updating website content.
- The model does not automatically publish or modify content.

---

## Future Improvements

Future work could include:

- Collecting verified refresh labels.
- Testing additional machine learning models.
- Adding SHAP explainability.
- Improving probability calibration.
- Incorporating seasonality and external search-demand signals.
- Developing a web interface for non-technical users.

---

## Project Status

This project was developed as part of the FlyRank Machine Learning Internship. It demonstrates data preparation, leakage detection, machine learning model evaluation, responsible AI practices, and content prioritization using historical performance data.

The current version is a prototype intended for learning and demonstration purposes.
