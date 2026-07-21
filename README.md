# Jar Growth Intern Assignment

My submission for the Jar Growth Intern take-home assignment. The brief has
three questions - a Python-based sales analysis, an app exploration writeup,
and a product/business opportunity discussion - and this repo has one
deliverable for each.

**Repository:** https://github.com/Ganesh-anandam/jar-assesment - the code,
notebook and full commit history are here for review alongside the PDF.

## What's in here

| File | Covers | Notes |
|---|---|---|
| `Jar_Growth_Intern_Assignment_Submission.pdf` | Questions 1, 2 & 3 | **Final submission file** - single report: cover page, Q1 analysis (code + tables + charts + findings), then Q2 and Q3 |
| `Sales_Analysis.ipynb` | Question 1 working | Source notebook behind the Q1 section - already executed, open it if you'd rather read/re-run the live version |
| `Written_Answers.md` | Question 2 & 3 working | Source markdown behind the Q2/Q3 sections |
| `List_of_Orders.xlsx` | raw data | one row per order (date, customer, state, city) |
| `Order_Details.xlsx` | raw data | one row per order line item (category, sub-category, amount, profit, quantity) |
| `Sales_target.xlsx` | raw data | monthly sales target per category |

The three Excel files are exactly as provided in the assignment - untouched,
so the data-cleaning steps can be followed from scratch.

The PDF is the actual submission, formatted as a single readable report
rather than a raw notebook export - same underlying analysis and numbers as
the notebook/markdown, just laid out for a reviewer rather than for
re-running.

## Question 1 - how it's organized

`Sales_Analysis.ipynb` walks through, in order:

1. **Loading the raw files** and a quick look at shapes/dtypes.
2. **Data cleaning** - `Order Date` in `List_of_Orders.xlsx` is a mix of real
   dates and `dd-mm-yyyy` text, and the month column in `Sales_target.xlsx`
   turned out to have its year and day fields swapped by Excel's autocorrect
   when the sheet was originally typed up. Both are explained inline with
   the actual values that gave it away, and fixed before any aggregation.
3. **Part 1 - Sales & Profitability by Category**: merges the orders and
   order-details sheets on `Order ID`, aggregates sales/profit/margin per
   category, drills into sub-categories to explain *why* the weaker
   category underperforms, and calls out the top and bottom performers with
   the reasoning behind the gap.
4. **Part 2 - Target Achievement (Furniture)**: month-over-month % change in
   the Furniture target, a chart of the trend, and a look at which months
   see unusually large jumps plus what that implies for how targets are set.
5. **Part 3 - Regional Performance**: top 5 states by order count, their
   sales/profit/margin, plus a city-level and all-state drill-down to flag
   specific regional disparities (not just the top 5) worth prioritizing.

Each part ends with a short markdown write-up of the findings, grounded in
the numbers computed just above it - the goal was to make every claim
traceable back to a specific cell in the notebook rather than a general
statement.

## Running it yourself

The notebook only needs pandas, openpyxl (to read `.xlsx`) and matplotlib:

```bash
pip install pandas openpyxl matplotlib jupyter
jupyter notebook Sales_Analysis.ipynb
```

Or to re-run it end-to-end from the command line and overwrite the saved
outputs:

```bash
jupyter nbconvert --to notebook --execute --inplace Sales_Analysis.ipynb
```

Both `.xlsx` inputs need to stay in the same folder as the notebook since
the file paths in the first cell are relative.

## Question 2 & 3

These are answered in `Written_Answers.md`:

- **Question 2 (App Exploration)** - five things about the Jar app that work
  well and five areas for improvement, each with the reasoning behind it.
- **Question 3 (Product Exploration)** - new business opportunities Jar
  could build on top of its existing savings/trust/automation strengths,
  ordered roughly from "closest to the current product" to "longer-term
  bet."
