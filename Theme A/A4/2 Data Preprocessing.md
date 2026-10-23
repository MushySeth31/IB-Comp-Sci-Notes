# Data Preprocessing

> **How do we tell whether data is reliable or not, and how do we fix it?**

## Data Cleaning

The process of detecting and correcting or removing inaccurate, incomplete, duplicated, irrelevant, or improperly formatted data.

After data has been collected, data cleaning ensures that data-quality problems are identified and addressed before they undermine subsequent analysis or model training.

### Why clean data?

Poor-quality data can cause:

- Inaccurate predictions
- Biased models
- Misleading patterns
- Poor generalization

---

## Data Quality

Concerns whether data is suitable for its intended purpose.

### Quality aspects

- **Completeness** — whether all required data is present.
- **Accuracy** — whether the data correctly represents the real-world value.
- **Consistency** — whether the same information is represented in the same way throughout the dataset.
- **Validity** — whether values conform to the expected format, range, or constraints.
- **Uniqueness** — whether each observation is represented only once.
- **Relevance** — whether the data is useful for the intended purpose.

---

# Types of Data Problems

## Outliers

An observation that differs substantially from the rest of the data.

### Example

Daily temperatures recorded by a weather station:

```text
28, 29, 30, 29, 31, 28, 250
```

`250` is unrealistic.

### Possible causes

- Measurement or entry errors
- Equipment malfunction
- Rare but legitimate events
- Genuine unusual behavior

### Actions

- Investigate the value
- Correct it
- Remove it
- Transform it
- Retain it if it is actually legitimate

> **Important:** Not all outliers are incorrect. A genuine outlier can contain useful information.

---

## Duplicate Data

The same observation is unintentionally included more than once.

### Possible effects

- Some observations may receive excessive weight.
- Summary statistics may be distorted.
- The model may learn misleading patterns.

### Solutions

- Remove duplicate records.
- Consolidate records when they contain complementary information.

---

## Incorrect Data

The dataset contains values that violate the expected constraints.

### Example

```text
Age = -17
```

### Possible solutions

- Apply validation rules.
- Cross-reference another source.
- Identify and investigate anomalies.
- Correct or remove invalid values.

---

## Irrelevant Data

Data that has little to no useful relationship to the predictions or analysis.

### Effects of removing irrelevant data

- Reduces computation
- Reduces noise
- Simplifies the model
- Reduces the risk of overfitting

---

## Inconsistent Data

The same information is represented differently.

If values are not standardized appropriately, a system may interpret equivalent values differently.

### Actions

- Use consistent date formats.
- Convert measurements into common units.
- Standardize categorical labels.
- Convert data types when necessary.

### Example

```text
Date: 10/05/2026
Date: 05/10/2026
```

Depending on the convention, these could represent different dates.

---

# Missing Data

A value that should be recorded is unavailable.

### Possible causes

- Sensor failure
- Record was not collected
- Data loss during transfer
- User did not provide the information

### Methods for handling missing data

1. Deletion
2. Imputation
3. Predictive modeling

---

## Deletion

Removes records or fields containing missing data.

### Advantages

- Simple to implement
- Does not introduce estimated replacement values

### Disadvantages

- Reduces the dataset size
- May discard useful information
- Can introduce bias if missingness is systematic

> May be appropriate when the affected records are few and removing them will not seriously distort the dataset.

---

## Imputation

Replaces missing values with estimated or selected values.

### Common approaches

- **Mean** — replace the missing value with the mean of the relevant values.
- **Median** — replace the missing value with the median.
- **Mode** — replace the missing value with the most frequent value.
- **K-NN-based estimate** — estimate the value using similar observations identified through K-nearest neighbors.

> Because imputed values are estimates, they are not necessarily the true values.

---

## Predictive Modeling

Uses another model to estimate the missing value.

### Advantages

- Can use relationships between variables.
- May produce more informative estimates than a simple average.

### Disadvantages

- Requires sufficient reliable data.
- More complex to implement.
- Can introduce errors if the predictive model is inaccurate.

---

## Distinction: Deletion vs Imputation vs Predictive Modeling

| Method | What it does | Main advantage | Main disadvantage |
|---|---|---|---|
| **Deletion** | Removes records or fields containing missing data | Simple | Can discard useful data and introduce bias |
| **Imputation** | Replaces missing values with estimated or selected values | Retains the dataset | Introduces estimated values |
| **Predictive modeling** | Uses a model to predict missing values | Can account for relationships between variables | More complex and dependent on model accuracy |

---

# Summary: Data Problems and Solutions

| Data problem | Description | Possible solution |
|---|---|---|
| **Outlier** | Value substantially different from the rest | Investigate, correct, remove, transform, or retain |
| **Duplicate** | Same observation appears more than once | Remove or consolidate |
| **Incorrect data** | Value violates expected constraints | Validate, cross-reference, correct, or remove |
| **Irrelevant data** | Data has little useful relationship to the task | Remove |
| **Inconsistent data** | Same information is represented differently | Standardize formats, units, labels, or data types |
| **Missing data** | Expected value is unavailable | Deletion, imputation, or predictive modeling |

---

# Normalization

A preprocessing technique that scales numerical data to a specified range, commonly **0 to 1**.

A common min-max normalization formula is:

$$
x' = \frac{x-x_{\min}}{x_{\max}-x_{\min}}
$$

where:

- $x$ is the original value.
- $x_{\min}$ is the minimum value in the dataset.
- $x_{\max}$ is the maximum value in the dataset.
- $x'$ is the normalized value.

### Example

For values ranging from 10 to 50:

```text
x = 30
x_min = 10
x_max = 50
```

$$
x' = \frac{30-10}{50-10}
$$

$$
x' = 0.5
$$

Therefore, `30` becomes `0.5` after normalization.

### Purpose

Normalization is useful when numerical features have different scales and a machine-learning algorithm is sensitive to the magnitude of the input values.

---

# Standardization

A preprocessing technique that transforms numerical data so that it has a mean of **0** and a standard deviation of **1**.

The standardization formula is:

$$
z = \frac{x-\mu}{\sigma}
$$

where:

- $x$ is the original value.
- $\mu$ is the mean of the dataset.
- $\sigma$ is the standard deviation.
- $z$ is the standardized value.

### Purpose

Standardization allows features with different units or scales to be placed on a comparable scale without restricting them to a specific range.

---

## Distinction: Normalization vs Standardization

| | **Normalization** | **Standardization** |
|---|---|---|
| **Main purpose** | Scale values to a specified range | Center and scale data |
| **Common result** | Usually 0 to 1 | Mean = 0, standard deviation = 1 |
| **Formula** | $\frac{x-x_{\min}}{x_{\max}-x_{\min}}$ | $\frac{x-\mu}{\sigma}$ |
| **Depends on** | Minimum and maximum | Mean and standard deviation |
| **Effect of outliers** | Can be strongly affected | Can also be affected |

---

# Feature Selection

Selecting the most informative input features and removing irrelevant or redundant ones.

Feature selection reduces the number of input variables used by a machine-learning model while retaining the features that are most useful for making predictions.

### Benefits

- Reduces computational requirements
- Reduces irrelevant information
- Can reduce overfitting
- Can improve model interpretability
- Can improve model performance

---

## Methods of Feature Selection

### Filter

Selects features using statistical characteristics **before training the model**.

Examples include evaluating:

- Correlation
- Statistical significance
- Variance

**Key idea:** Features are selected independently of the machine-learning model.

---

### Wrapper

Evaluates different **subsets of features by actually training and evaluating the model**.

The process typically involves:

1. Select a subset of features.
2. Train the model.
3. Evaluate its performance.
4. Compare it with other subsets.
5. Select the best-performing subset.

**Key idea:** Uses the model's performance to determine which features are useful.

---

### Embedded

Evaluates or selects features **during the model's training process**.

The learning algorithm itself determines which features are important.

**Key idea:** Feature selection is built into the training process.

---

## Distinction: Filter vs Wrapper vs Embedded

| Method | When selection occurs | How features are evaluated |
|---|---|---|
| **Filter** | Before model training | Statistical characteristics |
| **Wrapper** | Through repeated model training | Model performance using feature subsets |
| **Embedded** | During model training | The learning algorithm evaluates feature importance |

---

# Dimensionality Reduction

A technique that reduces the number of features in a dataset while attempting to preserve the important information.

Unlike feature selection, dimensionality reduction can **transform existing features into a smaller set of new features** rather than simply removing individual features.

### Purpose

- Reduce computational complexity
- Reduce the amount of data that must be processed
- Remove redundant information
- Make high-dimensional data easier to analyze or visualize
- Potentially reduce overfitting

### Example

A dataset contains:

```text
100 input features
```

A dimensionality-reduction technique could transform these into:

```text
10 new features
```

The 10 new features aim to preserve as much of the important information from the original 100 features as possible.

---

## Feature Selection vs Dimensionality Reduction

| | **Feature Selection** | **Dimensionality Reduction** |
|---|---|---|
| **What happens?** | Selects existing features | Creates/transforms features |
| **Original features** | Some are retained unchanged | Usually transformed into new representations |
| **Example** | Keep 10 of 100 features | Transform 100 features into 10 components |
| **Interpretability** | Generally easier to interpret | New features may be harder to interpret |
| **Main goal** | Remove irrelevant/redundant features | Reduce dimensionality while preserving information |

---

# Summary

Data preprocessing prepares raw data so that it is suitable for analysis and machine-learning models.

### Key techniques

- **Data cleaning** — detects and corrects or removes problematic data.
- **Deletion** — removes records or fields containing missing values.
- **Imputation** — replaces missing values with estimated or selected values.
- **Predictive modeling** — predicts missing values using relationships between variables.
- **Normalization** — scales numerical data to a specified range, commonly 0–1.
- **Standardization** — transforms data to have a mean of 0 and standard deviation of 1.
- **Feature selection** — selects useful existing features and removes irrelevant or redundant ones.
- **Dimensionality reduction** — transforms data into fewer dimensions while attempting to preserve important information.

> **Overall goal:** Improve the quality and suitability of data before it is used for analysis or machine-learning model training.
