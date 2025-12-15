# Trading Behavior & Market Sentiment Analysis

## 📊 Project Overview

This data science project investigates the relationship between cryptocurrency trader behavior on the Hyperliquid exchange and overall market sentiment measured by the Bitcoin Fear & Greed Index. The analysis explores whether trading profitability, risk, and behavior align with prevailing market sentiment patterns.

## 🎯 Objectives

- Analyze how trading behavior (profitability, risk, volume) correlates with market sentiment (fear vs greed)
- Identify hidden trends and patterns in trader performance across different sentiment regimes
- Develop trader profiles using clustering techniques to categorize different trading strategies
- Provide insights for developing smarter, data-driven trading strategies

## 📁 Dataset Description

### 1. Bitcoin Market Sentiment Data
- **File**: `fear_greed_index.csv`
- **Columns**: `timestamp`, `value`, `classification`, `date`
- **Description**: Daily Bitcoin Fear & Greed Index values ranging from 0-100, with classifications (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

### 2. Historical Trader Data
- **File**: `historical_data.csv`
- **Key Columns**: `Account`, `Execution Price`, `Size USD`, `Direction`, `Timestamp IST`, `Closed PnL`, `Fee`, etc.
- **Description**: Individual trade execution data from Hyperliquid exchange including PnL, trade size, and timing

## Running the Analysis
Ensure both CSV files are in the project directory

Open and run notebook_1.ipynb sequentially

Review generated visualizations and cluster results.

## 🛠️ Technical Implementation

### Data Processing Pipeline
1. **Data Loading & Cleaning**
   - Handled datetime conversions and missing values
   - Standardized column names and formats
   - Created daily aggregates from trade-level data

2. **Feature Engineering**
   - Daily trader metrics: `trades_count`, `total_pnl`, `avg_pnl`, `win_rate`, `std_pnl`
   - Rolling metrics: `rolling_pnl_7d` for trend analysis
   - Merged sentiment scores with daily trade aggregates

3. **Exploratory Data Analysis**
   - Correlation analysis between sentiment and trading metrics
   - Time series visualization of PnL and sentiment
   - Distribution analysis of trader performance

4. **Machine Learning & Clustering**
   - K-Means clustering with PCA for dimensionality reduction
   - StandardScaler for feature normalization
   - Cluster analysis and profile identification

### Key Libraries Used
- `pandas`, `numpy` - Data manipulation
- `matplotlib` - Data visualization
- `scikit-learn` - Clustering and preprocessing
- `statsmodels` - Statistical analysis

## 📈 Key Findings

### 1. Sentiment-Profitability Relationship
- **No strong direct correlation** between daily Fear & Greed values and trader profitability
- Market sentiment alone is not a reliable predictor of trading success
- Profitability appears driven more by individual strategy than market mood

### 2. Trader Behavior Segmentation
Three distinct trader profiles identified through clustering:

#### 🟢 Cluster 0: The Break-Even Majority
- Moderate activity across all metrics
- Low to moderate PnL with ~50% win rate
- Represents the average retail trade

#### 🔵 Cluster 1: The High-Rolling Whales
- Extremely high total PnL and high volatility
- Small group with outsized impact
- High-risk, high-reward strategies

#### 🟣 Cluster 2: The Consistent Winners
- High win rate with positive average PnL
- Moderate risk with consistent performance
- Most sustainable trading profile

### 3. Market Context
- Analysis period (Q4 2024) dominated by "Greed" to "Extreme Greed" sentiment
- Limited data from fear-dominated markets for comparative analysis

##Assignment link - https://colab.research.google.com/drive/1xrrNUtZLCnRqx1U2SxAu_J_9Oc6gHlsv?usp=sharing

## Author
Divya Prakash
raydivyaprakash@gmail.com
