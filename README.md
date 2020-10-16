# Covid-MedIA
This repository contains the dataset used in the article Chassagnon, Guillaume, et al.  "AI-Driven quantification, staging and outcome prediction of COVID-19 pneumonia" https://doi.org/10.1016/j.media.2020.101860 

The dataset includes 12 csv files.
For each file, the name follows the rules:
- The second word indicates the type of variables included in the file (clinical, radiomics from the disease, radiomics from the lung, radiomics from the heart)
- For the lung and disease variables, the third word indicates the side (left or right)
- The last word indicates the split of the data this file was involved in (Training or Testing)

The files with clinical variables also include the ground truth labels considered for the two classification tasks performed Non-Severe/Severe and Non-Severe/Intubated in 4 days/ Deceased in 4 days.

The first column contains the label of the patient, the first column the names of the variables.
Values reported are raw, in the article a z-score normalization over the training set was performed.

In the article, optimization of the variables was performed through a 100-fold cross-validation on the training set, generated using the scikit-learn function StratifiedShuffleSplit with a train size of 75% and a random seed of 10.

