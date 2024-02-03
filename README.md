# Handling Imbalanced Datasets with SMOTE and Sampling Techniques

## Imbalanced Dataset
Our initial dataset exhibits a severe class imbalance, with approximately 763 samples of class 0 and only 7 samples of class 1. Such a class imbalance can lead to biased model performance. To address this issue, we employed SMOTE (Synthetic Minority Over-sampling Technique) to create synthetic samples for the minority class.

## SMOTE (Synthetic Minority Over-sampling Technique)
SMOTE is a resampling technique used to balance class distribution by generating synthetic examples of the minority class. Here's how we used SMOTE to balance our dataset:

1. We identified the minority class, which in this case is class 1.

2. We applied SMOTE to the minority class, creating synthetic samples that are similar to existing class 1 samples.

3. After applying SMOTE, our dataset now has a balanced class distribution, which is essential for training machine learning models effectively.

## Sampling Techniques
To work with the balanced dataset and perform various analyses, we employed five different sampling techniques:

### 1. Random Sampling
Random sampling involves selecting data points randomly from the dataset without any specific order or pattern. The sample size was determined using the formula:

n = $\left( \frac{Z^2 \cdot p \cdot (1-p)}{(E)^2} \right)$

Where:
- `z` is the Z-score for the desired confidence level.
- `p` is the estimated proportion of the minority class.
- `i` is the total number of data points.
- `E` is the desired margin of error.

### 2. Systematic Sampling
Systematic sampling involves selecting every nth data point from the dataset, where 'n' is a fixed interval. This method provides a structured approach to sampling and can be useful for large datasets.

### 3. Stratified Sampling
Stratified sampling divides the dataset into subgroups (strata) based on a specific feature or characteristic. Samples are then taken proportionally from each stratum to ensure that the sample represents the entire population. The sample size for each stratum was determined using the formula:

n = $\left( \frac{Z^2 \cdot p \cdot (1-p)}{(E/S)^2} \right)$

Where:
- `z` is the Z-score for the desired confidence level.
- `p` is the estimated proportion of the minority class within the stratum.
- `i` is the total number of data points within the stratum.
- `E` is the desired margin of error.
- `S` is the estimated stratum size.

### 4. Bootstrap Sampling
Bootstrap sampling is a resampling technique that involves drawing samples with replacement from the dataset. This method allows us to estimate statistical properties and assess the robustness of our model.

### 5. Cross-Fold Validation
Cross-fold validation is a technique for model evaluation. It involves splitting the dataset into multiple subsets (folds), training and testing the model on different fold combinations. This method helps assess model performance and generalization.

## Conclusion
By initially addressing the class imbalance with SMOTE and subsequently applying different sampling techniques, we have created balanced samples for analysis, model training, and evaluation. Each sampling technique has its advantages and use cases, depending on the specific analysis or modeling task at hand.
