# Financial-Insights-EDA

### Introduction
The "Personal Finance Insights" project aims to provide a comprehensive analysis of my financial behavior and spending patterns over a specified period (March 2023-March 2024). By analyzing my bank statement data, this project offers insights into fund utilization, expense management, and income trends, contributing to personal financial management and decision-making.

![total_transaction_amount_over_time](https://github.com/skpordzih/Financial-Insights-EDA/assets/163223093/c86f102b-b275-464d-b6e4-bcbbb1d09a20)


### Tools
Jupyter Notebook
- Python

### Data Collection and Preparation
Bank statement data spanning from March 2023 to March 2024 was collected and prepared for analysis. The dataset includes columns such as Date, Description, Transaction Type, Amount, Category, and Balance. Initial data cleaning steps involved converting the Date column to datetime format, filling missing values, categorizing transactions, and reordering columns for better organization.

### Exploratory Data Analysis (EDA):
1. **Transaction Trends Over Time:** Visualized using interactive line plots, transaction trends over time provide insights into the fluctuation of financial activities.
2. **Spending Categories Distribution:** Bar plots illustrate the distribution of spending across various categories, offering insights into where funds are predominantly allocated.
3. **Transaction Distribution:** Stacked bar plots showcase the distribution of transactions by type and category, providing a detailed breakdown of financial activities.
4. **Category-wise Spending Analysis:** Summarized total spending by category, highlighting significant expenditure areas such as rent, transportation, subscriptions, and miscellaneous expenses.
5. **Balance Over Time:** Analyzed balance fluctuations over time using line plots, offering insights into financial stability and trends.
6. **Transaction Types Distribution:** Examined the distribution of transaction types (debit vs. credit) through count plots, providing an overview of transaction modes.
7. **Correlation Analysis:** Investigated correlations between numerical variables like Amount and Balance, revealing insights into financial dynamics.

## Dashboard Creation:
Interactive dashboards were created to visualize and summarize key findings:
- **Dashboard 1:** Presents daily and monthly total transactions, category-wise monthly total transactions, summary statistics, and missing values summary.
- **Dashboard 2:** Provides balance trends over time and histograms of transaction amounts, facilitating deeper exploration of financial dynamics.
- **Dashboard 3:** Offers insights into monthly income, expenses, and balance trends, along with a summary table presenting key financial metrics.

### Data Analysis

```python

categories_count = df['Category'].value_counts()
print(categories_count)

plt.figure(figsize=(12, 6))
sns.countplot(data=df, x='Category', order=df['Category'].value_counts().index)
plt.title('Transaction Categories Distribution')
plt.xticks(rotation=90)
plt.show()

```

### Findings

The analysis results are summarized as follows:
- Debit transactions dominate the dataset, comprising 220 out of 326 transactions, indicating higher expenditure compared to credits.
- Rent accounts for the highest expenditure, followed by Interac Sent and Account Transfers.
- Notable expenses include Grocery, Bank Transfer, and Subscriptions.
- The balance fluctuates over time, indicating varied spending patterns and income inflows.
- Monthly expenses exceed income in some months, leading to a decrease in the balance.
- The balance trend shows fluctuations, indicating changes in financial behavior and spending habits over time.

### Recommendations
Based on the analysis, I recommed the following actions:
- Prioritize expense reduction in categories such as Shopping & Miscellaneous to maintain a healthier financial balance.
- Consider budgeting techniques and expense tracking tools to monitor spending habits effectively.
- Consider implementing a spending cap or allocating a specific budget for non-essential expenses to maintain financial discipline.
