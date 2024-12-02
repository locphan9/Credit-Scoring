# Credit-Scoring
Build AI Model on public credit risk data set to segment credit scoring

Data set used: [Kaggle credit risk data set](https://www.kaggle.com/datasets/laotse/credit-risk-dataset/data)

For more details on how the model is trained: [Phan, Credit Risk](https://github.com/locphan9/Credit-Scoring/edit/main/)

## Visualization
![image](https://github.com/user-attachments/assets/c264ad3d-ba46-4b83-b6df-bd05ab43b877)
Number of Records: The dataset contains information on borrowers, including personal and financial data relevant to credit scoring.

### Columns:
**Person's Information:**
- person_age: Age of the borrower.
- person_income: Annual income of the borrower.
-person_home_ownership: Home ownership status of the borrower (e.g., OWN, RENT).
- person_emp_length: Employment length (in years) of the borrower.
**Loan Details:**
- loan_intent: Intended use of the loan (e.g., EDUCATION, BUSINESS).
- loan_grade: The loan grade assigned (A-E), based on credit risk.
- loan_amnt: The amount of the loan requested.
- loan_int_rate: Interest rate on the loan.
- loan_percent_income: The proportion of income required for the loan.
**Credit History:**
- cb_person_default_on_file: Historical record of default (0: No, 1: Yes).
- cb_preson_cred_hist_length: Length of credit history in years.
- Loan Status:
- loan_status: The status of the loan (0: Non-default, 1: Default).
**Target Variable:**

- loan_grade: A categorical feature representing the loan grade (A-E), used as the primary variable for prediction.
### Potential Use
The dataset can be used for classification tasks such as credit scoring, where the goal is to predict the loan_grade based on the borrower's financial and personal information.

### Imbalance
The dataset may contain imbalanced data regarding loan defaults (i.e., the number of defaults might be lower compared to non-defaults).


## Credit Risk Weights
![image](https://github.com/user-attachments/assets/d297c833-b1db-4edd-b53b-465e22ad5453)
The model puts heaviest emphasis on three dimensions: loan interest rate, historical default, and loan amount at the importance of 0.6, 0.3, 0.02 respectively. 

### 1. Credit Risk Department
Focus: Historical Default (0.3 importance)

**Actionable Item:**
Refine Historical Default Monitoring: The model places significant importance on historical default, so ensure that any borrower with a past default history is carefully assessed.
**Recommendation:** Review the records of borrowers with a history of defaults and explore targeted risk mitigation strategies, such as offering lower loan amounts or higher interest rates to those with a higher default risk.
**Action:** Implement stricter approval criteria or adjust the loan terms for individuals with a historical default on file.
### 2. Pricing/Finance Department
Focus: Loan Interest Rate (0.6 importance)

**Actionable Item:**
- **Adjust Loan Interest Rate Strategy:** Since the model gives the loan interest rate the highest importance, make sure the interest rate is adjusted to reflect the risk associated with each borrower.
- **Recommendation:** Use dynamic pricing models to determine the most appropriate loan interest rates based on the borrower's financial profile and historical data.
- **Action:** Monitor and regularly adjust interest rates based on changes in market conditions and borrower risk profiles.
### 3. Loan Approval Department
Focus: Loan Amount (0.02 importance)

- **Actionable Item:**
- **Assess Loan Amount Requests:** While loan amount has a lower importance, it is still relevant. Ensure that the loan amounts requested align with the borrower's income, creditworthiness, and the intended loan grade.
- **Recommendation:** Conduct a thorough review of loan amount requests to avoid overexposure. For higher-risk borrowers, consider approving smaller loan amounts to mitigate potential default risk.
- **Action:** Implement automated checks to flag loan amount requests that appear excessive relative to the borrower's financial standing.
### 4. Marketing Department
- **Focus:** Loan Interest Rate & Historical Default (Primary Factors)

- **Actionable Item:**
Targeted Marketing Campaigns: Use the insights from the model to create tailored marketing strategies. For borrowers with a clean credit history and lower default risks, promote lower-interest loans. For borrowers with historical defaults, focus on building trust and offering products designed to help rebuild their credit score.
- **Recommendation:** Develop targeted loan offers based on risk profiling—lower rates for "A" or "B" grade borrowers, and higher rates with more customized offers for "C", "D", and "E" grade borrowers.
- **Action:** Design promotional campaigns around specific loan products that cater to each group’s risk profile, ensuring borrowers see a clear value proposition for their credit situation.
### 5. Data Science & Analytics Department
Focus: Historical Default, Loan Interest Rate, Loan Amount

- **Actionable Item:**
- **Model Refinement:** Given the model's heavy emphasis on these three dimensions, consider refining the feature engineering process by adding more granular data (e.g., credit score, payment history, income variability) to improve predictive accuracy.
Recommendation: Review the weights and importance scores periodically to ensure they reflect actual risk behaviors and adjust features accordingly.
- **Action:** Continuously retrain the model with updated data and ensure that the model is adaptable to shifts in borrower behavior or economic conditions.
### 6. Customer Service Department
- **Focus:** Loan Interest Rate, Historical Default

- **Actionable Item:**
- **Customer Support for Risky Borrowers:** Ensure that customer service representatives are trained to handle sensitive conversations with borrowers who have been assigned higher interest rates or those flagged for historical defaults. Provide support with explanations of why certain rates were applied.
- **Recommendation:** Develop scripts for customer service reps to address customer concerns about loan terms and default history.
- **Action:** Offer financial counseling to borrowers with higher loan interest rates and work on building their trust in the loan process.
### General Recommendations for All Departments:
- **Collaborative Action:** Establish cross-departmental collaboration (e.g., between credit risk, marketing, and customer service) to ensure that insights from the model are fully utilized across the business processes.
- **Regular Review:** Periodically review the model’s output and performance to ensure the risk factors align with the latest financial data and market conditions.
- **Transparency:** Make sure that loan terms and conditions (especially interest rates) are transparent to borrowers, helping them understand how their credit risk affects their loan terms.
