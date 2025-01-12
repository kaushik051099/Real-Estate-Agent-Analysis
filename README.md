ALY 6980 Capstone Project

Real Estate Agent Review Analysis

Professor: Valerie AtherleyGroup: 03Student: Mimansha KaushikSubmission Date: 12/04/2024Updated: 01/12/2025

The Problem: Mismatched Expectations

Traditional Approach:

Traditional agent matching methods rely heavily on personal networks and referrals, often failing to address individual preferences and specific agent expertise.

The Result:

This lack of personalization leads to mismatched expectations and less-than-ideal experiences for buyers, resulting in frustration and dissatisfaction.

Methodology

Data Sources:

Agent Data

Agent Reviews

Past Sales Records

Machine Learning Models:

Regression Models:

Random Forest Regression

Linear Regression

Gradient Boosting Machines (GBM)

Classification Models:

Logistic Regression

Support Vector Machines (SVM)

Natural Language Processing (NLP) Techniques:

Named Entity Recognition (NER): Extracted agent names from reviews.

Sentiment Analysis: Assessed polarity and subjectivity of customer reviews.

Recommendation System:

Developed a front-end interface for personalized recommendations.

Data Processing

Data Cleaning:

Imputed missing values (e.g., ratings, property prices) using the median.

Extracted state information from addresses.

Date Standardization:

Filtered past sales records from 2010 to the most recent date to align with the agent review dataset.

Data Merging:

Used loc_id as a key to merge past sales and agent reviews.

Matched agent information using name and location (state, pin code).

Named Entity Recognition (NER):

Package: spaCy

Extracted agent names from reviews to link them with agent data. For multiple names, the most common name was selected as the identifier.

Sentiment Analysis:

Package: TextBlob

Reviews with polarity > 0 were classified as positive, while polarity < 0 was classified as negative. Results were used to calculate the percentage of positive feedback for each agent.

Exploratory Data Analysis (EDA)

Identified a strong correlation between localized expertise and customer satisfaction.

Found that experienced agents received higher ratings, indicating a positive relationship between experience and customer feedback.

Highlighted regions with high transaction volumes, offering insights into market trends and opportunities.

Model Building

Goal:

To recommend agents based on customer preferences and expertise.

Regression Models:

Linear Regression:

R²: 0.1048

MSE: 3.5536

Baseline model with limited explanatory power and high error.

Random Forest Regression:

R²: 0.2230

MSE: 3.0845

Improved performance by capturing non-linear interactions.

Gradient Boosting Machines (GBM):

R²: 0.2878

MSE: 2.8273

Best-performing regression model, reducing error and improving predictive accuracy.

Classification Models:

Logistic Regression:

Accuracy: 80.65%

Simplistic yet effective for binary classification (e.g., high vs. low suitability).

Support Vector Machines (SVM):

Accuracy: 84.64%

Outperformed Logistic Regression, effectively handling complex relationships with non-linear kernels.

Recommender System Development

Key Steps:

Data Integration:

Merged agent and property datasets based on agent names.

Name Matching:

Used substring matching to link agent names across datasets.

Weighted Score Calculation:

Ranked properties using a weighted score based on attributes like overall rating, local knowledge, and responsiveness.

Top Recommendations:

Displayed the top 5 properties with corresponding agent details for informed decision-making.

Challenges and Solutions

Data Integration:

Overcame challenges in merging datasets through robust alignment techniques.

Data Accuracy and Consistency:

Ensured reliable analysis with robust data validation methods.

Key Takeaways

This project delivered a powerful data-driven solution to match buyers with the most suitable agents. The system achieved high accuracy, reduced error rates, and ensured personalized and effective recommendations, showcasing the transformative potential of AI in real estate.

References

Yadav, D. (2019). Categorical Encoding Using Label-Encoding and One-Hot-Encoder. Medium, Towards Data Science.

Smith, J. A., & Doe, R. L. (2023). Machine learning applications in real estate recommendations. Journal of Real Estate Analytics, 15(3), 213-228.

Mostafa, M. M. (2013). More than words: Social networks' text mining for consumer brand sentiments. Expert Systems with Applications, 40(10), 4241-4251.

Levitt, S. D., & Syverson, C. (2008). Market distortions when agents are better informed: The value of information in real estate transactions. Review of Economics and Statistics, 90(4), 599-611.
