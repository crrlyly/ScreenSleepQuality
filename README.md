# Data Science Project Proposal

## Title and Team Information

### Project Title:
• Digital Dreams - Unveiling the Impact of Screen Time on Sleep Quality

### Names of All Members:
• Carly Chick 
• Meryl Gideon

## Research Question and Motivation

### Clearly state the research question you aim to answer:
• What is the relationship between screen usage and sleep quality?

### Provide context and motivation for why this question is important or interesting.
• Our project examines the connection between screen time and sleep quality, highlighting
the impact of electronic devices on our health. Poor sleep, linked to serious issues like
stress, heart disease, and cognitive impairment, can be exacerbated by the blue light from
screens which disrupts melatonin production. Our research aims to promote better screen
time management to improve sleep and overall well-being.

## Data Sources

### Identify the data sources you plan to use.
• Kaggle, Data.gov, Github18

### Explain how you will obtain, clean, and preprocess the data.
• We will download the provided csv files on the kaggle website and also get any other
information we need from the rest of our data sources.
• We will make sure to drop any NULL values and to get rid of columns that we don’t need,
make sure that numerical values are either int or floats, and we will get rid of any unneeded
information by extracting data using regex.

### If applicable, discuss potential challenges in data access, quality, or preprocessing.
• A potential challenge we face is determining the most relevant data to use, especially when
encountering datasets with multiple data points consolidated into a single cell, such as "3gb
/ 4gb."
• Another challenge is making sure that the data is all correctly cleaned. Some datasets are
extremely large so it is easy to miss uncleaned information.

## Methodology and Analysis Plan

### Describe the data science techniques you intend to use.
• **Regex** - for searching and manipulating strings based on patterns. Will also use in data
cleaning processes to remove unwanted characters.
• Pandas - make dataframes and combine tables to see relationships between values.
• Matplotlib - use this to visualize our data and more easily see distributions and metric data.
• Data Visualization - Understanding the data through statistics (mean, median, mode, vari-
ance, etc.) and distributions.

### Outline your approach for data exploration, modeling, and evaluation.

• **Data Exploration**
– We will download datasets from our mentioned data sources, making sure they are
relevant to our research question and use Python and Pandas to manipulate the data
as necessary to create our main dataframe. Then we will use Regex to clean text data
or extract specific information from strings. To handle missing values, we will either
replace them or drop them. We will also use Pandas to group data if needed.
– Tools: Python, Kaggle, Pandas, Numpy, re for Regex

• **Modeling**
– For modeling, we will normalize or scale data (if necessary).
– Use Matplotlib (and possibly Seaborn) to make charts and graphs that help visualize
our data distributions and variable relationships.
– Create a linear regression model to evaluate our data and test the relationships between fields.
– Tools used: Matplotlib, Seaborn, scikit-learn

• **Evaluation**
– We will analyze the graphs and use them to show trends and outliers. That will be used
to interpret the results in the context of the research question. From there, we will make
a conclusion based on the analysis to discuss any significant findings. Then, we will
suggest reasons for the observed trends and behaviors using both the data and external
research.

– Tools used: Python, Matplotlib, Jupyter Notebook for documentation.

## Expected Outcomes and Evaluation
### Discuss the anticipated findings or insights you hope to uncover.
• From our research, we hope to see the correlation between screen time and sleep quality,
focusing on how different levels of screen use affect sleep duration and quality. We anticipate
discovering variations in this correlation across different demographics like age groups.
We also expect to see how the timing of screen usage influences sleep patterns, potentially
identifying periods when screen exposure most negatively affects sleep quality.

### Define metrics or evaluation criteria for assessing your results.
• We will use the Correlation Coefficient to assess the strength of the relationship between
screen time and sleep quality, with values near -1 or 1 indicating strong correlations. We will
also compare the average sleep quality of high vs low screen users to identify any significant
differences and use the visual charts we created.

5.3 If applicable, outline any potential extensions or broader implications of your work.
• Our findings could help shape technology usage guidelines, influencing public health policies
and wellness, and could enrich the discourse on digital well-being, offering evidence on
how technology impacts our health.
