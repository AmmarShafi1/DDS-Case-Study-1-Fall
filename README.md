# Employee Attrition Analysis for Frito Lay - DDSAnalytics

## Executive Summary
DDSAnalytics, a leading talent management analytics firm, conducted an in-depth analysis of employee attrition for Frito Lay, aiming to identify the primary factors influencing turnover and predict which employees may be more likely to leave. Using a comprehensive dataset provided by Frito Lay, this project investigates key drivers of attrition, uncovers job role-specific trends, and builds a predictive model to assist in proactive retention strategies. We have developed a naive bayes based model to predict potential attrition in employees targetting attributes such as Age, Year Since Last Promotion, Salary Hike, Distance, Job Role, Years At Company, and Number of Companies Worked.

## Introduction
Employee attrition remains a critical concern in talent management, particularly within large organizations seeking to retain high-potential employees and minimize the costs associated with turnover. Frito Lay, a prominent brand under PepsiCo, has partnered with DDSAnalytics to leverage advanced analytics in understanding and mitigating attrition. This project involves analyzing a rich dataset to reveal patterns and factors influencing employee turnover and build a model that can predict future attrition risks.

### Data
![image](https://github.com/user-attachments/assets/ac620901-1268-432b-928c-08d2e9a3388f)

The charts display key demographic data for the organization. The first chart shows a higher number of male members (516) compared to females (354). The second chart highlights the age distribution, with the majority of members in the 30-40 age group (381), followed by the 20-30 group (172) and the 40-50 group (215). The third chart reveals that most employees are in the "Research & Development" department (562), while fewer are in "Sales" (273) and "Human Resources" (35). The maximum age in the dataset is 60, and the minimum age is 18.

![image](https://github.com/user-attachments/assets/07f0622c-0f21-40c8-a82a-f51da254255d)

Here we can see that there are similar distributions with gender, age, and attrition. When looking at the percentages, we can see that they are about even excpet for the youngest of males which have a high percentage of attrition.

![image](https://github.com/user-attachments/assets/4df3a986-5320-4f3b-87a2-c37298017fa6)

The first chart shows that attrition is highest for employees with 0 to 5 years of total working experience, with a consistent attrition for employees around years of experience. We can then see that there are relatively more attiritions in the sales department relative to the other departments. Finally, we can see that Sales Representatives are by far the most "attritioned" roles by percentage.

![image](https://github.com/user-attachments/assets/c369f355-38d9-46e8-9a50-5f9061456a67)
This first chart shows us that working at more than 5 companies could be associated with higher attrition. The second chart indicates the attrition percentage based on how many years they have been at the company. The third chart reveals that attrition percentages much higher when the worker is further from home. Finally the third chart indicates that distance from home could be a contributing factor to attrition as well. 

These will be the main attributes that we will use to build a predictive model for attrition.

### Model
##KNN

![image](https://github.com/user-attachments/assets/b598cce4-2f55-41dc-bbf5-1a4f49da61e2)
![image](https://github.com/user-attachments/assets/a35a3da0-c2c9-44c6-a20b-acc6a117df67)

##NB

![image](https://github.com/user-attachments/assets/8ed287cc-b37c-43d0-b014-34eed74e696f)
![image](https://github.com/user-attachments/assets/d6ffb2df-e630-4432-8ff9-5700581a35fe)

##Results

![image](https://github.com/user-attachments/assets/fb967093-9a93-4431-940c-c73f16312539)
Accuracy, This shows how often the model gets the prediction right overall. The KNN model gets it right about 79% of the time, and the NB model about 75%. A 3% decrease in accuracy doesn’t necessarily mean the model is worse because accuracy only tells us how often the model gets any prediction right.
Sensitivity: Sensitivity tells us how well the model spots the cases we’re really looking for (like "yes" cases). The KNN model finds these only 12% of the time, while the NB model finds them 66% of the time, so NB is much better at catching what we care about
Specificity: This tells us how often the model correctly ignores the cases we don’t want. The KNN model is very good at ignoring irrelevant cases 95% of the time, whereas NB does this 77% of the time.
F1 Score: The F1 score balances how well the model finds the right cases and avoids mistakes. KNN struggles here with a score of 0.176, while NB performs better at 0.461, showing it balances finding the right cases with avoiding mistakes
In this case, the Naive Bayes (NB) model, despite a slight drop in accuracy, is much better at identifying the important positive cases (higher sensitivity) and maintains a more balanced performance (higher F1 score). This means the NB model is more reliable for situations where missing key cases (false negatives) would be more costly than a few extra correct predictions of less important cases. So, even with a small accuracy drop, the NB model is better suited for our needs.



