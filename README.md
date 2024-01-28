# Sampling

Sampling is a method that allows us to get information about the population based on the statistics from a subset of the population (sample), without having to investigate every individual.
<br>

Before exploring different sampling techniques, a crucial preliminary step was taken to address the imbalance in our dataset. Initially, the dataset contained 763 non-fraudulent cases and only 9 fraudulent cases. To rectify this imbalance, an oversampling technique was employed. This involved creating additional instances of the minority class (fraudulent cases) to align more closely with the majority class (non-fraudulent cases). Subsequently, the balanced dataset was consolidated into a single data frame, which was named "df" for ease of reference.
<br>

Sampling Techniques used:

- Simple Random Sampling:
   It involves selecting individuals from the population entirely at random. 

- Systematic Sampling:
   It involves systematically selecting every kth individual from the population, where k represents a predetermined interval. 

- Cluster Sampling:
   This technique involves dividing the population into distinct clusters and then randomly selecting entire clusters for analysis. 

- Stratified Sampling:
   Stratified sampling involves categorizing the population into strata based on specific characteristics and then randomly selecting samples from each stratum. 

- Bootstrap Sampling:
   The bootstrap sampling technique employs resampling with replacement, allowing for the creation of multiple samples from the original dataset.
  
<br>
After computing five distinct samples using five different techniques, we applied five models to each sample. The computed accuracies for each model in a given sample are summarized in the table below:
  
| Sample Technique      | Logistic Regression | SVM           | Naive Bayes      | Decision Trees   | KNN              |
|-----------------------|---------------------|---------------|------------------|------------------|------------------|
| Simple Random Sampling| 0.8556              | 0.6889        | 0.7556           | 0.9222           | 0.9556           |
| Systematic Sampling   | 0.902               | 0.6765        | 0.7549           | 0.9608           | 0.9118           |
| Cluster Sampling      | 0.9583              | 0.8403        | 0.9861           | 0.9931           | 0.9861           |
| Stratified Sampling   | 0.8554              | 0.7952        | 0.7831           | 0.9157           | 0.9036           |
| Bootstrap Sampling    | 0.9375              | 0.6875        | 0.725            | 0.975            | 0.975            |

In this table, each row corresponds to a specific sampling technique, and the columns represent the accuracy achieved by each model applied to the respective sample generated using that technique.
<br>
Conclusion:-
The decision tree outperformed all other models when applied to cluster sampling with accuracy 0.9931.
