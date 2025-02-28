# Capstone_1
### Title: Diagnosing Autism Spectrum Disorder in Children
This repository contains a Jupyter Notebook for EDA part of Capstone project.

### Files
- `DiagnosingASDinChildren_EDA.ipynb`: The main Jupyter Notebook file.
- `README.md`: This file.

### Diagnosing Autism Spectrum Disorder in Children
**Goal:** Despite the clear benefits of early diagnosis, identifying autism in children remains a challenging task. This is due to the heterogeneity of symptoms, delays in recognizing early signs, and limited availability of accessible and reliable diagnostic tools, particularly in underserved communities. We aim to employ a classification-based approach, which involves categorizing children into two groups—those with autism and those without—based on input features derived from relevant datasets.

**Data Problem:** Finding good datasets for this research is not easy because of many challenges. This means we have a small dataset, and because of that, we need to be careful about overfitting.

**Expected Results:** Finding a proper model with high accuracy to determine whether a child is autistic or not based on input features. 


**Data**
Source: UC Irvine Machine Learning Repository
Link: https://archive.ics.uci.edu/dataset/419/autistic+spectrum+disorder+screening+data+for+children

Data contains 20 features to be utilised for further analysis especially in determining influential autistic traits and improving the classification of ASD cases. In this dataset, we record ten behavioural features (AQ-10-Child) plus ten individuals characteristics that have proved to be effective in detecting the ASD cases from controls in behaviour science. Number of records in the datasets is 292. 

#### Data Description
1 S/he often notices small sounds when others do not [0: No, 1: Yes]


2 S/he usually concentrates more on the whole picture, rather than the small details [0: No, 1: Yes]


3 In a social group, s/he can easily keep track of several different people’s conversations [0: No, 1: Yes]


4 S/he finds it easy to go back and forth between different activities [0: No, 1: Yes]


5 S/he doesn’t know how to keep a conversation going with his/her peers [0: No, 1: Yes]


6 S/he is good at social chit-chat [0: No, 1: Yes]

7 When s/he is read a story, s/he finds it difficult to work out the character’s intentions or feelings [0: No, 1: Yes]

8 When s/he was in preschool, s/he used to enjoy playing games involving pretending with other children [0: No, 1: Yes]

9 S/he finds it easy to work out what someone is thinking or feeling just by looking at their face [0: No, 1: Yes]

10 S/he finds it hard to make new friends [0: No, 1: Yes]

11 Age [years]

12 Gender [Male or Female]

13 Ethnicity [List of common ethnicities in text format] 

14 Born with jaundice [yes or no]

15 Family member with PDD [yes or no] 

16 Country of residence [List of countries in text format]

17 Used the screening app before [yes or no]

18 Screening Score [The final score obtained based on the scoring algorithm of the screening method used. This was computed in an automated manner]

19 Screening Method Type [0=toddler, 1=child, 2= adolescent, 3= adult]

20 Who is completing the test [Parent, self, caregiver, medical staff, clinician ,etc.]

21 ASD [Yes, No]

**Data Cleaning**

After checking data, we saw that some values are ? so I should change them to NaN.

Also, age_desc column has only one value, so I drop this feature.

In addition, age column is object and I should change it to number.

After data cleaning we have 8 categorical columns: gender, ethnicity, jundice, austim, contry_of_res, used_app_before, relation, class/asd (as Target)

Now, I should convert categorical variables into numerical formats. Because there is not any ranking in these categorical columns, so I use one-hot encoding. Also, because the number of countries is relatively high. I consider 10 most frequent ones and consider reminders as others. 

