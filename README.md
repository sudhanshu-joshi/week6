# 📊 Sales Trends & Customer Behavior in E-Commerce Dataset

An end-to-end Data Analytics project to explore online sales data, uncover customer insights, and build an interactive dashboard using Python and Power BI.

---

## ✅ Project Objectives

- Analyze sales performance and customer behavior
- Identify top-selling products and high-revenue countries
- Visualize KPIs and trends using Power BI or Plotly Dash
- Deliver business insights and recommendations

---

## 📁 Dataset

**Source:** [Kaggle: E-Commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)

**Features:**
- `InvoiceNo`, `StockCode`, `Description`, `Quantity`
- `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🧹 Data Cleaning (Python)

- Removed null `CustomerID` values
- Converted `InvoiceDate` to datetime format
- Created `TotalAmount = Quantity * UnitPrice`
- Removed cancelled orders (InvoiceNo starting with "C")

---

## 📊 Exploratory Data Analysis (EDA)

- 📈 Monthly Sales Trends  
- 🏆 Top 10 Products by Revenue  
- 🌍 Top Countries by Sales  
- 🔢 KPIs: Total Revenue, Orders, Customers  

```python
# Example: Total Sales
total_sales = df['TotalAmount'].sum()

# Example: Monthly Trend
sales_trend = df.groupby(df['InvoiceDate'].dt.to_period('M'))['TotalAmount'].sum()

## Power BI Dashboard
Upload the cleaned data and create visuals for:
  Sales over time
  Product-wise and country-wise performance
  KPI cards

## Key Insights
  Sales peak during the holiday season (Nov–Dec)
  UK contributes to the majority of sales
  A few products generate most of the revenue
