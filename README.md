# Seattle, WA. TerryStop Analysis

<img src=“images/handcuff.jpg” >

## Objectives
* Determine which modeling method performs best for this dataset.
* Does a relationship exist between race and being stopped?
* Does the difference between the officers race and the subjects race play a role?
* Is there a correlation between being frisked and being arrested?

## Which Modeling Algorithm Works Best?

In order to find a model that can predict if an arrest is made after being stopped, we had some work to do. After cleaning and engineering the dataset, it was divided into 75% to train and 25% to test. Continuous and categorical data were addressed using a StandardScaler and OneHotEncoding respectively. The imbalanced data from the trained dataset was put through a SMOTE to correct for imbalances and made ready for modeling.
A pipeline was created for our classifiers to obtain a model score. The classifiers used were:
* KNeighborsClassifier()
* RandomForestClassifier()
* AdaBoostClassifier()
* GradientBoostingClassifier()
The best model score was obtained from the RandomForestClassifier of 0.915.  

The features that I identified as being important included the officers age, repeat offenders and incident time.

![alt text](features.png)

## Identified Areas of Interest

### Q1: Is there a relationship between race and being stopped?

It was that there was a discrepancy in the African American community when it came to being stopped.

The percentage of those in the black/African-American community was disproportionate. While Blacks make up about 7% of the population of Seattle, they make up about 33% of those being stopped. It was also noted that the majority of the officers involved were white. This could point to a problem with officer demographics not representative of the communities they serve.

![alt text](Policecarbluelight.jpg)
![alt text](Policecarbluelight.jpg)

### Q2:  Is there an issues when the race of the officer is different than that of the subject?

Here, it was noted that there were as many as 1.5 times as many different race stops.  This is an area that could indicate that there may be a cultural problem as officers of the same race did not detain as many subjects.

![alt text](Policecarbluelight.jpg)

### Q3:  Are there correlations between frisks and arrests?

By isolating those who were only frisked and looking at those who were frisked and arrested, we found a large discrepancy.  It was noted that there were a large number of frisks that did not end in anyone being arrested.  This 'Gap' could signify that there frisking people may be excessive.  Excessive stops by officers can lead to a distrust or feeling of harassment by the communities they serve.

![alt text](Policecarbluelight.jpg)

#### Recommendation:

This dataset shows that there needs to be more research into community policing policies. I would recommend the department focus on community relations towards race relations as well.

### Conclusion:

This dataset identifies many areas where race and policing policies are in need of greater scrutiny.  There is a disproportionate amount of frisks being done that lead to nothing. Furthermore, these frisks are disproportionately affecting those of black/African-American descent.  This can cause a distrust of police and give the perception of racial profiling.
