# RFM Churn Risk Analyzer

The **RFM Churn Risk Analyzer** uses RFM (Recency, Frequency, Monetary) analysis to identify customers at risk of churn.  
The project consists of **three interconnected Tableau dashboards** that allow business owners to monitor customer health, prioritize retention efforts, and make data-driven decisions to strengthen long-term customer relationships.

---

## 🤖 Sales Simulation Bot (`next_sale_bot.ipynb`)

- Simulates **future sales events** based on historical RFM purchasing behavior  
- Generates realistic invoices, products, prices, and quantities  
- Automatically updates customer RFM metrics after each transaction  
- Recalculates churn risk and customer importance scores in real time  
- Keeps Tableau dashboards continuously **live and analytics-ready**

This bot acts as the data engine for the RFM Churn Risk Analyzer by continuously feeding evolving transactional data into the system.

---

## 📊 Tableau Dashboards (`RFM_Churn_Risk_Analyzer.twb`)

- Three interconnected dashboards focused on:
  - Customer segmentation
  - Churn risk identification
  - Retention prioritization

---

## 🛠 Tools & Technologies

- **Tableau Desktop & Tableau Server**
- **Database:** PostgreSQL
- **Analytics:** RFM Analysis (Recency, Frequency, Monetary)
- **Data preparation:** SQL

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
