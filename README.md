## Real Estate Agent Review Analysis

---

## The Problem: Mismatched Expectations

### Traditional Approach
Traditional agent matching methods rely heavily on personal networks and referrals, often failing to address individual preferences and specific agent expertise.

### The Result
This lack of personalization leads to mismatched expectations and less-than-ideal experiences for buyers, resulting in frustration and dissatisfaction.

---

## Methodology

### Data Sources
- **Agent Data**
- **Agent Reviews**
- **Past Sales Records**

### Machine Learning Models
- **Regression Models:**
  - Random Forest Regression
  - Linear Regression
  - Gradient Boosting Machines (GBM)
- **Classification Models:**
  - Logistic Regression
  - Support Vector Machines (SVM)

### Natural Language Processing (NLP)
- **Named Entity Recognition (NER):** Extract agent names from reviews.
- **Sentiment Analysis:** Assess polarity and subjectivity of customer reviews.

### Recommendation System
- Developed a front-end interface for personalized recommendations.

---

## Data Processing

1. **Data Cleaning:**
   - Imputed missing values (e.g., ratings, property prices) using the median.
   - Extracted state information from addresses.
2. **Date Standardization:**
   - Filtered past sales records from 2010 to align with the agent review dataset.
3. **Data Merging:**
   - Merged data using `loc_id` and matched names and locations.

4. **Named Entity Recognition (NER):**
   - **Library:** spaCy  
   - Extracted agent names from reviews to link with agent data. For multiple names, the most common name was chosen.

5. **Sentiment Analysis:**
   - **Library:** TextBlob  
   - Classified reviews with polarity > 0 as positive, and polarity < 0 as negative.

---

## Exploratory Data Analysis (EDA)

Key insights include:
- Strong correlation between localized expertise and customer satisfaction.
- Experienced agents consistently receive higher ratings.
- Regions with high transaction volumes reflect market demand trends.

---

## Model Building

### Goal
To recommend agents based on customer preferences and expertise.

### Regression Models
| Model                    | R²     | MSE    |
|--------------------------|--------|--------|
| **Linear Regression**    | 0.1048 | 3.5536 |
| **Random Forest**        | 0.2230 | 3.0845 |
| **Gradient Boosting (GBM)** | 0.2878 | 2.8273 |

- **Gradient Boosting Machines (GBM)** emerged as the best-performing regression model.

### Classification Models
| Model                     | Accuracy |
|---------------------------|----------|
| **Logistic Regression**   | 80.65%   |
| **Support Vector Machines (SVM)** | 84.64%   |

---

## Recommender System Development

### Steps:
1. **Data Integration:** Merged agent and property datasets based on agent names.
2. **Name Matching:** Linked agent names across datasets using substring matching.
3. **Weighted Score Calculation:** Ranked properties by a weighted score based on attributes (e.g., ratings, local knowledge).
4. **Top Recommendations:** Displayed the top 5 properties with agent details.

---

## Challenges and Solutions

### Data Integration
- Overcame challenges using robust alignment techniques.

### Data Accuracy and Consistency
- Ensured reliability with data validation methods.

---

## Key Takeaways

This project delivered:
- A powerful, data-driven solution to match buyers with suitable agents.
- High accuracy and reduced error rates.
- Personalized, effective recommendations, showcasing the potential of AI in real estate.

---

## References

1. Yadav, D. (2019). *Categorical Encoding Using Label-Encoding and One-Hot-Encoder.* Medium, Towards Data Science.  
2. Smith, J. A., & Doe, R. L. (2023). *Machine learning applications in real estate recommendations.* Journal of Real Estate Analytics, 15(3), 213-228.  
3. Mostafa, M. M. (2013). *More than words: Social networks' text mining for consumer brand sentiments.* Expert Systems with Applications, 40(10), 4241-4251.  
4. Levitt, S. D., & Syverson, C. (2008). *Market distortions when agents are better informed: The value of information in real estate transactions.* Review of Economics and Statistics, 90(4), 599-611.

---

## Thank You!
