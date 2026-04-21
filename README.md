# 📊 AI Data Report Generator — Live Demo

> Upload CSV/Excel → get a full management report with charts, KPIs, and AI executive summary in 30 seconds.

**[🔴 Live Demo](https://twojname.github.io/data-report-demo)** &nbsp;|&nbsp; Built by [Tomasz Witkowski](mailto:tomekw2323@gmail.com)

---

## What it does

1. **Ingests** any CSV, Excel file, or Google Sheets link
2. **Computes** KPIs, statistics, and trends with pandas
3. **Visualizes** data as charts with matplotlib
4. **Writes** an executive summary with Claude AI — in the correct language, with real numbers
5. **Exports** a branded PDF ready to forward to management

Average time saved: **~3 hours per week** for any team that produces regular reports manually.

---

## Demo

The `index.html` is a fully interactive browser demo. It uses 4 built-in sample datasets and calls Claude API live to generate the AI summary section.

### Deploy to GitHub Pages
1. Fork this repo
2. Go to **Settings → Pages → Deploy from branch → main / root**
3. Live at `https://yourusername.github.io/data-report-demo`

---

## Python Pipeline (production)

```bash
git clone https://github.com/yourusername/data-report-demo
cd data-report-demo
pip install -r requirements.txt
cp .env.example .env
# Set ANTHROPIC_API_KEY in .env
python generate_report.py --input data/sales.csv --output reports/
```

### Supported inputs

| Format | Notes |
|---|---|
| `.csv` | Any delimiter |
| `.xlsx` / `.xls` | All sheets |
| Google Sheets URL | Requires Sheets API key |
| Manual JSON | For API integration |

### Stack

| Component | Library |
|---|---|
| Data processing | pandas, numpy |
| Charts | matplotlib, seaborn |
| AI summary | Claude API (claude-opus-4-5) |
| PDF export | ReportLab |
| Scheduling | cron / APScheduler |
| Email delivery | smtplib / SendGrid |

---

## Sample output

```
MONTHLY SALES REPORT — Acme Corp.
Period: Jan–Dec 2024 | Generated: 2024-04-15

KPIs
├─ Total Revenue: €611,200
├─ YoY Growth: +24%
├─ Best Month: December (€67,200)
└─ Avg Monthly: €50,933

[Bar chart: monthly revenue]
[Doughnut chart: regional split]

AI EXECUTIVE SUMMARY
Revenue grew consistently throughout 2024, with Q4 showing the 
strongest performance at €184,400 — 30% of annual total. The North 
region continues to lead at 34% of revenue, while the West region 
(16%) presents an underexploited growth opportunity...

INSIGHTS
✓ Q4 surge exceeded forecast by 18%
⚠ West region growth stalled at 2% — review territory coverage
✓ Customer retention improved — repeat orders +11% YoY
✗ March dip (-4%) linked to logistics delays — monitor
```

---

## Contact

Want this automated for your business? I set it up, configure it, and hand it over — ready to run.

**Tomasz Witkowski** — Automation & AI specialist  
📧 tomekw2323@gmail.com  
📱 +48 784 237 870  
🔗 [LinkedIn](https://linkedin.com/in/twojprofil)

---

*Demo runs in browser. Production pipeline is pure Python — no cloud lock-in, runs on any server or locally.*
