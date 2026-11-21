# HR Attrition Analysis: Who Leaves, and Why?

A Power BI dashboard and follow-up analysis of employee attrition, with a closer look at one termination reason: **"unhappy"**.

## Question

Who leaves the company, and why? Within that, what do employees who left because they were *unhappy* have in common?

## Data

- **Source:** _add the dataset name, link, and license here_
- **Size:** 311 employees (207 active, 104 terminated)
- **Period:** hires and terminations from 2006 to 2018
- **Key fields:** department, position, manager, salary, recruitment source, termination reason, performance score, tenure

## Dashboard

Built in Power BI. It covers:

- Hires vs. terminations by year
- Terminations by recruitment source
- Top termination reasons
- Attrition rate by department
- Median salary by department
- Terminations by manager
- Slicers for department and gender

## Key Findings

### Overview

- Production has the highest attrition: **39.7%** (83 of 209 employees who ever worked there).
- "Unhappy" is the third most common termination reason: **14 of 104 exits (13.5%)**.

### The 14 "unhappy" exits

- All 14 worked in **Production**.
- **Technician II** had roughly double the rate of Technician I: **10.5%** (6 of 57) vs. **5.1%** (7 of 137).
- **11 of 14** had performance ratings of "Fully Meets" or "Exceeds".
- Average tenure was **3.3 years**, compared with **5.7 years** for currently active Production employees.
- Pay was similar to peers in the same role, so salary alone does not seem to explain it.

### Attrition rate by recruitment source

Raw counts and rates tell different stories. Google Search produced the most leavers, but it also had the highest attrition rate.

| Source | Leavers | Hired | Attrition rate |
|---|---|---|---|
| Google Search | 30 | 49 | 61.2% |
| Diversity Job Fair | 16 | 29 | 55.2% |
| CareerBuilder | 11 | 23 | 47.8% |
| Indeed | 21 | 87 | 24.1% |
| LinkedIn | 18 | 76 | 23.7% |
| Employee Referral | 5 | 31 | 16.1% |

## Analysis Decisions

- **Median instead of mean for salary.** A few very high salaries (CEO at 250K, CIO at about 220K) pull the mean up to about 69K. The median (about 62.8K) better reflects a typical employee.
- **Corrected a misleading chart.** An early version of the termination-reason donut showed "unhappy" as 26%. It only included the top 4 reasons (54 exits). Across all 104 exits, the figure is 13.5%.
- **Attrition is cumulative.** Rates are exits divided by everyone who ever worked in the group (2006–2018). They are not annual turnover rates.

## Limitations

- The "unhappy" group is only 14 people, so these are exploratory signals, not proof of causation.
- The data is historical (2006–2018).
- Survey satisfaction scores did not reliably flag who would leave: about half of the 14 rated their satisfaction 4 or 5.

## Recommendations

- Investigate satisfaction among Production Technicians, especially Technician II.
- Run targeted exit interviews around the 3–4 year mark.
- Track retention by recruitment source to evaluate hiring effectiveness.

## Repository Structure

```
├── README.md
├── data/
├── dashboard/
│   ├── HR_analytics.pbix
│   └── dashboard.png
└── analysis/
```

## Tools

Power BI, Excel
