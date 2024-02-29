
# Lead Scoring
 - Supervised Learning



## Authors

- [Jeetendra Sarpe](https://github.com/jtndr26)


### Business Context:
X Education, an online education company, caters to industry professionals seeking to enhance their skills through online courses. Each day, numerous professionals visit the company's website to explore available courses. Upon providing their contact information through a form submission or as a result of past referrals, these individuals are classified as leads. Subsequently, the sales team engages with these leads through various channels such as phone calls and emails to encourage course enrollment. While some leads successfully convert into paying customers, a significant portion do not. This dynamic highlights the need for an effective lead scoring machine learning model to prioritize and focus sales efforts on leads with the highest likelihood of conversion, thereby optimizing the company's sales process and maximizing revenue generation potential.

### Project Description:
X Education faces a significant challenge with its lead conversion rate, which currently stands at only 30%, well below industry standards. To address this issue and improve efficiency, the company seeks to identify the most promising leads, or "Hot Leads," who are most likely to convert into paying customers. In response to this need, our task is to develop a Logistic Regression model that assigns a lead score between 0 and 100 to each lead. This score will enable the company to prioritize its sales efforts, focusing more on leads with higher scores, which indicate a greater likelihood of conversion. The ultimate goal of this case study is to build a predictive model that empowers X Education to target potential leads more effectively, ultimately aiming for a target lead conversion rate of approximately 80%. By implementing this model, X Education aims to significantly enhance its lead conversion process and maximize revenue generation opportunities.
### Data Overview:
https://docs.google.com/spreadsheets/d/1XYBs3H8TQWRCuhjyPaqePJWPHQYYLNoU/edit?usp=sharing&ouid=117516517112872589188&rtpof=true&sd=true

The dataset comprises various variables related to leads generated by X Education. Here's a brief description of each variable:

Certainly! Here's the description of each variable with the variable names bolded:

**Prospect ID**: Unique identifier for each prospect.

**Lead Number**: Unique identification number assigned to each lead.

**Lead Origin**: The origin or source from which the lead was generated.

**Lead Source**: The specific channel or platform through which the lead was acquired.

**Do Not Email**: Indicates whether the prospect has opted out of receiving emails.

**Do Not Call**: Indicates whether the prospect has opted out of receiving phone calls.

**Converted**: Binary variable indicating whether the lead was successfully converted (1) or not (0).

**TotalVisits**: Total number of visits made by the prospect to the website.

**Total Time Spent on Website**: Total time (in seconds) spent by the prospect on the website.

**Page Views Per Visit**: Average number of pages viewed per visit by the prospect.

**Last Activity**: Last recorded activity of the prospect.

**Country**: Country of the prospect.

**Specialization**: Area of specialization or interest of the prospect.

**How did you hear about X Education**: Source through which the prospect learned about X Education.

**What is your current occupation**: Occupation of the prospect.

**What matters most to you in choosing this course**: Key factors influencing the prospect's course selection.

**Search, Magazine, Newspaper Article, X Education Forums, Newspaper, Digital Advertisement, Through Recommendations, Receive More Updates About Our Courses**: Binary variables indicating whether the prospect was influenced by each respective channel.

**Tags**: Tags assigned to the lead based on various criteria.

**Lead Quality**: Quality assessment of the lead.

**Update me on Supply Chain Content, Get updates on DM Content**: Preferences of the prospect regarding content updates.

**Lead Profile**: Profile of the lead based on various attributes.

**City**: City of residence of the prospect.

**Asymmetrique Activity Index, Asymmetrique Profile Index, Asymmetrique Activity Score, Asymmetrique Profile Score**: Indices and scores related to asymmetrical profiling of the prospect.

**I agree to pay the amount through cheque**: Indicates whether the prospect agreed to pay through cheque.

**A free copy of Mastering The Interview**: Indicates whether the prospect is interested in receiving a free copy of the mentioned book.

**Last Notable Activity**: Last notable activity recorded for the prospect.


## Approach

For the project using Logistic Regression to assign lead scores, the approach can be structured as follows:

1. **Data Preprocessing**: 
   - Handle missing values: Impute or remove missing values in the dataset.
   - Encode categorical variables: Convert categorical variables into numerical format using techniques like one-hot encoding.
   - Feature scaling: Scale numerical variables to ensure they have a similar range.

2. **Feature Selection**:
   - Identify relevant features: Use techniques like correlation analysis, feature importance, or domain knowledge to select the most predictive features for lead scoring.
   
3. **Train-Test Split**:
   - Split the dataset into training and testing sets to evaluate the performance of the model.

4. **Model Training**:
   - Train a Logistic Regression model using the training data.
   - Tune hyperparameters: Use techniques like grid search or random search to find the optimal hyperparameters for the model.

5. **Model Evaluation**:
   - Evaluate the performance of the model using evaluation metrics such as accuracy, precision, recall, F1-score, and ROC-AUC score.
   - Use techniques like cross-validation to ensure the model's generalizability.

6. **Model Interpretation**:
   - Interpret the coefficients of the logistic regression model to understand the impact of each feature on lead scoring.
   - Analyze the odds ratios to identify the factors that contribute most to lead conversion.

7. **Lead Scoring**:
   - Use the trained logistic regression model to predict lead scores for new leads in the dataset.
   - Assign lead scores ranging from 0 to 100 based on the predicted probabilities of conversion.

8. **Model Deployment**:
   - Deploy the trained logistic regression model into the production environment to score new leads in real-time.
   - Monitor the model's performance regularly and retrain it periodically to ensure its effectiveness over time.


![image](https://github.com/jtndr26/Lead-Scoring/assets/78334379/74129a9f-dde0-47fe-b7c7-696ae7c6d473)
![image](https://github.com/jtndr26/Lead-Scoring/assets/78334379/309f5d56-485d-4016-a2cc-32a119fbc4ab)
![image](https://github.com/jtndr26/Lead-Scoring/assets/78334379/c24f56b3-a3ca-42de-9502-b946ec7339b0)



## **Result**: 

Based on the logistic regression model analysis, the Lead Score column has been created to represent the probability of a lead getting converted, with higher scores indicating a higher likelihood of conversion. The median lead score was found to be 33.0, suggesting that leads above this value have a better probability of enrollment. 

The variables identified as most influential in predicting potential buyers, in descending order of importance, are as follows:

1) **Total Time Spent on the Website:** Leads who spend more time on the website are more likely to convert, indicating a strong interest in the courses offered.
   
2) **Lead Origin_Lead Add Form:** Leads generated through the lead add form have a higher probability of conversion, likely due to their proactive engagement with the company's offerings.

3) **What is Your Current Occupation_Working Professional:** Working professionals are more likely to convert, possibly due to their intent to advance their careers through further education.

4) **Lead Source_Referral Sites:** Leads sourced from referral sites have a higher likelihood of conversion, indicating the importance of word-of-mouth marketing and recommendations from trusted sources.

Additionally, leads from India, students, and those who were approached via SMS also show potential for conversion. Leads generated from live chat and referral sites, particularly those who were referred, are also identified as promising candidates for enrollment.

By focusing efforts on engaging leads who exhibit these characteristics, X Education can significantly increase its conversion rate and expand its customer base. Leveraging these insights can help the company effectively target and nurture potential buyers, ultimately leading to greater success in selling their courses.

![image](https://github.com/jtndr26/Lead-Scoring/assets/78334379/44e620ad-5e35-48d2-9333-7089e8337555)

## **Conclusion**:
The logistic regression model reveals key insights into lead conversion for X Education. The top three features that significantly influence the target variable, i.e., the likelihood of lead conversion, are identified as Total Time Spent on Website, Lead Origin_Lead Add Form, and What is your current occupation_Working Professional. A threshold lead score of 33.0 is determined, above which leads have higher chances of conversion, providing a clear guideline for prioritizing leads. Moreover, the model achieves a commendable Recall Score of 80%, meeting the set target of 80% and indicating its efficacy in predicting lead conversion. Additional influential features include Lead Source_Referral Sites and Do Not Email_Yes, suggesting that targeting working professionals and visitors who spend more time on the site, along with students, could be advantageous strategies for lead targeting. By leveraging these insights, X Education can optimize its lead conversion efforts and focus on engaging with leads most likely to convert, thereby enhancing its overall sales performance and customer acquisition.





