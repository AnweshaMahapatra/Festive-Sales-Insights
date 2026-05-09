# 📊FESTIVE SALES Analysis  
### MySQL & Power BI | Diwali 2023 & Sankranti 2024  

> 🎯 *A two-part analytical project examining promotional effectiveness using MySQL (analysis) + Power BI (visual storytelling) to improve future festive campaign decisions.*

---

## LIVE DASHBOARD LINK :
https://app.powerbi.com/groups/me/reports/10bec79c-50ed-4ad3-8cc0-723dceef87ad?pbi_source=desktop

# 🧾 Overview

- 🏬 AtliQ Mart ran promotional campaigns during **Diwali 2023** and **Sankranti 2024**
- 🎉 Promotions included: discounts, cashback, BOGOF, bundle offers
- 📊 Objective: Evaluate **what actually worked and what destroyed value**

### 📌 Key Results
- 💰 Incremental Revenue (IR): **₹155M**
- 🚀 Revenue Growth: **211.28%**
- 📦 Incremental Units Sold (ISU): **442K**
- 📈 Volume Uplift: **110.10%**

👉 But the real insight:  
✔ Some promotions drove massive profit  
❌ Some destroyed revenue  
⚠ Some cities underperformed completely  

---

# 🎯 Business Questions

- 🏙️ Which state had the **highest revenue increase?**
- 🎁 Which promotion had the **highest IR & ISU?**
- ❌ Which promotion performed the **worst?**
- 📦 Which products had the **highest & lowest lift?**

👉 No single system existed earlier to answer all of these together.

---

# 🏗️ Project Structure

## 🧠 Part 1 MySQL (Analysis Layer)
- Run ad-hoc SQL queries
- Answer business questions directly
- Analyze:
  - Products
  - Stores
  - Cities
  - Promotions
  - Campaigns

---

## 📊 Part 2 Power BI (Visualization Layer)
- Import MySQL data into Power BI
- Build relationships using keys:
  - `product_code`
  - `store_id`
  - `campaign_id`
- Create dashboards + KPIs

---

# ⚙️ Steps Followed

## 🧱 Step 1 Data Load (MySQL)
- Loaded raw tables:
  - `fact_events`
  - `dim_stores`
  - `dim_products`
  - `dim_campaigns`

---

## 🔍 Step 2 Ad-Hoc SQL Analysis
- Identified:
  - 🛒 High-value BOGOF products (> ₹500)
  - 🏬 Store distribution by city
  - 📊 Campaign performance (before vs after)
  - 📦 Category ISU% ranking (Diwali)
  - 🏆 Top products by IR%

---

## 📥 Step 3  Power BI Import
- Imported all tables
- Built relationships between fact & dimensions

---

## 🧮 Step 4 DAX Measures

### 📦 Quantity After Promotion
- BOGOF doubles units

### 💰 Revenue After Promotion
- Promo-aware revenue logic:
  - BOGOF → 50% pricing logic
  - Cashback → fixed ₹500 reduction
  - Discounts → % based reduction

### 📊 Key KPIs
- Revenue Before Promotion
- Incremental Units Sold (ISU)
- Incremental Revenue (IR)
- IR %
- ISU %

---

## 📊 Step 5 Dashboard Pages

### 🏬 Page 1 Store Performance

<img width="936" height="568" alt="Store performance analysis" src="https://github.com/user-attachments/assets/663b8092-7240-4949-9eba-59934a396bfb" />


- 📉 Bottom stores by IR & ISU
- 🏙️ City-wise IR% ranking
- 🛒 Category performance per store

---

### 🎁 Page 2 Promotion Analysis

<img width="790" height="512" alt="P analysis" src="https://github.com/user-attachments/assets/4ac9a639-6fdf-4f1e-af11-4ffc197fffbe" />


- 📊 IR & ISU by promotion type
- 🪔 Diwali vs 🌾 Sankranti comparison
- 💡 Promo effectiveness comparison

--


### 📦 Page 3 Product & Category Insights

<img width="795" height="499" alt="A" src="https://github.com/user-attachments/assets/16750dca-ecf4-4f49-8e6d-f38bf9972357" />


- 📦 Category-level before/after performance
- 🏆 Top 5 products by IR & ISU

---

# 🔑 Key Findings

---

## 🏙️ Cities & Stores
- 🥇 Madurai: **120% IR% (Top performer)**
- ❌ Visakhapatnam: **94.39% IR% (Only negative city)**
- 🏙️ Bengaluru: Most stores (10)
- 🏚️ Vijayawada & Trivandrum: Least stores (2 each)

---

## 🎁 Promotion Performance

### 🏆 Best Promotions
- 💳 500 Cashback → **₹91M IR (Best revenue driver)**
- 📦 BOGOF → **372K ISU (Best volume driver)**

---

### ❌ Worst Promotions
- ❌ 25% OFF → –₹3M
- ❌ 33% OFF → –₹2M
- ❌ 50% OFF → –₹1M

👉 Insight:
- Discounts = revenue loss
- Volume gain was NOT enough to compensate

---

## 📦 Category Insights

🔌 Home Appliances:

- 🚀 IR%: **265.21%**
- 📈 ISU%: **628.78% (Highest spike)**

🧴 Personal Care:

- ❌ IR%: **–34.20% (Only negative category)**
- 🛒 Grocery & Staples:
- 📉 Very low incremental lift

---

## 🏆 Top Products

- 🥇 Atliq Waterproof Immersion Rod → **266.19% IR%**
- 🧺 Atliq Farm Chakki Atta (1KG) → **118K units sold**
- 🎁 Home Essential Combo → **₹91M IR (Highest revenue product)**

---

# 📁 Repository Structure

- 📄 README.md → Overview
- 📄 Steps_Followed.md → Full workflow
- 📄 SQL_and_DAX_Reference.md → Queries + formulas
- 📄 Story Behind Dashboard.md → Business narrative
- 📄 Business Questions.md → Insights Q&A

---

# 🛠️ Tools Used

- 🐬 MySQL Workbench → Data analysis
- 📊 Power BI → Visualization
- 🧮 DAX → KPI calculations
- 💻 GitHub → Portfolio hosting

---

# 🚀 Conclusion

## 📌 Strategic Takeaways

- 🔥 Focus on:
  - Combo1
  - Home Appliances
  - Grocery & Staples (selectively)

- 🏙️ Target cities:
  - Madurai
  - Chennai
  - Bengaluru

- ❌ Avoid:
  - 25%, 33%, 50% OFF promotions

- 💳 Prioritize:
  - 500 Cashback
  - BOGOF

- 🪔 Diwali > Sankranti (higher ROI season)

---

# 👤 Author

**Anwesha Mahapatra**

- 💼 Data Analyst  
- 📊 MySQL | Power BI | Business Intelligence  

- 🔗 LinkedIn: https://www.linkedin.com/in/anweshamahapatra-dataanalyst/ 
- 💻 GitHub:https://github.com/AnweshaMahapatra  
- 📧 Email: anweshamahapatra8888@gmail.com  
