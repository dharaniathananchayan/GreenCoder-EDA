# GreenCoder-EDA
EDA for GreenCoder : AI Powered Code Optimizer Dataset
🌱 GreenCoder – Exploratory Data Analysis (EDA)

GreenCoder is an AI-driven research project focused on analyzing the carbon footprint of software code using static code features and runtime performance metrics.
This repository contains the Exploratory Data Analysis (EDA) performed on a 1 million row dataset to understand how coding patterns influence energy consumption and carbon emissions.

📌 Project Objective

The goal of this EDA is to:

Understand relationships between code structure, resource usage, and carbon emissions

Identify key features that contribute to inefficient (high-emission) code

Prepare clean, validated data for machine learning models that classify code as efficient or inefficient

📂 Dataset Overview

File name: greencoder_standard_1M.csv

Rows: 1,000,000

Columns: 12

Memory size: ~91 MB

Missing values: None (clean dataset)

🔢 Feature Description
Feature	Description
line_of_code	Number of lines in the program
cyclomatic_complexity	Logical complexity of the code
unused_imports	Count of unused imports
uses_bubble_sort	Whether bubble sort is used (0/1)
uses_linear_search	Whether linear search is used (0/1)
has_redundant_loops	Presence of unnecessary loops
cpu_usage_pct	CPU usage percentage
memory_usage_mb	Memory consumed (MB)
runtime_sec	Execution time (seconds)
energy_consumed_kwh	Energy consumption
carbon_emissions_g	Carbon emissions (grams)
is_efficient	Target label (1 = efficient, 0 = inefficient)
🔍 EDA Steps Performed
1️⃣ Data Validation

Checked data types and structure

Verified zero missing values

Confirmed numerical consistency

2️⃣ Correlation Analysis

Heatmap used to identify which features most strongly influence carbon emissions

Strong correlations found with:

CPU usage

Runtime

Memory usage

Cyclomatic complexity

3️⃣ Algorithm Efficiency Analysis

Compared bubble sort vs optimized algorithms

Used log-scale boxplots to handle extreme emission values

Bubble sort shows significantly higher emissions

4️⃣ Target Variable Distribution

Verified balance between:

Efficient code (1)

Inefficient code (0)

Dataset is suitable for supervised ML training

5️⃣ Resource Usage Exploration

CPU usage distribution analyzed for noise spikes

Memory vs emissions scatter plots show clear separation between efficient and inefficient code

6️⃣ AST Feature Insight

Regression analysis between:

Cyclomatic complexity

Carbon footprint

Higher complexity directly increases emissions

🧠 Features Used for ML Training

Excluded:

is_efficient (target)

energy_consumed_kwh

carbon_emissions_g

Final feature set:

line_of_code
cyclomatic_complexity
unused_imports
uses_bubble_sort
uses_linear_search
has_redundant_loops
cpu_usage_pct
memory_usage_mb
runtime_sec

🛠️ Technologies Used

Python

Pandas – data handling

Matplotlib – visualization

Seaborn – statistical plots

Google Colab – execution environment

📈 Key Insights

Inefficient algorithms dramatically increase emissions

Cyclomatic complexity is a strong predictor of carbon footprint

Resource-heavy code (CPU & memory) correlates with higher emissions

Dataset is ML-ready with no missing values

🚀 Next Steps

Feature scaling & normalization

Train ML models (Random Forest, XGBoost, Neural Networks)

Predict and classify carbon-efficient code

Build an AI-powered Green Coding Recommendation System
