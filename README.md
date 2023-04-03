# Exploratory Data Analysis
## About the data:
This dataset includes data on adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. This data is used for DNPAO's Data, Trends, and Maps database, which provides national and state specific data on obesity, nutrition, physical activity, and breastfeeding.

The original data can be acess on: [Source Data](https://catalog.data.gov/dataset/nutrition-physical-activity-and-obesity-behavioral-risk-factor-surveillance-system)

## Data cleaning and first investigations
The original dataset contains **33 variables** and **88629 registers**.

For variables that have **missing values above 50%** referring to the total numbers of records, they were eliminated. Below are the variables that were disregarded in this analysis.
<p align="center">
  <img src="img_examples/loss_variables.png">
</p>

Howerver, the data set was reduced to 24 variables. The relationship between the variable and its description can be found in the data dictionary, present in this link: 

[Data dictionary](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7)

It was verified that the `YarStart` and `YearEnd` columns in the dataset have the same values, that is, redundant, thay were transformed into only one variable called `Year_ref`.  
<p align="center">
  <img src="img_examples/variables.png">
</p>

## Formulating Questions: 
### What are the questions and yours code link? 
<p align="center">
  <img src="img_examples/id_question.png">
</p>

The records are arranged on 9 classes of questions, they are classified according to the question and location. Where each question carries information about the characteristics of nutrition, physical activity, obesity, etc.

### What are the most frequently questions?  
<p align="center">
  <img src="img_examples/frequent_question.png">
</p>

- The most questions frequencies are ***Q036***, ***Q037*** and **Q047**.
    
    `Q036` - *'Percent of adults aged 18 years and older who have obesity'*.
    
    `Q037` - *'Percent of adults aged 18 years and older who have an overweight classification'*.
    
    `Q047` - *'Percent of adults who engage in no leisure-time physical activity'*.
    
- The less frequencies are:
    
    `Q018` - *'Percent of adults who report consuming vegetables less than one time daily'*
    
    `Q019` - *'Percent of adults who report consuming fruit less than one time daily'*
   
### What are the distributions about `Data_Values` for this `QuestionsIDs`? 
<p align="center">
  <img src="img_examples/distributions.png">
</p>  
By note the histograms about each questionID, probably data follows a normal distribution curve. To reject the hypothese h0= the distribuition are normal was applied the hypothese test of Shapiro-Wilk for mains questions Q036, Q037, Q046, Q018 e Q019. The results are:
<p align="center">
  <img src="img_examples/tests.png">
</p>

### What are the top 10 higher percent of adults aged 18 years and older who have obesity and what is your location by year reference? 
<p align="center">
  <img src="img_examples/top10_obesity.png">
</p>
Note that the mean value to this group are 58% with obesity of total observation, the standart variation are 1.22%. The max point was in Ohio in 2016 with 60.4%. 

### What are the percent obesity evolution by year and state?
<p align="center">
  <img src="img_examples/evolution.png">
</p>
Note: All states are in uptrend. 

### What are the correlation between the % of adults with obesity and the % of adults who do not exercise ?
To answer this question, was consider a random sample of the two class with 16000 observations, this is necessary because the two class have diferente size.
<p align="center">
  <img src="img_examples/correlation.png">
</p>  
The Pearson Correlation to this case are next to zero. (-0.007184474663715776). Therefore, this data don’t show a correlation with the %non exercise with % obesity. 

### What are the 10 regions that have the highest rates of non-exercise practitioners?



