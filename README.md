## 🤖 Sales Simulation Bot (next_sale_bot.ipynb)

- Simulates **future sales events** using historical RFM purchasing patterns  
- Generates realistic invoices, products, prices, and quantities  
- Automatically updates customer RFM metrics after each transaction  
- Recalculates churn risk and importance scores in real time  
- Keeps Tableau dashboards continuously **live and analytics-ready**  

This bot powers the RFM Churn Risk Analyzer by feeding it realistic, evolving transactional data.

# RFM Churn Risk Analyzer (RFM_Churn_Risk_Analyzer.twb)

**RFM Churn Risk Analyzer** leverages RFM (Recency, Frequency, Monetary) analysis to identify clients who are at risk of being lost by the business. This project comprises **three interconnected Tableau dashboards**, enabling business owners to proactively monitor at-risk clients, make data-driven retention decisions, and strengthen long-term customer relationships.


---

## Tools & Technologies
- **Tableau Desktop & Tableau Server**  
- **Data source:** PostgreSQL
- **Analytics methods:** RFM Analysis (Recency, Frequency, Monetary)  
- **Optional:** SQL for data preparation  

---

## Dashboards

### 1. Overview Dashboard

**Purpose:** Displays the top 100 clients ranked by importance score.  
<img width="1439" height="786" alt="Screenshot 2026-01-15 at 10 47 19 PM" src="https://github.com/user-attachments/assets/49e00a74-38a6-4ccc-accf-ff10957bee10" />

**Key Features:**
- Filter by **“Risky to Lose”** indicator  
- Clickable client entries to navigate to the **Breakdown Dashboard**  
- Quick identification of high-value clients at risk  

**Insights:**  
- Quickly highlights which clients require immediate attention  
- Prioritizes retention efforts based on importance score

**Additional KPI's:**
- Number of customers filtered
- New customers today
- RTL customers

---

### 2. Breakdown Dashboard
<img width="1438" height="791" alt="Screenshot 2026-01-15 at 10 47 32 PM" src="https://github.com/user-attachments/assets/f71f0d05-3be3-451a-85b1-8230ee695545" />

**Purpose:** Provides a detailed view of a selected client’s spending patterns.  

**Key Features:**
- Daily spending graph for the selected client  
- KPI section showing key metrics and insights  
- Personalized **recommendations and actions** based on client rank and risk status  
- Option to select a specific day to dive deeper into spending history  

**Insights:**  
- Enables targeted retention strategies per client  
- Visualizes trends in spending and engagement  

---


### 3. Invoice Detail Dashboard
<img width="1440" height="789" alt="Screenshot 2026-01-15 at 10 47 42 PM" src="https://github.com/user-attachments/assets/68b3ec16-3f04-44ec-8093-79cfa68c4060" />
  
**Purpose:** Shows a granular breakdown of all invoices for a selected day.  

**Key Features:**
- Item-level details for every transaction  
- Full transparency into client purchasing behavior  

**Insights:**  
- Helps understand the composition of client purchases  
- Supports actionable decisions for promotions or interventions
- Includes insightful tooltip that contains the amount spent per item, and the entire invoice grouped

---

## Data
- **Source:** PostgreSQL database   
- **Refresh:** Live Connection
- **Notes:** Data anonymized for privacy  

---

## Limitations & Assumptions
- Analysis based on historical invoices only  
- RFM scoring assumes recency, frequency, and monetary metrics are equally weighted  
- Personalized recommendations are generated based on rules; not predictive modeling  
- Data anonymized; actual client identifiers are replaced with unique IDs  


---

## Usage Instructions
1. Start on the **Overview Dashboard** to identify top clients at risk.  
2. Click on a client to open the **Breakdown Dashboard**.  
3. Select a day in the spending graph to see **Invoice Detail Dashboard** for granular analysis.  
4. Use filters to adjust date ranges or risk categories as needed.  
