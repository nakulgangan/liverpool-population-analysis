# 🏥 Healthcare Activity Dashboard — Hospice Clinical Reporting Simulation

> Simulating a Power BI-ready data pipeline for children's hospice clinical activity reporting, using SQL, Python, and interactive visualisation. Inspired by the data reporting requirements of organisations like Rainbows Hospice for Children and Young People.

---

## 📌 Project Overview

Children's hospices serve some of the most vulnerable patients — babies, children, and young people with life-limiting conditions — across multiple care settings (hospice, hospital, home). This project simulates the end-to-end data workflow a Data Analyst would own: extracting clinical activity data, validating quality, and producing commissioner-ready reports and dashboards.

**Key skills demonstrated:** SQL (schema design, aggregation, QA/QC), Python ETL, Power BI-style dashboard design, contract monitoring, statutory reporting.

---

## 📊 Dashboard Preview

![Clinical Activity Dashboard](dashboard.png)

---

## 🗂️ Repository Structure

```
project1_healthcare_dashboard/
├── analysis.py          # Python ETL pipeline + visualisation
├── sql_queries.sql      # SQL schema + 5 production queries
├── dashboard.png        # Output dashboard (Power BI-ready design)
└── README.md
```

---

## 🔑 Key Findings

| Metric | Result |
|--------|--------|
| Total patients served | **768** (exceeds 750 target ✅) |
| Total care episodes | **3,200** across 24 months |
| Family/carer reach | **3,568** people across East Midlands |
| Largest care setting | Home care (80% of patients) |
| Palliative episodes | 40% of all activity |
| Data completeness | **100%** after QA/QC validation |
| Contract compliance | Palliative & Respite ON TARGET; End-of-Life flagged AMBER Q3–Q4 |

---

## 🛠️ Technical Approach

### SQL Queries (`sql_queries.sql`)

| Query | Purpose |
|-------|---------|
| 1. Monthly Activity Summary | Aggregates episodes by care setting and service type — direct input to Power BI |
| 2. Data Quality Validation | Flags nulls, orphaned records, invalid durations — mirrors real SystmOne export QA |
| 3. Rolling 12-Month KPIs | Calculates dashboard card values (unique patients, setting breakdown) |
| 4. Contract Compliance RAG | Actual vs target by commissioner — GREEN/AMBER/RED status |
| 5. Family Support Impact | Regional reach of wider family/carer support — demonstrates H&SC system impact |

### Python Pipeline (`analysis.py`)

- **Data generation:** 780 patients, 3,200 episodes, 2,800 family contacts with realistic distributions
- **ETL validation:** Null checks, duplicate detection, referential integrity, completeness scoring
- **KPI calculation:** Total reach, setting breakdown, service mix
- **Visualisation:** 4-panel dashboard — KPI cards, monthly episode bar chart, age×service heatmap, contract RAG, regional family support

---

## 💻 How to Run

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn

# Run analysis and generate dashboard
python analysis.py
```

---

## 🔗 Relevance to Healthcare Reporting

This project directly mirrors the reporting workflow at a children's hospice:
- **SystmOne-style data extraction** → validated with SQL QA queries
- **ThankQ/CRM-adjacent** family support tracking
- **Commissioner reporting** with contract compliance RAG status
- **Statutory body requirements** — structured for NHS/ICB submission formats

---

## 👤 Author

**Nakul Gangan** | MSc Geographic Data Science, University of Liverpool  
[LinkedIn](https://linkedin.com/in/nakulgangan066207104) | nakulgangan@gmail.com
