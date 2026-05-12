# 🛒 SuperStore Sales Analysis
 
A full end-to-end data analysis project on the classic **SuperStore** retail dataset, covering data cleaning with Python, exploratory analysis in a Jupyter notebook, and an interactive business intelligence dashboard built in Power BI.
 
---
 
## 📁 Project Structure
 
```
SuperStore/
├── SuperStore.ipynb              # Data cleaning & preprocessing notebook
├── SuperStores_cleaned.xlsx      # Cleaned dataset (output of the notebook)
└── SuperStores_Dashboard.pbix    # Power BI interactive dashboard
```
 
---
 
## 📊 Dataset Overview
 
The dataset contains US retail transactions from **2017 to 2020** across multiple product categories and customer segments.
 
| Column | Description |
|---|---|
| `Order ID` | Unique identifier for each order |
| `Order Date` / `Ship Date` | Order placement and shipping dates |
| `Ship Mode` | Shipping method (Standard, Second Class, First Class) |
| `Customer ID / Name` | Customer details |
| `Segment` | Customer segment: Consumer, Corporate, Home Office |
| `Region / State / City` | Geographic data |
| `Category / Sub-Category` | Product classification |
| `Product Name` | Individual product |
| `Sales` | Revenue per line item |
| `Quantity` | Units sold |
| `Discount` | Discount applied |
| `Profit` | Profit per line item |
 
---
 
## 🧹 Data Cleaning (`SuperStore.ipynb`)
 
The Jupyter notebook performs the following preprocessing steps:
 
1. **Load the raw data** from the original Excel file
2. **Convert date columns** — `Order Date` and `Ship Date` parsed as proper `datetime` objects
3. **Handle missing values** — `Postal Code` nulls filled with `0` and cast to integer
4. **Add time-series helper columns**:
   - `Order Year` — extracted from `Order Date`
   - `Order Month` — monthly period for time-series aggregation
5. **Export the cleaned dataset** as `SuperStores_cleaned.xlsx`
### Libraries Used
 
```python
pandas
matplotlib
seaborn
openpyxl
```
 
---
 
## 📈 Power BI Dashboard (`SuperStores_Dashboard.pbix`)
 
The dashboard provides interactive, filterable visualizations for business insights including:
 
- 📦 **Sales & Profit by Category and Sub-Category**
- 🗺️ **Regional Performance** across US states
- 👥 **Customer Segment Analysis** (Consumer / Corporate / Home Office)
- 📅 **Sales Trends Over Time** (2017–2020)
- 🚚 **Shipping Mode Distribution**
> Open the `.pbix` file in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to interact with the dashboard.
 
---
 
## 🚀 Getting Started
 
### Prerequisites
 
- Python 3.8+
- Jupyter Notebook or JupyterLab
- Power BI Desktop (for the dashboard)
### Installation
 
```bash
# Clone the repository
git clone https://github.com/your-username/superstore-analysis.git
cd superstore-analysis
 
# Install required Python packages
pip install pandas matplotlib seaborn openpyxl jupyter
```
 
### Running the Notebook
 
```bash
jupyter notebook SuperStore.ipynb
```
 
The notebook will read the raw data, apply cleaning steps, and save the cleaned output to `SuperStores_cleaned.xlsx`.
 
---
 
## 🔑 Key Insights
 
- The dataset spans **4 years** (2017–2020) of US retail transactions
- Three product **categories**: Furniture, Office Supplies, Technology
- Three customer **segments**: Consumer, Corporate, Home Office
- Orders are distributed across **4 regions**: East, West, South, Central
- Some high-discount orders (40–80%) result in **negative profit**, highlighting a pricing challenge
---
 
## 📄 License
 
This project uses the publicly available [Superstore dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final), commonly used for data analysis and BI practice.
 
---
 
## 🙋 Author
 
Made with ❤️ using Python & Power BI.  
Feel free to open an issue or submit a pull request!
