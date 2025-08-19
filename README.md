# Yelp Reviews Analysis — Food & Beverage Segment  

## Overview  
This project explores what drives **high Yelp ratings (4.5 stars or higher)** for Food & Beverage businesses.  
The goal: move from messy Yelp data → clear, actionable insights that a restaurant owner or operator could use to improve performance.  

I used the [Yelp Open Dataset](https://www.yelp.com/dataset) and focused on **restaurants, cafes, bars, and specialty food businesses**.  

---

## Objectives  
1. **Identify drivers** of high ratings in Yelp reviews.  
2. **Translate findings** into practical recommendations for operators.  
3. **Highlight data gaps** where Yelp (or a business) should collect more info.  

---

## Workflow  

### 1. Data Loading & Cleaning  
- **What:** Loaded Yelp’s business dataset, filtered to Food & Beverage businesses.  
- **Why:** Raw data contained multiple categories (auto, shopping, gyms, etc.). We narrowed focus to restaurants and cafes since that’s most actionable for Yelp and Warmer’s scope.  
- **Steps taken:**  
  - Parsed business attributes (e.g., parking, delivery, price range).  
  - Handled missing values (e.g., “Parking” field often inconsistent).  
  - Standardized categories (merged “Café” and “Coffee & Tea” together).  

*Outcome:* A cleaned dataset focused on F&B with reliable attributes to analyze.  

---

### 2. Target Definition  
- **What:** Defined “high rating” as `stars > 4.5`.  
- **Why:** Business decisions are usually made around excellence — what separates “good” from “great.”  

*Outcome:* Binary target variable (`high_rating`) created for modeling.  

---

### 3. Exploratory Analysis  
- **What:** Looked at distributions of categories, star ratings, and attribute coverage.  
- **Why:** Before modeling, we need to know *what data we actually have* and where gaps exist.  
- **Example:** Parking info was missing for many businesses — a signal of data collection gaps.  

*Outcome:* Identified strong candidate features and flagged missing-data issues.  

---

### 4. Modeling Drivers of High Ratings  
- **What:** Used a logistic regression model with L1 regularization.  
- **Why:** This helps identify the *most important predictors* of high ratings, while avoiding overfitting.  
- **How we validated:** Cross-validation, a tree-based model, and SHAP importance (to double-check consistency).  

*Outcome:* Key drivers of high Yelp ratings included:  
- Cuisine type (e.g., bakeries, cafes, Japanese cuisine).  
- Operational features (delivery, good for groups, outdoor seating).  
- Venue type (bars and specialty shops outperformed generic categories).  

---

### 5. Translating Insights → Recommendations  
- **What:** Grouped findings into an **operational playbook**.  
- **Why:** Data science is only useful if it tells operators what to do.  
- **Examples:**  
  - Businesses with outdoor seating had higher odds of 5-star reviews → invest in patios where possible.  
  - Categories like bakeries and specialty food had outsized lift → niche offerings may outperform broad menus.  
  - Parking info is missing in many cases → Yelp should improve data capture to guide users better.  

*Outcome:* Actionable guidance for operators + ideas for Yelp product improvements.  

---

## Key Visuals  
*(Add inline screenshots/plots from your notebook here)*  

- Bar chart of **top drivers of high reviews**.  
- SHAP summary showing consistency of predictors.  
- Heatmap/table summarizing category performance.  

---

## Challenges & How They Were Addressed  
- **Messy attributes:** Parking data inconsistent → standardized via parsing.  
- **Sparse features:** Many businesses missing hours/delivery info → flagged in insights as a data collection issue.  
- **Model explainability:** Logistic regression chosen over black-box models for interpretability.  

---

## Next Steps  
If I had more time/data, I would:  
- Build an **interactive dashboard** for operators (filters by cuisine, region).  
- Explore **time-based patterns** (do openings/closings impact ratings?).  
- Add **geographic analysis** (are certain neighborhoods over/underperforming?).  

---

## Takeaways  
1. Data confirms: **Operational choices (delivery, outdoor seating) directly affect Yelp ratings.**  
2. **Niche offerings outperform broad menus** — specialization is rewarded.  
3. **Data gaps (like parking info)** limit insights — better data capture would benefit both Yelp and businesses.  

---
