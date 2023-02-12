# PHASE-3-PROJECT: PREDICTING THE PROBABILITY THAT A PERSON WILL RECEIVE THE H1N1 AND SEASONAL FLU VACCINES USING MACHINE LEARNING MODELS



# Overview


The goal is to predict how likely individuals are to receive their H1N1 and seasonal flu vaccines. 
Specifically,predicting two probabilities: one for h1n1_vaccine and one for seasonal_vaccine.
A pandemic brought on by the H1N1 influenza virus, also known as "swine flu," started in the spring of 2009. According to research, it caused anywhere from 151,000 to 575,000 deaths worldwide in the first year.

In October 2009, an H1N1 flu vaccination became widely accessible. The National 2009 H1N1 Flu Survey was carried out in the US in late 2009 and early 2010. In addition to personal information, this phone poll also questioned participants if they had gotten the H1N1 and seasonal flu vaccines. These extra questions included their social, economic, and demographic background, viewpoints on disease risks and the efficacy of vaccinations, as well as actions aimed at reducing transmission. A clearer knowledge of the connections between these traits and individual vaccination habits can

![vaccine](https://user-images.githubusercontent.com/22881701/218325070-031d25c5-359c-4aa0-bdb4-b4ea5097857a.jpg)



# BUSINESS UNDERSTANDING

In 2009, the H1N1 influenza pandemic, commonly referred to as "swine flu," spread across the world, resulting in an estimated 151,000 to 575,000 deaths globally in its first year. To combat the virus, a vaccine was made publicly available in October 2009. To gain insight into vaccination patterns and behavior, the United States conducted the National 2009 H1N1 Flu Survey, which was a phone survey that asked participants about their H1N1 and seasonal flu vaccine status, as well as their social, economic, and demographic information, opinions on illness and vaccine risks, and behaviors for reducing transmission. By gaining a better understanding of the relationships between these factors and vaccination patterns, this information can be used to guide future public health initiatives.



# Main Objective 

The goal is to predict how likely individuals are to receive their H1N1 and seasonal flu vaccines. 

# The metric of success
The performance will be evaluated according to the area under the receiver operating characteristic curve (ROC AUC) for each of the two target variables.


# Data Understanding 
Data Source

Data that was used was downloaded from  [Driven Data](https://www.drivendata.org/competitions/66/flu-shot-learning/page/210/)


# Data Description 

The information in the data is as follows:
* h1n1_concern - Level of concern about the H1N1 flu.
* h1n1_knowledge - Level of knowledge about H1N1 flu.
* behavioral_antiviral_meds - Has taken antiviral medications. 
* behavioral_avoidance - Has avoided close contact with others with flu-like symptoms. 
* behavioral_face_mask - Has bought a face mask. 
* behavioral_wash_hands - Has frequently washed hands or used hand sanitizer. 
* behavioral_large_gatherings - Has reduced time at large gatherings. 
* behavioral_outside_home - Has reduced contact with people outside of own household. 
* behavioral_touch_face - Has avoided touching eyes, nose, or mouth. 
* doctor_recc_h1n1 - H1N1 flu vaccine was recommended by doctor.
* doctor_recc_seasonal - Seasonal flu vaccine was recommended by doctor. 
* chronic_med_condition - Has any of the following chronic medical conditions: asthma or an other lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness. 
* child_under_6_months - Has regular close contact with a child under the age of six months. 
* health_worker - Is a healthcare worker. 
* health_insurance - Has health insurance. 
* opinion_h1n1_vacc_effective - Respondent's opinion about H1N1 vaccine effectiveness.
* opinion_h1n1_risk - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.
* opinion_h1n1_sick_from_vacc - Respondent's worry of getting sick from taking H1N1 vaccine.
* opinion_seas_vacc_effective - Respondent's opinion about seasonal flu vaccine effectiveness.
* opinion_seas_risk - Respondent's opinion about risk of getting sick with seasonal flu without vaccine.
* opinion_seas_sick_from_vacc - Respondent's worry of getting sick from taking seasonal flu vaccine.
* age_group - Age group of respondent.
* education - Self-reported education level.
* race - Race of respondent.
* sex - Sex of respondent.
* income_poverty - Household annual income of respondent with respect to 2008 Census poverty thresholds.
* marital_status - Marital status of respondent.
* rent_or_own - Housing situation of respondent.
* employment_status - Employment status of respondent.
* hhs_geo_region - Respondent's residence using a 10-region geographic classification defined by the U.S. Dept. of Health and Human Services. Values are represented as short random character strings.
* census_msa - Respondent's residence within metropolitan statistical areas (MSA) as defined by the U.S. Census.
* household_adults - Number of other adults in household, top-coded to 3.
* household_children - Number of children in household, top-coded to 3.
* employment_industry - Type of industry respondent is employed in. Values are represented as short random character strings.
* employment_occupation - Type of occupation of respondent. Values are represented as short random character strings.



# Data Preparation

Loading Libraries
Load the libraries necessary for cleaning and analysis

Loading the Data
Load the dataset from the CSV file. The names of the CSV files are: “test_set_features.csv, “training_set_features.csv”, “training_set_labels.csv” and “submission_format.csv”
The shape of the dataset is: training set labels(26707rows,3 columns), training set features (26707 rows, 36 columns), and test set features (26707 rows, 36 columns). 

Cleaning the Data
Data cleaning is the process of preparing data for analysis by removing irrelevant or incorrect information. This type of information usually reinforces a false belief, which can have a negative impact on the model or algorithm into which it is fed.


The steps for the data cleaning process are:

* Ensured that there are no duplicates in the data.

* Ensured that the dataset data types are correct.

* Ensured that there are no missing values in the dataset.


# Modelling

To predict the likelihood of respondents in the survey taking the h1n1 vaccine and seasonal vaccine, machine learning algorithms were used.
The ultimate accuracy was determined using logistic regression, decision trees, and XGBoost.

![modelling](https://user-images.githubusercontent.com/22881701/218327274-45075b5c-f176-40de-a234-19cdc10a4840.png)

The logistic regression model, which returned 81.29% more results than the other two models, is now the best of the ones that were utilized.


![model](https://user-images.githubusercontent.com/22881701/218340781-3cd4fbba-297d-476c-8406-9714aacb0a0b.PNG)


# Conclusion and Recommendation 

# Conclusion

* People who received the seasonal vaccine outperformed those who received the H1N1 vaccine.
* Women received both immunizations at a higher rate than males.
* White folks received both immunizations at a higher rate than other races.
* People with health insurance chose seasonal vaccines over H1N1 vaccines.
* More People chose the seasonal vaccine over the H1N1 vaccine based on doctor’s recommendations.
* There were fewer persons seeking both immunizations than predicted.
* In addition, children were not as well immunized as planned.

# Recommendations 
Based on the conclusion drawn from the data, here are a few recommendations that could be made:
* Promote the importance of the seasonal flu vaccine over the H1N1 vaccine, highlighting its higher efficacy and safety record.
* Encourage greater immunization rates among males and people of other races, perhaps through targeted outreach and education initiatives.
* Address the issue of access to health insurance, as it appears to impact vaccine choice.
* Encourage more people to seek recommendations from their healthcare providers, as this seems to be a significant factor in vaccine choice.
* Address the low immunization rate among children by increasing awareness of the importance of protecting this vulnerable population and providing easier access to vaccines for families with young children.
* Consider additional strategies to increase overall immunization rates, such as offering incentives or increasing accessibility to vaccines.
* Further analysis and research may be needed to understand and address the underlying issues more effectively.





