# Business Intelligence with Tableau
Interactive Business Intelligence dashboard developed with Tableau Desktop as part of the **Business Intelligence with Tableau** module of the Master's in Data Science, Big Data & Business Analytics at Universidad Complutense de Madrid.

[![View on Tableau Public](https://img.shields.io/badge/Tableau%20Public-View%20Dashboard-E97627?style=flat&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/daniel.molina.novoa/viz/PracticaDanielMolinafinal/DashboardEasyLoans)

---

# Dashboard preview
![Easy Loans Dashboard](./easy-loans-dashboard/dashboard-preview.png)

---

## Case Study: Easy Loans — Loan Operations Analysis (2023)
**Easy Loans** is a financial company that grants loans for purchasing products at European merchants. The goal of the analysis is to extract insights from operations carried out during 2023 to support strategic decision-making.

**Main business question:**
> *How are loan operations distributed by country, merchant, and status, and what is the cumulative revenue trend over the year?*

---

## Technical development

### Data modeling
- Connection to an Excel data source (`Easy Loans Operaciones 2023.xlsx`)
- Relational model with three tables: `Orders`, `Merchants`, and `Refunds`
- Data source filter: exclusion of operations in Morocco (European markets only)
- Saved in `.twbx` format to preserve data and settings

### Calculated fields
| Field | Description |
|-------|-------------|
| Average Loans | Average price of all loans |
| Sum of Loans | Total sum of amounts |
| Maximum / Minimum | Extreme loan values |
| Total Merchants | Count of distinct merchants |
| Total Operations | Total number of operations |
| Total Refunds | Count of refunds |
| Cumulative Value | Cumulative amount using `RUNNING_SUM` |
| Overall Average | Fixed average using `FIXED` (Level of Detail) |
| Average Deviation | Variation of the selected average vs. the overall average |
| Average Legend | Conditional field for the ▲/▼ indicator |

### Visualizations
- **Main KPI:** Average of selected loans vs. overall average, with a deviation indicator
- **Secondary KPIs:** Operations, Merchants, Maximum, Minimum, and Refunds
- **Geographic map:** Average loans by country with a color gradient
- **Line chart:** Daily cumulative amount, colored by total sum
- **Tree Map:** Top N merchants by total sum of operations
- **Pie Chart:** Distribution of operations by status (ACTIVE, CLOSED, CANCELLED, DELINQUENT)

### Interactivity
- **Global filters** applied to all sheets: Country, Status, and date range (Created At)
- **Top N parameter:** Dynamic control to filter the number of merchants shown in the Tree Map
- **Dashboard action:** Clicking on the map filters the rest of the visualizations

---

## Technologies
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)

- **Tool:** Tableau Desktop
- **Data source:** Microsoft Excel (.xlsx)
- **Publishing:** Tableau Public

---

## Repository structure
```
tableau-business-intelligence/
│
└── easy-loans-dashboard/
    ├── dashboard-preview.png     # Screenshot of the final dashboard
    └── easy-loans-analysis.twbx  # Tableau file (optional)
```

---

## Author
**Daniel Molina Novoa** · Data Analyst
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-molina-novoa/)
[![GitHub](https://img.shields.io/badge/GitHub-danielmolinan-181717?style=flat&logo=github&logoColor=white)](https://github.com/danielmolinan)
[![Tableau Public](https://img.shields.io/badge/Tableau%20Public-danielmolinan-E97627?style=flat&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/daniel.molina.novoa)
