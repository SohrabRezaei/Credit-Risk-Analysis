# Credit-Risk-Analysis

## Overview of the analysis

I am asked to resample the credit card data since it is not balanced. First, I start to split the data and perform oversampling with [RandomOverSampler](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html) and [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html) method, and I undersample with [ClusterCentroids](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.ClusterCentroids.html) algorithm. Then, I utilize the [SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html) method to oversample and undersample the data. Finally, I use ensemble models such as [EasyEnsembleClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html) and [BalancedRandomForestClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html) to predict the credit card fraud risks.

## Results

* The balanced accuracy score for RandomOverSampler oversampling method is 0.643. The precision and recall are 1 and 0.59, respectively, for non-fraudulent credit cards.
![image](https://user-images.githubusercontent.com/95439555/166144499-6098bf12-3d43-4ad8-9a63-9bc0e25410a3.png) ![image](https://user-images.githubusercontent.com/95439555/166144506-3ebc890b-1b39-4ebf-88db-52e2f52e5172.png)

* The balanced accuaracy score for SMOTE oversampling method is 0.662. The presicion and recall is 1 and 0.69 respectively for non-fraudaulent credit cards. ![image](https://user-images.githubusercontent.com/95439555/166144740-6390904a-24ce-4d67-8f0a-759c359e35f9.png) ![image](https://user-images.githubusercontent.com/95439555/166144753-9d084bdb-78b8-480e-ad1f-813a9989e26d.png)

* The balanced accuaracy score for ClusterCentroids undersampling method is 0.544. The presicion and recall is 1 and 0.4 respectively for non-fraudaulent credit cards. ![image](https://user-images.githubusercontent.com/95439555/166144821-bffbcd5b-17f7-40af-880a-df68c03972ea.png) ![image](https://user-images.githubusercontent.com/95439555/166144832-b4c0ce13-2072-4a63-9536-18e073805539.png)

* The balanced accuracy score for SMOTEENN oversampling and undersampling method is 0.674. The precision and recall is 1 and 0.59 respectively for non-fraudulent credit cards.![image](https://user-images.githubusercontent.com/95439555/166144931-d86edc94-6a40-4e9f-994f-5b8002bcff92.png) ![image](https://user-images.githubusercontent.com/95439555/166144946-14e5df62-230d-4f3d-ab3c-75390bfcd7e5.png)

* The balanced accuaracy score for BalancedRandomForestClassifier ensemble method is 0.788. The presicion and recall is 1 and 0.87 respectively for non-fraudaulent credit cards. ![image](https://user-images.githubusercontent.com/95439555/166145117-a7b67831-22db-4c39-9db4-270c18b40cb0.png) ![image](https://user-images.githubusercontent.com/95439555/166145135-56cc197a-505b-45b1-ab2a-2584666c538b.png)

* The balanced accuaracy score for EasyEnsembleClassifier ensemble method is 0.915. The presicion and recall is 1 and 0.9 respectively for non-fraudaulent credit cards. ![image](https://user-images.githubusercontent.com/95439555/166145155-689b0184-bbc6-46f4-8a59-423c19467fbf.png) ![image](https://user-images.githubusercontent.com/95439555/166145165-e3576a80-78d3-4aee-936c-67535953930f.png)

## Summary

All the models had a precision of 1 for non-fraudulent cards, and all of them had 0.01 precision for fraudulent cards. Therefore, they are not suitable for predicting fraudulent credit cards. I recommend using The EasyEnsembleClassifier model, which has a balance accuracy score of 0.915 and a recall of 0.9 for non-fraudulent credit cards.



