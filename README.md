# Yelp Business Success Analysis  

## Project Overview  
This project explores the **Yelp Open Dataset** to identify what factors make Food & Beverage businesses highly successful (defined as **≥4.5 stars with 20+ reviews**).  

I performed data cleaning, exploratory analysis, feature engineering, and built predictive models to identify **key success drivers and risk factors**. Finally, I translated model results into an **operator playbook** that provides actionable recommendations for businesses.  

---

## Repository Structure  

### Key Files  
- **`analysis.ipynb`**  
  - The full technical notebook containing **all analysis steps**: parsing raw JSON, cleaning, EDA, feature engineering, modeling, validation, and outputs.  
  - Use this if you want to **reproduce the entire pipeline**.  

- **`analysis_overview.ipynb`**  
  - An **index-style notebook** with a step-by-step summarization of the workflow.  
  - Explains *what* was done and *why*, without the heavy technical details.  
  - Use this as a **quick entry point** into the project.  

- **`yelp_data_summarization.pdf`**  
  - The **presentation deck** summarizing the overarching project, findings, and recommendations.  

---

### Folders  
- **`Yelp-JSON/`**  
  - Original raw dataset folder (not fully uploaded to save memory).  
  - Used as the starting point for analysis.  

- **`outputs/`**  
  - Contains all processed data outputs generated from `analysis.ipynb`.  
  - **Note:** The large file `business_clean.csv` is excluded due to size.  

  Inside `outputs/food_&_beverage/`:  
  - **Q1 outputs** → results from *“What variables are most strongly correlated with success?”* (performance drivers).  
  - **Q2 outputs** → results from *operational recommendations*, including the **playbook CSV** and supporting charts.  

---

## How to Navigate  
1. Start with **`analysis_overview.ipynb`** → high-level understanding of the project flow.  
2. Dive into **`analysis.ipynb`** if you want the **full technical details** and data processing steps.  
3. Review **`yelp_data_summarization.pdf`** for the **executive summary** and visual storytelling.  
4. Explore the **`outputs/` folder** for datasets and charts used in Q1 (drivers) and Q2 (recommendations).  

---

## Key Deliverables  
- **Clean dataset pipeline** from messy JSON to structured analysis-ready tables.  
- **Feature engineering** to standardize categories, fix overlaps, and normalize biases.  
- **Predictive modeling** (logistic regression + refinements).  
- **Playbook CSV** → a prioritized list of business levers (success drivers & risks) with recommended actions and A/B test designs.  
- **Final presentation** highlighting challenges, findings, and actionable recommendations.  
