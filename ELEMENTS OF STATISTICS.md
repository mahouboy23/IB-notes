---
tags:
  - mod
  - Math
  - stat
---
# **Created: 2025-09-18**

# Introduction to Statistics

## Definition
- **Statistics** =:: collection of methods for planning studies/experiments, obtaining data, organizing, summarizing, analyzing, interpreting, and drawing conclusions.
- Goal of statistics =:: collect data from a small part (sample) to learn about the larger group (population).

## Key Terms
- **Data** =:: observations collected (measurements, genders, survey responses).
- **Population** =:: complete collection of all elements studied.
- **Census** =:: data from every member of the population.
- **Sample** =:: subcollection of population members.

### Example
Survey of 1500 U.S. adults → 855 said _yes_ to global warming.
- Population =:: all U.S. adults.
- Sample =:: 1500 surveyed adults.
- Sample data =:: 855 yes, 645 no.

---

# Parameters vs Statistics

- **Parameter** =:: numerical measurement describing a population characteristic.
- **Statistic** =:: numerical measurement describing a sample characteristic.

**Example 1**: Avg. salary $83,121 from 200 career centers →:: sample statistic.  
**Example 2**: Avg. SAT score 1442 for all 2182 admitted students →:: population parameter.

---

# Types of Data

## Qualitative vs Quantitative
- **Quantitative data** =:: numbers representing counts/measurements (e.g., weight, population).
- **Qualitative data** =:: attributes, labels, non-numerical (e.g., names, gender).

### Example
Cities & populations:
- Names =:: qualitative.
- Populations =:: quantitative.

## Discrete vs Continuous
- **Discrete data** =:: countable values ($0,1,2,3,\dots$). Example: number of eggs.
- **Continuous data** =:: infinitely many possible values on a scale (e.g., milk amount can be $2.343115$ gallons).

---

# Graphing Data

## Frequency Distribution
- **Frequency distribution** =:: table showing classes (intervals) with counts of entries.
- Frequency $f$ of class =:: number of entries in class.

### Guidelines to Construct
1. Choose number of classes ($5 \leq \text{classes} \leq 20$).
2. Find class width: $\text{Range}/\text{classes}$, round up.
3. Determine class limits (no overlap).
4. Tally each entry into a class.
5. Count tallies for frequencies.

---

# Extra Features in Frequency Table

- **Midpoint** =:: $\dfrac{\text{Lower limit} + \text{Upper limit}}{2}$
- **Relative frequency** =:: $\dfrac{f}{n}$ where $n =$ sample size
- **Cumulative frequency** =:: $\sum f$ up to that class
- **Class boundaries** =::
    - Lower boundary = $\text{Lower limit} - 0.5$
    - Upper boundary = $\text{Upper limit} + 0.5$

# **9/23/2025**
### Example table :
![[file-20250918111709365.png]]


### EX 1 :
![[STATS EX 1]]

---

# Histogram

- **Histogram** =:: bar graph with adjacent bars, showing distribution.
- Horizontal axis =:: class boundaries/midpoints.
- Vertical axis =:: frequencies.

![[file-20250923103056089.png]]
### 5 Key Features (CVDOT)
1. Center =:: typical middle value.
2. Variation =:: spread of data.
3. Distribution =:: shape (bell, skewed, uniform).
4. Outliers =:: unusual far-away values.
5. Time =:: data changes over time.

---

# Frequency Polygon

- **Frequency polygon** =:: line graph using class midpoints vs frequencies.

![[file-20250923104123878.png]]

# Dotplot

- **Dotplot** =:: each value plotted as a dot; stacked if repeated.

![[file-20250923110146203.png]]

# Stemplot (Stem-and-Leaf Plot)

- Splits each value into:: stem (left digits) + leaf (last digit).
- Similar to histogram but keeps raw data.

![[file-20250923111443056.png]]

# **9/30/2025**
# Ogive

- **Ogive** =:: line graph showing cumulative frequencies.
- Horizontal axis =:: upper class boundaries.
- Vertical axis =:: cumulative frequencies.
![[file-20250930101136501.png]]
# Scatter Plot

- **Scatter plot** =:: paired $(x,y)$ data on 2 axes → shows relationship between 2 quantitative variables.
![[file-20250930101147996.png]]
# Measures of Central Tendency
## Mean
- **Mean (average)**:  
$$\bar{x} = \dfrac{\sum x}{n}$$
- **Population mean**:  
$$\mu = \dfrac{\sum x}{N}$$
- **Sample mean**:  
$$\bar{x} = \dfrac{\sum x}{n}$$
- Sensitive to outliers; balancing point of data.

## Median
- Middle value when data are ordered.  
- If $n$ odd → median = middle value.  
- If $n$ even → median = average of two middle values.  
- Example:  
$$1,2,5,7,9 \;\Rightarrow\; \text{Median}=5$$  
$$1,2,5,7,9,12 \;\Rightarrow\; \text{Median}=\dfrac{5+7}{2}=6$$

## Mode
- Value(s) that occur most often.  
- No mode / Unimodal / Bimodal / Multimodal.

## Midrange
- **Midrange**:  
$$\text{Midrange}=\dfrac{\text{Lowest value}+\text{Highest value}}{2}$$
- Easy to compute but very sensitive to outliers.

## Weighted Mean
- Formula:  
$$\bar{x} = \dfrac{\sum (w \cdot x)}{\sum w}$$
- Where $w$ = weight of each value, $x$ = data value.  
- Used when data values are not equally important.

### Example
If test scores are weighted: Homework (40%), Midterm (30%), Final (30%), compute mean by applying weights.

## Mean from a Frequency Distribution
- Formula:  
$$\bar{x} \approx \dfrac{\sum (f \cdot x)}{\sum f}$$
- Where $f$ = frequency of each class, $x$ = class midpoint.  
- Used when data are grouped in a frequency table.

### Steps
1. Find midpoint of each class.  
2. Multiply each midpoint by its class frequency.  
3. Add up all $f \cdot x$.  
4. Divide by total frequency $n$.

# **10/2/2025**
# Measures of Variability
## Range
- **Range**:  
$$\text{Range}=\text{Maximum}-\text{Minimum}$$  
- Depends only on two values; very sensitive to outliers.

## Variance & Standard Deviation
### Population
- Variance:  
$$\sigma^2=\dfrac{\sum (x-\mu)^2}{N}$$
- Standard deviation:  
$$\sigma=\sqrt{\dfrac{\sum (x-\mu)^2}{N}}$$

### Sample
- Variance:  
$$s^2=\dfrac{\sum (x-\bar{x})^2}{n-1}$$
- Standard deviation:  
$$s=\sqrt{\dfrac{\sum (x-\bar{x})^2}{n-1}}$$

### Notes
- Units of $s$ and $\sigma$ are same as data.  
- Larger values → more variation.  
- $n-1$ = Bessel’s correction (unbiased estimate).

## Coefficient of Variation (CV)
- Sample:  
$$CV=\dfrac{s}{\bar{x}}\times 100\%$$
- Population:  
$$CV=\dfrac{\sigma}{\mu}\times 100\%$$
- Compares relative variability between datasets.

## Empirical Rule (bell-shaped distributions)
- About $68\%$ within $1\sigma$ of $\mu$  
- About $95\%$ within $2\sigma$  
- About $99.7\%$ within $3\sigma$

# Correlation

## Definition
- **Correlation** measures the strength and direction of the linear relationship between two quantitative variables.  
- Denoted by correlation coefficient $r$.  
- Values of $r$:  
  $$-1 \leq r \leq 1$$

## Pearson Correlation Coefficient
- Formula:  
$$r = \dfrac{n\sum xy - (\sum x)(\sum y)}{\sqrt{\big(n\sum x^2 - (\sum x)^2\big)\big(n\sum y^2 - (\sum y)^2\big)}}$$
- $r > 0$: positive correlation.  
- $r < 0$: negative correlation.  
- $r = 0$: no linear correlation.

## Properties
- $|r|$ close to 1 → strong correlation.  
- $|r|$ close to 0 → weak correlation.  
- Symmetric: correlation of $x$ with $y$ = correlation of $y$ with $x$.  
- Unit-free: does not depend on scale of measurement.

## Scatterplot
- A graph of paired $(x,y)$ data.  
- Used to visually assess correlation.  
- Points close to a straight line → strong correlation. 

![[file-20251002112808616.png]]

[[Stat exercises]] 
# **10/14/2025**
# Regression

## Definition
- **Regression** is a statistical method used to describe the relationship between two quantitative variables.
- The variable used to predict (independent variable) is called **x**, and the variable being predicted (dependent variable) is **y**.
- The goal is to find the **line of best fit** (regression line) that minimizes the sum of squared vertical distances between data points and the line.

![[file-20251014101618008.png]]

---

## Regression Line (Line of Best Fit)
- Equation of the regression line:
$$\hat{y} = a + bx$$

Where:
- $\hat{y}$ = predicted value of $y$
- $a$ = y-intercept
- $b$ = slope of the line

### Formulas
$$b = \dfrac{n\sum xy - (\sum x)(\sum y)}{n\sum x^2 - (\sum x)^2}$$
$$a = \dfrac{\sum y - b\sum x}{n}$$

---

## Interpretation
- **Slope ($b$)**: the amount $y$ changes for every one-unit increase in $x$.
- **Y-intercept ($a$)**: the predicted value of $y$ when $x = 0$.
- The equation $\hat{y} = a + bx$ can be used for **prediction**.

---

## Coefficient of Determination ($r^2$)
- Measures the proportion of the variation in $y$ explained by $x$.
$$r^2 = (r)^2$$
- $r^2 = 1$: perfect prediction.
- $r^2 = 0$: no linear relationship.
- Expressed as a percentage.

---

# Causation

## Correlation vs. Causation
- **Correlation** shows relationship; **causation** shows cause and effect.
- A strong correlation **does not imply** that one variable causes the other.
- Correlation may occur due to:
  - **Lurking variables** (hidden causes)
  - **Coincidence**
  - **Reverse causation**

![[file-20251016090421067.png]]

### Example
- Ice cream sales and drowning rates both increase in summer.
  → Correlation exists, but temperature is the lurking variable.

---
# **10/16/2025**
# Multiple Regression

## Definition
- **Multiple regression** is used to describe the linear relationship between one dependent (response) variable and **two or more independent (predictor)** variables.
- The goal is to **predict the value of the dependent variable** based on the values of several independent variables.

## Multiple Regression Equation
The general form of the multiple regression equation is:

$$
\hat{y} = b_0 + b_1x_1 + b_2x_2 + \dots + b_nx_n
$$

where:
- $\hat{y}$ = predicted value of the dependent variable  
- $b_0$ = intercept (value of $y$ when all $x$ values are 0)  
- $b_1, b_2, \dots, b_n$ = regression coefficients for each predictor variable  
- $x_1, x_2, \dots, x_n$ = independent (predictor) variables  

---

## Interpretation of Coefficients
- Each coefficient $b_i$ represents the **average change in $y$** when $x_i$ increases by 1 unit, while holding other variables constant.
- The **sign** of $b_i$ indicates the **direction** of the relationship:
  - $b_i > 0$: positive relationship  
  - $b_i < 0$: negative relationship  

---

## Example
**Example:**  
A study includes data for heights of mothers ($x_1$), fathers ($x_2$), and their daughters ($y$).  
We can express the relationship as:

$$
\hat{y} = b_0 + b_1x_1 + b_2x_2
$$

Suppose the resulting equation is:

$$
\hat{y} = 30.4 + 0.28x_1 + 0.41x_2
$$

Interpretation:
- The intercept $b_0 = 30.4$ means that if both parents were 0 cm tall (hypothetically), the predicted daughter’s height would be 30.4 cm.
- For each additional centimeter in the **mother’s height**, the daughter’s height increases by about **0.28 cm**, assuming the father’s height stays the same.
- For each additional centimeter in the **father’s height**, the daughter’s height increases by about **0.41 cm**, assuming the mother’s height stays the same.

---

## Coefficient of Determination ($R^2$)
- Measures how well the regression model fits the data.
- Formula:

$$
R^2 = 1 - \dfrac{\text{SS}_{\text{residual}}}{\text{SS}_{\text{total}}}
$$

where:
- $\text{SS}_{\text{residual}}$ = sum of squared differences between observed and predicted $y$ values  
- $\text{SS}_{\text{total}}$ = total sum of squares of differences between observed $y$ values and their mean  

Interpretation:
- $R^2$ ranges from 0 to 1.
- A higher $R^2$ means a better fit (the model explains more of the variation in $y$).

---

## Graphical Interpretation
 ![[file-20251016102204793.png]]
- The plane represents the best-fit surface through the 3D scatter of points.

---

## Remarks
- Calculations are typically done using statistical software due to their complexity.  
- Multiple regression helps account for **multiple factors simultaneously**, improving prediction accuracy.
- However, **correlation does not imply causation** — a strong model does not prove a cause-and-effect relationship.

---
# Section 6: Production of Data — Experimentation and Sampling

## Introduction
- The goal of data production is to **collect information** in a way that produces **valid, reliable, and unbiased results**.
- Two main sources of data:
  1. **Observational studies**
  2. **Experiments**

---

## Observational Studies
- In an **observational study**, researchers observe and record data **without influencing** the subjects.
- Used to describe situations or find associations, but **cannot establish causation**.
- Example: studying smoking habits and heart disease by observing existing behavior.

---
## Experiments
- An **experiment** involves **actively applying a treatment** to subjects and measuring the effect.
- The goal is to determine **cause-and-effect relationships**.
- The researcher **controls** one or more explanatory variables (factors).

(graph of experimental design layout)

---
## Key Terms in Experimentation
- **Experimental units**: the individuals or objects receiving the treatment.  
  - If human → called **subjects**.
- **Factor**: an explanatory variable (e.g., type of fertilizer, dosage level).
- **Treatment**: a specific condition applied to experimental units.
- **Response variable**: the outcome measured after the treatment.

---

## Principles of Experimental Design
1. **Control** – minimize effects of lurking variables.
2. **Randomization** – assign subjects to treatments randomly to avoid bias.
3. **Replication** – repeat the experiment on many subjects to reduce chance variation.

(graph of experimental process)

---

## Control Group and Placebo Effect
- **Control group**: receives no treatment or a standard treatment for comparison.
- **Placebo**: a fake treatment with no active effect.
- **Placebo effect**: subjects may respond simply because they believe they are being treated.
- To reduce bias, researchers use a **double-blind experiment**:
  - Neither subjects nor experimenters know who receives the real treatment.

---

## Types of Experimental Designs
### Completely Randomized Design
- All subjects are randomly assigned to different treatment groups.
(graph of randomized design)

### Randomized Block Design
- Subjects are grouped into **blocks** based on a shared characteristic (e.g., gender, age).
- Random assignment occurs **within each block**.
(graph of block design)

### Matched Pairs Design
- Each subject is paired with another that has similar characteristics, or with themselves under two conditions.
- Example: before-and-after weight loss measurements.

---

## Lurking and Confounding Variables
- **Lurking variable**: a hidden variable not included in the study that may influence the results.
- **Confounding variable**: occurs when the effects of two variables on a response cannot be separated.
(graph of confounding relationship)

---

# Sampling Methods

## Population vs Sample
- **Population ($N$)**: entire group of interest.
- **Sample ($n$)**: a subset of the population used to estimate population characteristics.

---

## Why Sampling?
- Studying an entire population is often **impractical** or **impossible**.
- A good sample should be **representative** of the population to avoid bias.

---

## Types of Sampling Methods

### 1. Simple Random Sample (SRS)
- Every member of the population has an **equal chance** of being chosen.
- Example: drawing names from a hat.
(graph of SRS selection)

### 2. Stratified Sampling
- Population is divided into **strata** (groups) based on a shared characteristic (e.g., gender, income level).
- A random sample is taken from each stratum.
(graph of stratified sampling)

### 3. Cluster Sampling
- Population is divided into clusters (e.g., schools, neighborhoods).
- Some clusters are randomly selected, and **all individuals** within selected clusters are surveyed.
(graph of cluster sampling)

### 4. Systematic Sampling
- Select every $k$th individual after a random starting point.
$$k = \dfrac{\text{Population size } (N)}{\text{Sample size } (n)}$$
(graph of systematic sampling)

### 5. Convenience Sampling
- Choosing individuals that are easy to reach.
- Often **biased** and **not representative**.

### 6. Voluntary Response Sampling
- Participants **choose to be part of the sample**, often leading to bias since only people with strong opinions respond.

---

## Sampling Bias
- **Bias** occurs when the sampling method **systematically favors** certain outcomes.
### Common Types:
1. **Undercoverage bias** – some groups are left out of the process.
2. **Nonresponse bias** – selected individuals do not respond.
3. **Response bias** – respondents give inaccurate answers (e.g., due to wording, interviewer, or memory).

(graph of bias examples)

---

## Random Sampling vs Random Assignment
- **Random sampling**: how subjects are selected from the population.
  - Ensures representativeness.
- **Random assignment**: how subjects are assigned to treatments.
  - Allows for cause-and-effect conclusions.

| Goal | Method Used |
|------|--------------|
| Generalize to population | Random Sampling |
| Establish causation | Random Assignment |

---

## Summary
- **Observational studies** → describe relationships.  
- **Experiments** → test causation.  
- **Randomization, control, and replication** → key to valid experiments.  
- **Sampling methods** → determine how representative and unbiased results are.


# Section 7: Probability

## Basic Concepts
- **Experiment**: any process that produces an outcome.
- **Outcome**: result of a single trial.
- **Event**: a collection of outcomes.
- **Sample space ($S$)**: set of all possible outcomes.

---

## Probability Notation
- Probability of an event $A$:
$$P(A) = \dfrac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}$$
- $0 \leq P(A) \leq 1$
- $P(A) = 0$ → impossible event.
- $P(A) = 1$ → certain event.

---

## Complement Rule
- The complement of event $A$ is all outcomes **not in A**, written $A'$.
$$P(A') = 1 - P(A)$$

---

## Addition Rule
- For **mutually exclusive** events (cannot happen together):
$$P(A \text{ or } B) = P(A) + P(B)$$
- For **non-mutually exclusive** events:
$$P(A \text{ or } B) = P(A) + P(B) - P(A \text{ and } B)$$

(graph of Venn diagram for probability addition)

---

## Multiplication Rule
- For **independent events**:
$$P(A \text{ and } B) = P(A) \times P(B)$$
- For **dependent events**:
$$P(A \text{ and } B) = P(A) \times P(B|A)$$
- Where $P(B|A)$ = probability of $B$ given $A$ occurred.

---

## Conditional Probability
- Formula:
$$P(B|A) = \dfrac{P(A \text{ and } B)}{P(A)}$$
- Used when the outcome of $A$ affects the probability of $B$.

---

## Law of Total Probability
If $A_1, A_2, A_3, \dots, A_n$ are mutually exclusive and exhaustive events:
$$P(B) = \sum P(B|A_i)P(A_i)$$

---

## Tree Diagrams
- Visual tool to show all possible outcomes and probabilities.
(graph of tree diagram example)

---

## Counting Techniques
### Fundamental Counting Rule
If one event can occur in $m$ ways and another in $n$ ways:
$$\text{Total outcomes} = m \times n$$

### Factorials
$$n! = n \times (n-1) \times (n-2) \times \dots \times 1$$

### Permutations
Order **matters**:
$$P(n, r) = \dfrac{n!}{(n-r)!}$$

### Combinations
Order **does not matter**:
$$C(n, r) = \dfrac{n!}{r!(n-r)!}$$

---

## Probability Distribution
- A table or formula that gives the probability for each possible value of a random variable $x$.  
- The sum of all probabilities must equal $1$:
$$\sum P(x) = 1$$

(graph of discrete probability distribution)
