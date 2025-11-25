# Trader Behavior vs Bitcoin Market Sentiment  
### Data Science Assignment – Trader Insights Analysis  

---

## Project Overview

This project analyzes how trader performance on the Hyperliquid exchange varies under different Bitcoin market sentiment states (Fear, Greed, Neutral).  

We combine:
1. **Hyperliquid Historical Trader Data**  
2. **Bitcoin Fear & Greed Index Data**

The aim is to uncover whether trader profitability and trading volume change during Fear vs Greed conditions, and extract insights useful for trading strategy design.

---

## Repository Structure

ds_shruti_pachpor/

notebook_1.ipynb – Main notebook (cleaning, EDA, merging, analysis, charts)

notebook_2.ipynb – Optional notebook (extra exploration)

csv_files/

daily_trader_sentiment_merged.csv – Processed + merged dataset

outputs/

avg_pnl_by_sentiment.png

total_pnl_by_sentiment.png

avg_volume_by_sentiment.png

ds_report.pdf – Final PDF report (insights + visualizations)

README.md – Project documentation


---

## Methodology

### **1. Data Cleaning**
- Converted UNIX timestamps to proper datetime format  
- Extracted a `date` column to match trades with sentiment  
- Handled missing/null values  
- Standardized sentiment into:
  - **Greed** (Greed + Extreme Greed)
  - **Fear**
  - **Neutral**

### **2. Feature Engineering**
Calculated the following metrics per day:
- `pnl_sum`  → total daily PnL  
- `pnl_mean` → average PnL per trade/day  
- `volume_sum` → total traded volume (USD)

### **3. Data Merging**
Merged the above metrics with the Fear/Greed index on the `date` column.

### **4. Analysis**
Grouped and compared trader performance across sentiment states, focusing on:
- PnL  
- Trading volume  
- Behavioral differences  

### **5. Visualization**
Generated 3 charts:
- **Average PnL by sentiment**
- **Total PnL by sentiment**
- **Average trading volume by sentiment**

These are saved in the `outputs/` folder.

---

## 📊 Key Insights

- **Fear days showed the highest trader profitability and the highest trading volume**, indicating strong volatility and opportunity.
- **Greed days had the lowest PnL**, suggesting a more stable market with fewer profitable moves.
- **Neutral days** fall between Fear and Greed in both performance and volume.
- Market sentiment strongly correlates with trader behavior and can be used to enhance trading strategies.

---

## ▶️ How to Run the Notebook

1. Open **notebook_1.ipynb** in Google Colab.  
2. Upload the raw datasets (`historical_data.csv` and `fear_greed_index.csv`) into Colab.  
3. Run all cells sequentially to:
   - Clean & prepare data  
   - Generate daily metrics  
   - Merge datasets  
   - Produce charts  
4. Download the processed file (`daily_trader_sentiment_merged.csv`) and all PNG charts.  
5. Read **ds_report.pdf** for the full analysis summary.

---



