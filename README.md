# Agentic AI — Multi-Agent E-Commerce Analytics

A multi-agent machine learning system for e-commerce analytics, built with 5 specialized agents.

##  Project Structure

| Agent | Type | Model(s) | Folder |
|-------|------|----------|--------|
| **Agent 1** – Customer Segmentation | USL | K-Means + DBSCAN | `segmentation_model/` |
| **Agent 2** – Demand Forecasting | Time Series | ARIMA / SARIMA / Prophet | `time_seris_model/` |
| **Agent 3** – Churn Prediction | SML | Random Forest / XGBoost | `churn_model/` |
| **Agent 4** – Price-Gap Analysis | USL | Custom Pricing Model | `price_gap_agent/` |
| **Agent 5** – Global EDA | EDA | Exploratory Data Analysis | `golbal eda/` |

##  Agent Details

### Agent 1 · Customer Segmentation (USL)
- **Input**: Customer ID, InvoiceDate, Quantity, Price
- **Features**: Recency, Frequency, Monetary (RFM)
- **Models**: K-Means (primary) + DBSCAN (handles noise)
- **Output**: Segment labels — Champion / Loyal / At-Risk / Lost

### Agent 2 · Demand Forecasting (Time Series)
- **Input**: InvoiceDate, Quantity, Price → weekly Revenue
- **Models**: ARIMA · SARIMA · Prophet
- **Metrics**: RMSE, MAE
- **Output**: 4–8 week revenue forecast with confidence intervals

### Agent 3 · Churn Prediction (SML)
- **Input**: RFM features + days between purchases + country
- **Label**: No purchase in 90 days = churned (1), else active (0)
- **Models**: Random Forest · XGBoost
- **Output**: Churn probability per customer

### Agent 4 · Price-Gap Analysis
- **Model**: Custom pricing model
- **Output**: Pricing insights and recommendations

### Agent 5 · Global EDA
- **Purpose**: Exploratory Data Analysis across the full dataset
- **Output**: Visual summaries and statistical insights

## 🛠️ Tech Stack
- Python, Jupyter Notebooks
- scikit-learn, XGBoost, statsmodels, Prophet, mlxtend
- pandas, numpy, matplotlib, seaborn
