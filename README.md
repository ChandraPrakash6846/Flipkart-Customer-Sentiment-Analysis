# Flipkart iPhone 16 Customer Sentiment Analysis

## Project Overview
This project is an end-to-end **Sentiment Analysis and Web Scraping case study** on Flipkart customer reviews for the **Apple iPhone 16 (128GB)**. The objective was to transform raw, unstructured customer reviews into structured insights using **Python, NLP, and Data Visualization**.

The workflow covers:
* Dynamic web scraping using Selenium
* Text preprocessing using NLTK
* Sentiment classification using TextBlob
* Statistical analysis and visualization
* Business insight generation

---

## Business Problem
As a Data Analyst, the goal was to analyze customer feedback to help stakeholders:

* Understand overall customer sentiment toward the product.
* Identify key drivers of positive and negative reviews.
* Measure the relationship between star ratings and textual sentiment.
* Detect recurring product issues for improvement strategy.

---

## Project Execution & Methodology

### A. Data Collection (Web Scraping)

Customer reviews were scraped dynamically from Flipkart using Selenium and BeautifulSoup.

* Automated browser navigation across multiple review pages.
* Extracted:
  * `reviewer_name`
  * `review_rating`
  * `review_text`
* Removed duplicate reviews using composite keys.
* Exported cleaned dataset to CSV for further analysis.

Key Techniques:
* Selenium for dynamic content loading
* BeautifulSoup for HTML parsing
* Duplicate detection using tuple-based uniqueness logic

---

### B. Data Cleaning & Preprocessing

To prepare text data for sentiment analysis, the following transformations were applied:

* Removed duplicate records.
* Converted text to lowercase.
* Removed punctuation and special characters using regex.
* Tokenized text using NLTK.
* Removed English stopwords.
* Applied WordNet lemmatization.
* Converted `review_rating` to numeric format.
* Created new feature: `review_length` (word count).

Generated new columns:
* `clean_review`
* `sentiment`
* `review_length`

---

### C. Sentiment Classification

Sentiment polarity was calculated using **TextBlob**.

Classification Rule:
* Polarity ≥ 0.1 → Positive
* Polarity < 0.1 → Negative

This approach converts subjective review text into measurable sentiment categories.

---

### D. Data Analysis & Business Insights

Several analytical techniques were applied:

* **Sentiment Distribution Analysis**
  * Counted Positive vs Negative reviews.
  * Visualized using bar charts.

* **Sentiment vs Star Rating**
  * Calculated average rating per sentiment class.
  * Measured alignment between textual sentiment and star ratings.

* **Review Length Analysis**
  * Compared review length across sentiment categories.
  * Identified whether longer reviews indicate stronger sentiment.

* **Keyword Pattern Detection**
  * Extracted high-frequency terms in positive reviews.
  * Extracted complaint clusters in negative reviews.

---

## Technologies & Skills

* **Programming Language:** Python
* **Web Scraping:** Selenium, BeautifulSoup
* **Data Processing:** Pandas, NumPy
* **NLP:** NLTK, TextBlob
* **Visualization:** Matplotlib, Seaborn
* **Core Competencies:**  
  * Web Scraping Automation  
  * Text Preprocessing  
  * Sentiment Modeling  
  * Feature Engineering  
  * Exploratory Data Analysis  
  * Business Insight Extraction  

---

## Key Insights & Impact

The analysis revealed several strategic findings:

* **Majority Positive Reception:** Most reviews show positive sentiment toward the product.
* **Strong Rating-Sentiment Alignment:** Higher star ratings strongly correlate with positive polarity.
* **Positive Drivers:**
  * Camera quality
  * Performance
  * Battery life
  * Display quality
* **Negative Drivers:**
  * High price perception
  * Heating issues
  * Battery drain
  * Charging problems

These insights can directly support:

* Product improvement prioritization
* Pricing strategy evaluation
* Marketing message optimization
* Brand perception monitoring

---

## Challenges Faced

* Handling dynamic page loading on Flipkart.
* Dealing with inconsistent HTML structure.
* Removing duplicate reviews across pages.
* Cleaning noisy, user-generated textual data.
* Managing missing reviewer information.

---

## Future Enhancements

* Add Neutral sentiment classification.
* Implement VADER for improved social media text handling.
* Deploy interactive dashboard using Streamlit or Power BI.
* Automate scraping with scheduling.
* Apply topic modeling (LDA) for deeper thematic clustering.

---

## Mentorship

This project was completed under the guidance of **WsCube Tech** as part of the Data Analytics curriculum, focusing on real-world, industry-aligned implementation of Web Scraping and NLP.
