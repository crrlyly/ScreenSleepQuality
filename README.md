# Digital Dreams: Screen Time & Sleep Quality Analysis

**Exploratory Data Analysis • Data Visualization • Regression Modeling**

A collaborative data science research project exploring relationships between pre-sleep social media use, screen exposure, and sleep outcomes. Using Python, we examined patterns across demographic groups, visualized relationships in the dataset, and built regression models to predict sleep efficiency.

**Contributors:** Carly Chick and Meryl Gideon  
**Project type:** Academic data science research project

## Project Overview

**Research question:** What relationships exist between screen usage and sleep quality?

The analysis investigates how pre-sleep social media use and blue-light exposure relate to sleep quality, sleep latency, melatonin levels, and sleep efficiency. We also explore whether patterns differ across age groups, gender, and types of social media content.

> **Important:** This is an observational data analysis. Associations and model predictions do not establish that screen use causes changes in sleep outcomes.

## Technologies & Skills

- **Languages and environment:** Python, Jupyter Notebook
- **Data preparation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Modeling:** scikit-learn, multivariate linear regression, polynomial regression
- **Evaluation:** Train/test split, R², cross-validation
- **Analytical techniques:** Exploratory data analysis (EDA), data cleaning, feature engineering, demographic comparisons

## Analysis Workflow

### 1. Data Preparation

- Loaded the sleep and social media usage dataset into a Pandas DataFrame.
- Removed columns not needed for the analysis and checked for missing values.
- Created an **Age Group** feature to compare participants across age ranges.
- Confirmed that the variables used in the analysis were available in numerical form where required.

### 2. Exploratory Data Analysis

Created visualizations to explore relationships and group differences:

- **Scatterplots:** Pre-sleep social media use versus sleep quality, including comparisons by age group and gender.
- **Bar charts:** Average total sleep time and sleep latency by social media content type.
- **Heatmaps:** Average melatonin levels across screen-time and blue-light-exposure groups, segmented by age.

These visualizations help identify patterns worth investigating further; they are not, by themselves, evidence of causation.

### 3. Regression Modeling

Built a multivariate linear regression model to predict **sleep efficiency (%)** using:

- Pre-sleep social media use duration
- Blue-light exposure before sleep
- Sleep latency
- Melatonin level

The notebook also constructs a **degree-2 polynomial regression pipeline** to explore nonlinear relationships among the predictors.

### 4. Model Evaluation

- Split the dataset into training and test sets.
- Examined model coefficients and plotted actual versus predicted sleep efficiency.
- Used **3-fold cross-validation** to evaluate the polynomial regression pipeline.

**Recorded cross-validation results (polynomial pipeline):**

| Fold | R² |
| --- | ---: |
| 1 | 0.852 |
| 2 | 0.810 |
| 3 | 0.808 |
| **Mean** | **0.823** |

The mean cross-validated R² is approximately **0.823** for the notebook's reported evaluation. This should not be interpreted as a causal effect or as a separately measured held-out test score.

**Evaluation note:** In the current notebook, the actual-versus-predicted chart uses predictions from the original linear model, while the cross-validation scores come from the polynomial pipeline. These are different evaluations and should not be described as results from the same fitted model.

## Interpretation & Limitations

The project demonstrates a workflow for exploring sleep-related data and comparing predictive models. Several limitations matter when interpreting the results:

- **Correlation is not causation:** The analysis cannot establish that screen time directly causes changes in sleep quality.
- **Predictor choice:** Sleep latency and melatonin levels are closely related to sleep outcomes; a screen-exposure-only model would help isolate how much predictive value the exposure variables provide.
- **Model comparison:** Linear and polynomial models should be compared on the same evaluation splits and metrics before selecting a preferred approach.
- **Generalizability:** Findings depend on the dataset's collection methods, population, and representativeness.

## Repository Contents

| File | Description |
| --- | --- |
| [`final-project.ipynb`](final-project.ipynb) | Python notebook containing preprocessing, visualizations, and regression modeling |
| [`Final_DS_Research_Paper.pdf`](Final_DS_Research_Paper.pdf) | Full research paper |
| [`SocialMediaUsage_SleepLatencyAnalysis_Singapore (1).csv`](SocialMediaUsage_SleepLatencyAnalysis_Singapore%20(1).csv) | Dataset used in the analysis |
| [`README.md`](README.md) | Project overview and documentation |

## Run the Notebook Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/crrlyly/ScreenSleepQuality.git
   cd ScreenSleepQuality
   ```

2. Install the required packages:

   ```bash
   python -m pip install pandas numpy matplotlib seaborn scikit-learn ipykernel
   ```

3. Open `final-project.ipynb` in VS Code with the **Python** and **Jupyter** extensions installed, or open it in Jupyter Notebook.
4. Select a Python kernel with the packages installed.
5. **Before running**, update the CSV path in the notebook to match the dataset filename in this repository:

   ```python
   df = pd.read_csv('SocialMediaUsage_SleepLatencyAnalysis_Singapore (1).csv')
   ```

6. Run the cells in order.

## Future Improvements

- Compare baseline linear and polynomial regression using consistent test-set metrics (including RMSE).
- Evaluate models using screen-exposure predictors alone versus additional sleep-related predictors.
- Add a concise results summary with selected charts to the README.
- Document the dataset's original source, sampling process, and potential biases in more detail.

---

**Explore the work:** [Jupyter Notebook](final-project.ipynb) · [Research Paper](Final_DS_Research_Paper.pdf)
