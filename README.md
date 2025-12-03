# CF-Gun-Violence-Analysis (Python & Tableau)

Python + Tableau analysis of multi-year Gun Violence Archive data to explore where, when, and how severely gun violence incidents occur in the U.S. The project combines web-scraped incident-level data, exploratory analysis in Python, and an interactive Tableau story to support a hypothetical national public safety nonprofit in prioritizing prevention efforts.

This repo contains reproducible notebooks, a tidy data pipeline, and clear visuals that move from early exploration (EDA, correlation, clustering) to more actionable geographic and time-based insights.

🔗 **Interactive Tableau Story:** [View the dashboard on Tableau Public](https://public.tableau.com/views/GunViolenceintheUnitedStates_17647715349050/GUNVIOLENCESTORY?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
---

## Disclaimer

This repository is a practice project for CareerFoundry (CF). It uses incident-level data from the publicly available Gun Violence Archive (GVA), accessed via web scraping for educational purposes. The analysis is for learning only and is **not** affiliated with or endorsed by the Gun Violence Archive or any nonprofit or governmental organization.

---

## Objective

A national public safety nonprofit wants to understand where and when gun violence is most concentrated, and how severe incidents tend to be.  
My task is to perform an exploratory data analysis of multi-year GVA incident data using Python, then build a Tableau storyboard that:

- Explains the scale and distribution of incidents and victims.
- Documents analytical approaches that **did not** yield strong insights (e.g., correlation and clustering).
- Highlights clearer patterns by geography and time that can guide prevention and outreach.

---

## Key Questions

- **Distribution:** How are incidents and victims distributed across U.S. states?  
- **Timing:** When do incidents spike across months and years, and how does partial 2018 data affect the pattern?  
- **Severity:** How severe are incidents in terms of numbers killed, injured, and total victims?  
- **Relationships:** Do things like the number of guns involved and where an incident happens seem strongly linked to how many people are killed or injured?  
- **Methods:** Which analytical approaches (correlation, clustering, geographic and time-based views) are most useful for non-technical stakeholders?

---

## Data

- Multi-year incident-level data from the **Gun Violence Archive**, accessed via a **Kaggle dataset** that compiles GVA records from 2013–2018.
- The Kaggle dataset maintainer performed the original web scraping from GVA and shared the combined CSV files; this project uses that compiled version rather than scraping GVA directly.
- Fields include:
  - Incident date, state, city/county, latitude, longitude  
  - Number killed (`n_killed`), number injured (`n_injured`)  
  - Number of guns involved (`n_guns_involved`)  

- The dataset includes both shooting and some non-shooting events (e.g., gun buybacks), and `n_guns_involved` has substantial missing data. These are treated as important limitations in the analysis and Tableau story.

> **Note:** This project is for educational purposes only and does not attempt to make causal claims.

---

## Deliverables

- **Python notebooks** for:
  - Cleaning, wrangling, and exploratory analysis (EDA).
  - Correlation analysis (heatmap) and clustering experiments (k-means).  

- **Analytical findings**, including:
  - Descriptive statistics and distribution summaries for killed, injured, and guns involved.  
  - Correlation heatmap showing weak linear relationships between severity, guns, and location.  
  - Clustering attempts that yielded overlapping, hard-to-interpret groups.  
  - Aggregations by state and month to reveal geographic concentration and seasonality.

- **Tableau storyboard** that:
  - Presents key KPIs (incidents, killed, injured, total victims) and time trends.  
  - Documents “failed” or less useful approaches (correlation + clustering) and explains why they weren’t chosen.  
  - Highlights clearer, actionable views by **state** (where incidents are concentrated) and **month** (when incidents spike).  
  - Ends with a summary, limitations, and recommendations for further analysis (e.g., rates per population, separating shooting vs. non-shooting incidents).

---

## Tools Used

- **Language:** Python 3.x  
- **Data handling:** pandas, numpy, os, json  
- **Visualization:** matplotlib, seaborn, pylab  
- **Mapping:** folium  
- **Machine learning:** scikit-learn (KMeans, StandardScaler)  
- **Statistical modeling:** statsmodels (via `statsmodels.api` as `sm`)  
- **Environment:** Jupyter Notebook
- **Visualization & BI:**  
  - **Tableau** (storyboard, dashboards, maps, BANs)

---

## About

Python + Tableau analysis of Gun Violence Archive data to explore incident severity, geography, and seasonality. The project emphasizes transparent analytical thinking: starting with broad EDA, documenting methods that didn’t provide clear answers (correlation, clustering), and ending with more interpretable, stakeholder-ready views in Tableau to support data-informed public safety decisions.

---

## Tableau Story

The final findings are presented in an interactive Tableau storyboard that walks through:

- Overall KPIs and trends (incidents, killed, injured, total victims)  
- Correlation and clustering attempts that were not very useful  
- State-level concentration of incidents  
- Seasonality and partial 2018 effects  
- Summary, limitations, and next steps  

👉 [View the Tableau story on Tableau Public](https://public.tableau.com/views/GunViolenceintheUnitedStates_17647715349050/GUNVIOLENCESTORY?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

