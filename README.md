# Sales Performance Analysis

An end-to-end data analysis of 512 retail orders across six Nigerian cities (January to December 2025), done in Python. The project covers data inspection, cleaning, analysis and visualisation, and ends with business recommendations.

> **Note:** The dataset is simulated for practice. It was deliberately generated with common data problems, so the findings illustrate the method and are not real market evidence.

## Business Questions
1. Which cities generate the most and least revenue?
2. Which categories and products drive revenue?
3. How does revenue change month by month?
4. How healthy is order fulfilment?

## Project Contents
```
├── sales_analysis.ipynb          # Full analysis notebook
├── sales_data_raw.csv            # Raw dataset (512 rows, 12 columns)
├── generate_practice_data.py     # Script that generated the dataset

```

## Data Cleaning
| Problem | Action |
|---|---|
| 12 duplicate rows | Removed |
| Inconsistent city labels (UYO, uyo, " Uyo ") | Trimmed and standardised |
| Dates stored as text in two formats | Parsed each format into real dates |
| Impossible ages and ratings | Set to missing |
| Unit price typo (₦45,000,000) | Corrected to ₦65,000 |
| Quantity typo (500) | Row removed |
| Missing payment method | Labelled "Unknown" |
| Missing age | Filled with the median |
| Missing rating | Left missing, not invented |

Final dataset: 499 rows.

## Key Findings
Revenue figures use **delivered orders only** (397 orders, ₦112.8M).

- **Top city:** Port Harcourt (₦29.5M); weakest: Enugu (₦5.9M).
- **Top category:** Electronics, about 78% of revenue. Laptops alone contribute about 50%.
- **Peak months:** February (₦16.6M) and June (₦15.1M); lowest: September (₦5.2M).
- About ₦27.6M of order value is tied up in pending or cancelled orders.
- Cleaning mattered: two typing errors had inflated revenue to about ₦320.9M and pointed to the wrong top city and category.

## Recommendations
- Protect electronics stock, since two products drive about 75% of revenue.
- Reduce pending and cancelled orders.
- Investigate why Enugu is underperforming.
- Plan promotions for the weaker months.

## Tools Used
Python, pandas, NumPy, matplotlib, Jupyter Notebook

## How to Run
1. Clone the repository.
2. Install the libraries: `pip install pandas numpy matplotlib jupyter`
3. Open `sales_analysis.ipynb` and run all cells.

## Author
Isaac | [GitHub](https://github.com/Okoro-Isaac-Chisom)
