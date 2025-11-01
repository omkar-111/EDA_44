
## 📋 Project Overview
This project presents an **Exploratory Data Analysis (EDA)** of the **Hotel Bookings Dataset**, which contains details about hotel reservations, cancellations, guest demographics, and booking trends.  
The dataset consists of **119,390 records** and **32 features**, covering key aspects such as lead time, stay duration, booking channels, and revenue metrics (ADR – *Average Daily Rate*).  

The EDA aims to extract insights that help understand **customer behavior, revenue drivers**, and **operational patterns** in hotel management.

---

## 🎯 Core Objectives
1. Understand customer attributes and booking behaviors impacting revenue.  
2. Identify trends in lead time, stay duration, and booking channels.  
3. Detect anomalies or inconsistencies in room allocation.  
4. Explore relationships between booking patterns and satisfaction indicators.  
5. Evaluate operational or customer variables affecting ADR and room upgrades.

---

## ⚙️ Technologies Used
- **Python** 🐍  
- **Libraries:** `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Scipy`  
- **Jupyter Notebook / Google Colab** for data analysis and visualization  

---

## 🧹 Data Cleaning and Preprocessing
Key preprocessing steps included:  
- Dropped columns with excessive missing values (`company` – 94%).  
- Filled missing values:
  - `children` → 0  
  - `country` → mode value  
  - `agent` → 0  
- Removed **32,020 duplicate records**.  
- Converted date columns into a unified `arrival_date` column.  
- Engineered new features:  
  - `total_stays` = sum of weekday and weekend nights  
  - `total_guests` = adults + children + babies  

---

## 📊 Exploratory Data Analysis (EDA)
The analysis included:
- **Univariate Analysis:** Distribution of features like ADR, lead time, and customer type.  
- **Bivariate Analysis:** Relationships between hotel type, market segment, and ADR using boxplots and scatterplots.  
- **Multivariate Analysis:** Combined multiple features (e.g., ADR by hotel and customer type).  
- **Time-Series Analysis:** Monthly and seasonal booking trends.

---

## 🔗 Correlation Analysis
- Computed a **Pearson correlation matrix** to evaluate relationships among numerical variables.  
- Visualized via **heatmap**, highlighting strong correlations:
  - `adr` positively correlated with `lead_time`, `total_guests`, and `special_requests`.  
- Helped detect **multicollinearity** and identify **influential revenue drivers**.

---

## 🧪 Hypothesis Testing
Three key hypotheses were tested:  

| Hypothesis | Test Used | Result |
|-------------|------------|--------|
| Difference in ADR between Online TA and Direct channels | Welch’s t-test | Significant difference (p < 0.05) |
| Relationship between room upgrades and lead time | Welch’s t-test | Lead time impacts upgrades |
| Variation in stay duration across customer types | One-way ANOVA | Significant variation |

✅ **All null hypotheses rejected**, confirming statistically significant relationships.

---

## 💡 Key Business Questions Answered
- What factors most influence **ADR (Average Daily Rate)?**  
- How do **lead times** affect booking modifications and cancellations?  
- Are there **country-based patterns** in pricing or booking behavior?  
- Are **room upgrades or reassignments** consistent across customer types?  
- Do certain **market segments** yield higher **revenue and consistency?**  
- How do **special requests** correlate with longer stays or higher ADR?  

---

## 🧭 Insights & Conclusion
- Guests booking earlier tend to have **higher ADR** and **more special requests**.  
- **Online TA channels** show higher ADR variation than direct bookings.  
- **Corporate and transient guests** differ in stay duration and revenue contribution.  
- **Lead time and special requests** play a crucial role in predicting cancellations and upgrades.  

The EDA provides actionable insights for improving **pricing strategies, marketing**, and **guest satisfaction**, helping hotels **maximize revenue** and **optimize operations**.

---

