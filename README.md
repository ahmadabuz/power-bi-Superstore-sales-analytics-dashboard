# Sales Analytics Dashboard

Interactive sales performance dashboard built with Power BI to analyze retail data and uncover actionable business insights.

![Dashboard Overview](screenshots/Screenshot 2026-02-13 004347.png)

## Project Overview

This is my first Power BI project, completed as part of my data science learning journey. The dashboard demonstrates fundamental business intelligence skills using Power BI and DAX to transform raw sales data into visual insights.

**Key Metrics:**
- Total Sales: $2.26M
- Year-over-Year Growth: 47%
- Products Analyzed: 1,849
- Total Customers: 793
- Cities Covered: 529
- States: 49

## Dataset

- **Source:** Kaggle Superstore Sales Dataset
- **Location:** dataset/ folder in this repository
- **Records:** 9,000+ transactions
- **Format:** CSV
- **Time Period:** 2015-2018
- **Categories:** Office Supplies, Furniture, Technology


## Dashboard Features

### Interactive KPIs
- Dynamic year-over-year growth indicators with conditional formatting
- Automatic color coding (green for positive growth, red for negative)
- Real-time metrics across different business segments and regions

### Visualizations
- Sales trends from 2015-2018
- Regional performance comparison (West, East, Central, South)
- Top-selling products ranking
- Category breakdown (Office Supplies, Furniture, Technology)
- Segment analysis (Consumer, Corporate, Home Office)

### User Interactivity
- Multi-page dashboard with drill-through navigation
- Interactive filters for City, State, Region, and Postal Code
- Product name and Order ID search


## Technical Implementation

### DAX Measures

**Dynamic KPI with Conditional Formatting:**
```dax
Sales KPI = 
VAR g = [Sales Growth %]
VAR arrow =
    IF(g > 0, "▲ ", IF(g < 0, "▼ ", "■ "))
RETURN
arrow & FORMAT(g, "0%")
```

**Additional Measures:**
- Year-over-Year Growth Percentage
- Total Sales (Current Year)
- Total Sales (Previous Year)
- Customer Count
- Product Count

### Skills Applied
- Data modeling and relationship management
- DAX calculations for time intelligence
- Conditional formatting
- Drill-through navigation
- Data visualization principles


## Screenshots

### Main Dashboard - Overview Page
![Overview Page](screenshots/overview.png)

### Order Monitoring Page
![Orders Page](screenshots/orders.png)


## Key Insights

### Segment Performance
- Consumer segment: $1.1M (50% of revenue)
- Corporate segment: $0.7M
- Home Office segment: $0.4M

### Regional Analysis
- West region: $0.71M
- East region: $0.67M
- Central region: $0.49M
- South region: $0.39M

### Product Performance
- Top product: Canon imageCLASS 2200 (62K sales)
- Office Supplies category leads in volume
- Technology products show higher average order values

### Growth Trends
- 47% year-over-year growth rate
- Sales increased from 1,953 units (2015) to 3,258 units (2018)

## How to Use

1. Download the .pbix file from the dashboard/ folder
2. Install Power BI Desktop (free from Microsoft)
3. Open the file and explore the interactive features

The dataset is also available in the dataset/ folder for further analysis.

## Repository Structure
```
powerbi-sales-analytics-dashboard/
├── README.md                          # Project documentation
├── dashboard/
│   └── Sales_Dashboard.pbix           # Power BI dashboard file
├── dataset/
│   └── superstore_sales.csv           # Source dataset
└── screenshots/
    ├── overview.png                   # Main dashboard
    └── orders.png                     # Orders page
```

## Tools Used

- Power BI Desktop
- DAX (Data Analysis Expressions)
- Power Query

## Future Improvements

- Add predictive analytics for sales forecasting
- Include profit margin analysis
- Create mobile-optimized layout
- Connect to live data sources

## Contact

- LinkedIn: https://www.linkedin.com/in/ahmad-abu-zayyad-897b922a4/?originalSubdomain=jo
- Email: ahmadabuzayad9@gmail.com


**Note:** This is an academic project using publicly available data from Kaggle
