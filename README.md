# Loan & Financial Risk Analysis (Nova Bank Credit Risk Challenge)

An Excel-based credit risk analysis that explores **which borrowers tend to default** and **which financial indicators are linked to default**, finishing with a 3-page interactive dashboard and a business insights report.

> **Note:** This is a descriptive analysis. It shows patterns in historical data. It does not show causes, and it is not a predictive model.

---

## Business Problem

Nova Bank wants to lend fairly and accessibly while protecting itself from unnecessary risk. The goal of this project is to use the data to:

- See which groups of borrowers are more or less likely to default
- Identify the factors that matter most when explaining loan outcomes
- Explore how loan size, income, interest rates and repayment terms relate to risk
- Spot early signs of financial trouble
- Suggest ways the bank can adjust lending policies

## Dataset

| Item | Detail |
|---|---|
| Records | 32,581 loans |
| Columns | 29 |
| Countries | USA, UK, Canada |
| Overall default rate | 21.8% (7,108 defaulted, 25,473 non-defaulted) |
| Average loan | about $9,589 (total loan amount $312,431,300) |
| Average borrower income | $66,075 |
| Average interest rate | 11.0% |
| Average DTI | 35% |

## Tools & Techniques

- **Microsoft Excel**: data cleaning, formulas, grouping, pivot tables, charts
- **Dashboard design**: KPI cards, slicers (loan grade, loan term, country), interactive charts
- **Techniques**: data cleaning and standardisation, feature grouping (age, employment length, credit history, DTI and income bands), exploratory data analysis, business storytelling

## Project Workflow

1. **Business understanding**: define the goal and questions
2. **Data understanding & EDA**: data dictionary, structure, issues
3. **Data cleaning & preparation**
4. **Exploratory analysis**: KPIs and 8 business questions
5. **Dashboard development**
6. **Business recommendations**

### Data Cleaning Summary

| Column | Issue | Action |
|---|---|---|
| Person age | Invalid values (e.g. 123, 144) | Replaced with the median |
| Person employment length | Invalid values (123 years) and 895 missing values | Replaced with the median (4,105 zero values kept as real values) |
| Loan intent | Inconsistent formatting, missing spaces | Standardised, consolidated "Debt Consolidation" |
| Loan interest rate | 3,116 missing values | Filled with the median rate of the same loan grade |
| Loan-to-income ratio | Inconsistent with loan amount and income | Recalculated as loan amount / income |
| Employment type | Words separated by hyphens | Replaced hyphens, standardised text |
| City, latitude, longitude | Not needed for analysis | Removed |

## Business Questions

1. Which types of borrowers are more likely to default?
2. Do certain loan purposes carry more risk?
3. How do loan-to-income and debt-to-income ratios relate to repayment?
4. How do past defaults or longer credit histories affect loan outcomes?
5. Are there clear differences between borrowers in the USA, UK and Canada?
6. Which loan grades or terms seem safer, and which are riskier?
7. Does employment type or home ownership make a difference?
8. Can groups of borrowers be identified that look "safe" versus "risky"?

## Key Findings

| Area | Result |
|---|---|
| **Loan grade** | Default rate rises from 9.96% (grade A) to 98.44% (grade G); grades D to G range from 59.05% to 98.44% |
| **Previous default on file** | 37.81% default rate vs 18.39% for borrowers without one |
| **Debt burden** | Defaulted borrowers: average DTI 42% vs 32%; average LTI 25% vs 15% |
| **Home ownership** | Owners 7.47%, mortgage 12.57%, renters 31.57% |
| **Employment length** | 0 years 27.94% falling to 16.23% for 11+ years |
| **Loan purpose** | Debt consolidation 28.59% (highest), venture 14.81% (lowest); medical loans produce the most defaults (about 1,621) |
| **Little difference** | Marital status, education, country, employment type and loan term |

See the full report for interpretation, limitations and recommendations.

## Dashboard

The Excel dashboard has three pages, each with KPI cards and slicers for loan grade, loan term and country:

- **Executive Overview**: defaulted vs non-defaulted loans, loan purpose default rate, average loan by DTI and income category
- **Borrower Risk Analysis**: default rate by age, education, employment length and marital status
- **Loan & Financial Risk Analysis**: default rate by credit history, DTI category, loan grade and previous default on file


## Business Recommendations (summary)

1. Apply tiered credit review by loan grade (stricter for D to G)
2. Set affordability checks using DTI and LTI
3. Flag previous default for mandatory review
4. Strengthen assessment for debt consolidation, medical and home improvement loans
5. Use home ownership and employment length as supporting context, after a fairness check
6. Avoid relying on age, marital status, education, country or loan term

Each recommendation has a supporting insight and a KPI in the full report.
