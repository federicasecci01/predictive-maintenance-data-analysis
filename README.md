🇬🇧 English | 🇮🇹 [Italiano](README_IT.md)

# Predictive Maintenance Data Analysis

### Analysis of operating conditions and machine failures through Excel, descriptive statistics and Tableau

This project analyzes the **AI4I 2020 Predictive Maintenance Dataset**, consisting of **10,000 observations** from an industrial predictive maintenance context.

The objective of the project is to study machine operating behavior, compare the conditions of machines that experienced a failure with those that operated normally, and analyze the different failure modes included in the dataset.

The project combines **Microsoft Excel and Power Query** for data preparation, transformation and quantitative analysis with **Tableau**, which will be used in the final stage to build an interactive dashboard.

My background in **Mathematics** influenced the analytical approach adopted in this project, particularly in the construction of additional quantitative variables, the use of descriptive statistics, correlation analysis and the structured interpretation of numerical results.

> **Project status:** work in progress.  
> The Excel analysis has been completed. The Tableau dashboard is currently under development and will be added to the repository once completed.

---

## Analysis Objectives

The analysis was developed around a set of key questions:

* What is the overall failure frequency in the dataset?
* Which failure modes occur most frequently?
* Do average operating conditions differ between failed and non-failed machines?
* What differences emerge in terms of torque, power, tool wear, rotational speed and temperature?
* Are there linear relationships between operating variables and Machine Failure?
* How does failure frequency vary across product categories L, M and H?
* Can the main findings be summarized through an interactive dashboard?

The objective was not only to describe the dataset, but to build a structured analytical process connecting machine operating conditions with the observed failure events.

---

## Data Preparation and Transformation

**Microsoft Excel** and **Power Query** were used for data preparation and transformation.

The process included:

* dataset import;
* validation and correction of data types;
* management of failure-related variables;
* verification of the dataset structure;
* creation of additional quantitative features useful for the analysis.

### Angular Velocity

Angular velocity was calculated from rotational speed expressed in rpm:

**ω = (2 × π × n) / 60**

where:

* `ω` = angular velocity in rad/s;
* `n` = rotational speed in rpm.

### Temperature Difference

The difference between process temperature and air temperature was calculated as:

**ΔT = Process Temperature − Air Temperature**

This variable provides a direct measure of the thermal difference between the process and the surrounding environment.

### Mechanical Power

Mechanical power was calculated using torque and angular velocity:

**P = T × ω**

where:

* `P` = mechanical power;
* `T` = torque in Nm;
* `ω` = angular velocity in rad/s.

The resulting value was then converted into **kW**.

The introduction of these additional variables extends the original dataset with quantities that can be directly interpreted from a physical and mechanical perspective.

---

## Exploratory and Statistical Analysis

The quantitative analysis included:

* descriptive statistics of the main operating variables;
* comparison of mean, median, standard deviation, minimum and maximum values;
* Pivot Tables;
* comparison between failed and non-failed machines;
* analysis of individual failure modes;
* comparison across product categories L, M and H;
* correlation matrix;
* analysis of relationships between operating variables and Machine Failure.

The main variables considered include:

* Air Temperature;
* Process Temperature;
* Rotational Speed;
* Torque;
* Tool Wear;
* Delta Temperature;
* Angular Velocity;
* Mechanical Power.

---

## Failure Modes

The dataset distinguishes between several failure types:

* **TWF — Tool Wear Failure**
* **HDF — Heat Dissipation Failure**
* **PWF — Power Failure**
* **OSF — Overstrain Failure**
* **RNF — Random Failure**

The analysis compares their frequency and distribution within the dataset.

---

## Failed vs Non-Failed Machines

One of the main Pivot Tables was used to compare the **average operating conditions** of machines that did not experience a failure with those that recorded a Machine Failure.

The comparison considers variables such as:

* Rotational Speed;
* Delta Temperature;
* Mechanical Power;
* Tool Wear;
* Torque.

The results highlight differences in average operating conditions between the two groups.

In particular, failed machines show:

* **Mechanical Power:** approximately `+16,63%`
* **Tool Wear:** approximately `+34,76%`
* **Torque:** approximately `+26,59%`
* **Rotational Speed:** approximately `−2,84%`
* **Delta Temperature:** approximately `−6,16%`

The most noticeable differences emerge in **Tool Wear, Torque and Mechanical Power**.

This analysis helps identify operating characteristics associated with the failure cases observed in the dataset. However, the results are **descriptive** and should not be interpreted as evidence of a causal relationship between an individual variable and Machine Failure.

> The percentage values will be updated using the final version of the Pivot Table.

---

## Correlation Analysis

A correlation matrix was created to analyze the linear relationships between selected operating variables and **Machine Failure**.

Among the observed values:

* **Mechanical Power – Machine Failure:** `r = 0.176`
* **Tool Wear – Machine Failure:** `r = 0.105`
* **Delta Temperature – Machine Failure:** `r = -0.112`

The coefficients indicate overall **weak linear relationships**.

Mechanical Power and Tool Wear show a weak positive association with Machine Failure, while Delta Temperature shows a weak negative association.

These findings suggest that none of the individual variables considered shows, on its own, a sufficiently strong linear relationship to explain the occurrence of machine failures.

Analyzing multiple operating conditions together may therefore provide a more complete representation of machine behavior.

It is important to note that correlation measures linear association and **does not imply causation**.

---

## Main Findings

The dataset contains:

**10,000 observations**

**339 Machine Failures**

**Overall Failure Rate: approximately 3.39%**

Among the recorded failure modes, **Heat Dissipation Failure (HDF)** is the most frequent, followed by **Overstrain Failure (OSF)** and **Power Failure (PWF)**.

The comparison between failed and non-failed machines also highlights differences in operating conditions, particularly in **Tool Wear, Torque and Mechanical Power**.

Overall, the analysis indicates that machine failure cannot be reduced to the behavior of a single variable and should instead be examined by considering multiple operating conditions simultaneously.

---

## Interactive Tableau Dashboard

The final stage of the project consists of transforming the findings obtained in Excel into an **interactive Tableau dashboard**.

The dashboard will be designed to visually summarize the main analytical results while allowing dynamic exploration of the data.

It will include:

* KPIs related to the total number of Machine Failures;
* overall Failure Rate;
* distribution of the different failure modes;
* comparison between failed and non-failed machines;
* comparison across product categories L, M and H;
* analysis of the main operating conditions;
* visualization of the key insights identified during the exploratory analysis.

### Interactive Dashboard

**Currently under development.**

Once completed, the following will be added:

* dashboard preview;
* link to the interactive Tableau Public dashboard.

<!--
![Predictive Maintenance Dashboard](dashboard_preview.png)

[Explore the dashboard on Tableau Public](INSERT_LINK)
-->

---

## Tools and Skills

**Microsoft Excel**

* Power Query
* Data Cleaning
* Data Transformation
* Pivot Tables
* Descriptive Statistics
* Correlation Analysis
* Exploratory Data Analysis
* Feature Engineering

**Tableau**

* Interactive Dashboards
* KPIs
* Filters
* Data Visualization
* Comparative Analysis

**Quantitative Skills**

* Descriptive Statistics
* Correlation Analysis
* Quantitative Reasoning
* Data Interpretation
* Comparative Analysis
* Application of Physical and Mechanical Quantities
* Analytical Problem Solving

---

## Repository Contents

| File | Description |
| --- | --- |
| `predictive-maintenance-excel-analysis.xlsx` | Excel workbook containing data preparation, descriptive statistics, Pivot Tables and correlation analysis |
| `dashboard_preview.png` | Tableau dashboard preview — to be added once completed |
| Tableau Workbook | To be added once the dashboard is completed |

---

## Dataset Source

This project uses the **AI4I 2020 Predictive Maintenance Dataset**, available through the **UCI Machine Learning Repository**.

The dataset contains **10,000 observations** and was developed as a synthetic dataset designed to reflect real industrial predictive maintenance data as closely as possible.

It was used in this project for educational and portfolio purposes.

The data preparation, feature engineering, statistical analyses, Pivot Tables, interpretation of results and the Tableau dashboard were developed as part of my personal Data Analytics portfolio.

**Official source:**  
[AI4I 2020 Predictive Maintenance Dataset — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maint)

**DOI:** `10.24432/C5HS5C`

**License:** CC BY 4.0

---

## About the Project

This project represents an application of my **Mathematics background to Data Analytics in an industrial context**, combining descriptive statistics, quantitative reasoning and the interpretation of physical quantities with tools used for data preparation, analysis and visualization.

It is part of an evolving portfolio focused on transforming theoretical and analytical skills into practical, data-driven projects.
