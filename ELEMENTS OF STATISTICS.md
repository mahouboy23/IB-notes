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
$$\bar{x} = \dfrac{\sum (f \cdot x)}{\sum f}$$
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