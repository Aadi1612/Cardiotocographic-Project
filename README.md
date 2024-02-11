# Fetal Heart Rate Classification Cardiotocographic Project

This project involves building machine learning models to classify fetal heart rate patterns based on various features extracted from cardiotocography (CTG) examinations. The dataset used in this project contains information about CTG examinations, including baseline values, accelerations, uterine contractions, and other parameters.

## Data Description

The dataset contains the following columns:

- **LBE**: Baseline value (medical expert)
- **LB**: Baseline value (SisPorto)
- **AC**: Accelerations (SisPorto)
- **FM**: Foetal movement (SisPorto)
- **UC**: Uterine contractions (SisPorto)
- **ASTV**: Percentage of time with abnormal short term variability (SisPorto)
- **mSTV**: Mean value of short term variability (SisPorto)
- **ALTV**: Percentage of time with abnormal long term variability (SisPorto)
- **mLTV**: Mean value of long term variability (SisPorto)
- **DL**: Light decelerations
- **DS**: Severe decelerations
- **DP**: Prolongued decelerations
- **DR**: Repetitive decelerations
- **Width**: Histogram width
- **Min**: Low frequency of the histogram
- **Max**: High frequency of the histogram
- **Nmax**: Number of histogram peaks
- **Nzeros**: Number of histogram zeros
- **Mode**: Histogram mode
- **Mean**: Histogram mean
- **Median**: Histogram median
- **Variance**: Histogram variance
- **Tendency**: Histogram tendency: -1=left asymmetric; 0=symmetric; 1=right asymmetric
- **A**: Calm sleep
- **B**: REM sleep
- **C**: Calm vigilance
- **D**: Active vigilance
- **E**: Shift pattern (A or Susp with shifts)
- **AD**: Accelerative/decelerative pattern (stress situation)
- **DE**: Decelerative pattern (vagal stimulation)
- **LD**: Largely decelerative pattern
- **FS**: Flat-sinusoidal pattern (pathological state)
- **SUSP**: Suspect pattern
- **CLASS**: Class code (1 to 10) for classes A to SUSP
- **NSP**: Normal=1; Suspect=2; Pathologic=3

## Preprocessing

- Null values were removed from the dataset.
- The dataset was split into features (X) and the target variable (Y).
- Standard scaling was applied to the features.

## Models Used

1. **Support Vector Machine (SVM)**:
   - Used for classifying the target variable into normal, suspect, and pathologic.
   - Achieved an accuracy of 87.77%.

2. **Decision Tree Classifier**:
   - Built a decision tree classifier with specified parameters.
   - Achieved an accuracy of 86.83%.

3. **Ensemble Techniques**:
   - Utilized voting classifier with SVM, Random Forest, and Decision Tree.
   - Improved the overall accuracy to 88.40%.

4. **Bagging Classifier**:
   - Improved the accuracy to 88.87% using bagging with Decision Trees.

5. **AdaBoost Classifier**:
   - Achieved an accuracy of 86.21%.

6. **XGBoost Classifier**:
   - Achieved an accuracy of 88.24%.

7. **Voting Classifier with SVM and XGBoost**:
   - Achieved an accuracy of 88.08%.

## Conclusion

- The ensemble techniques, especially the Voting Classifier, demonstrated the highest accuracy in classifying fetal heart rate patterns.
- XGBoost also performed well and can be considered for further optimization.
- The project showcases the effectiveness of machine learning in classifying CTG examination results, which can aid in prenatal care decision-making.
