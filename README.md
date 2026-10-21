# India-Stocks-1471-1500-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1471 to 1500)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1471-1500-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1471 to 1500)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1471 | `KKCL` | Kewal Kiran Clothing Limited | `KKCL.NS` |
| 1472 | `KLBRENG-B` | Kilburn Engineering Limited | `KLBRENG-B.NS` |
| 1473 | `KMCSHIL` | K M C Speciality Hospitals (India) Limited | `KMCSHIL.NS` |
| 1474 | `KMEW` | Knowledge Marine & Engineering Works Limited | `KMEW.NS` |
| 1475 | `KMSUGAR` | K.M.Sugar Mills Limited | `KMSUGAR.NS` |
| 1476 | `KNACK` | Knack Packaging Limited | `KNACK.NS` |
| 1477 | `KNAGRI` | KN Agri Resources Limited | `KNAGRI.NS` |
| 1478 | `KNRCON` | KNR Constructions Limited | `KNRCON.NS` |
| 1479 | `KOHINOOR` | Kohinoor Foods Limited | `KOHINOOR.NS` |
| 1480 | `KOKUYOCMLN` | Kokuyo Camlin Limited | `KOKUYOCMLN.NS` |
| 1481 | `KOLTEPATIL` | Kolte - Patil Developers Limited | `KOLTEPATIL.NS` |
| 1482 | `KOPRAN` | Kopran Limited | `KOPRAN.NS` |
| 1483 | `KOTARISUG` | Kothari Sugars And Chemicals Limited | `KOTARISUG.NS` |
| 1484 | `KOTHARIPET` | Kothari Petrochemicals Limited | `KOTHARIPET.NS` |
| 1485 | `KOTHARIPRO` | Kothari Products Limited | `KOTHARIPRO.NS` |
| 1486 | `KOTIC` | Kothari Industrial Corporation Limited | `KOTIC.NS` |
| 1487 | `KOTYARK` | Kotyark Industries Limited | `KOTYARK.NS` |
| 1488 | `KOVAI` | Kovai Medical Center & Hospital Limited | `KOVAI.NS` |
| 1489 | `KPEL` | K.P. Energy Limited | `KPEL.NS` |
| 1490 | `KPIGREEN` | KPI Green Energy Limited | `KPIGREEN.NS` |
| 1491 | `KPL` | Kwality Pharmaceuticals Limited | `KPL.NS` |
| 1492 | `KRBL` | KRBL Limited | `KRBL.NS` |
| 1493 | `KREBSBIO` | Krebs Biochemicals and Industries Limited | `KREBSBIO.NS` |
| 1494 | `KRIDHANINF` | Kridhan Infra Limited | `KRIDHANINF.NS` |
| 1495 | `KRISHANA` | Krishana Phoschem Limited | `KRISHANA.NS` |
| 1496 | `KRISHIVAL` | Krishival Foods Limited | `KRISHIVAL.NS` |
| 1497 | `KRISHNADEF` | Krishna Defence And Allied Industries Limited | `KRISHNADEF.NS` |
| 1498 | `KRITI` | Kriti Industries (India) Limited | `KRITI.NS` |
| 1499 | `KRITIKA` | Kritika Wires Limited | `KRITIKA.NS` |
| 1500 | `KRITINUT` | Kriti Nutrients Limited | `KRITINUT.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream KKCL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1471-1500-Historical-Data/main/KKCL/1m/2026/10/KKCL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
