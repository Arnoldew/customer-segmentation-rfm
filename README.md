# Customer Segmentation with RFM Analysis

Segmenting 4,338 retail customers based on purchasing behavior using the RFM (Recency, Frequency, Monetary) framework — with actionable marketing strategies per segment.

---

## Dataset

**Source:** UCI Machine Learning Repository — [Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail)

| Attribute | Detail |
|-----------|--------|
| Period | December 2010 – December 2011 |
| Total transactions | ~541,000 rows |
| Customers analyzed | 4,338 unique CustomerIDs (after cleaning) |
| Region | Primarily United Kingdom |

---

## Tools

- Python (Pandas, NumPy)
- Matplotlib, Seaborn
- Jupyter Notebook

---

## How RFM Works

RFM measures three dimensions of customer behavior:

| Metric | Question | Scoring |
|--------|----------|---------|
| **Recency (R)** | How recently did they buy? | Lower = better → score reversed |
| **Frequency (F)** | How often do they buy? | Higher = better |
| **Monetary (M)** | How much do they spend? | Higher = better |

Each metric is scored 1–5 using quantile-based scoring (quintiles), so customers are distributed evenly across score bands. Final RFM score is a combination of R + F + M scores, which maps each customer to one of 5 segments.

---

## Customer Segments

| Segment | Customers | Recency (avg) | Frequency (avg) | Monetary (avg) |
|---------|-----------|---------------|-----------------|----------------|
| Champions | — | ~5 days | ~18 transactions | ~11,221 |
| Loyal Customers | ~791 (~18%) | ~16 days | ~6 transactions | ~2,556 |
| At Risk | — | ~137 days | ~4 transactions | ~1,575 |
| New Customers | — | — | ~1 transaction | ~458 |
| Others | ~60% of total | — | ~2 transactions | low |

---

## Key Findings

**Champions** are the top revenue drivers. They buy frequently, spent the most, and came back recently. Small in number but high in value — the priority is keeping them.

**Loyal Customers** (~18%) are stable and active. They haven't reached Champion level yet, but they're close. The gap between them and Champions is mostly in spend per transaction.

**At Risk** customers used to be active — 4 transactions on average with decent spend — but haven't bought in ~137 days. This is the most urgent segment to address before they're gone.

**New Customers** made exactly one purchase. They have no loyalty signal yet, which means the onboarding experience matters a lot here.

**Others** make up 60% of the customer base. Low frequency, low spend, irregular recency. The segment is too broad to target efficiently without further splitting.

---

## Business Recommendations

| Segment | Strategy |
|---------|----------|
| Champions | VIP program, early access to new products, loyalty rewards |
| Loyal Customers | Bundle promotions, cross-selling, loyalty points |
| At Risk | Reactivation email campaign, targeted discount, personal outreach |
| New Customers | Welcome discount, onboarding series, product recommendations |
| Others | Retargeting ads, marketing automation, low-cost engagement |

---

## Project Structure
```
customer-segmentation-rfm/
│
├── data/
│   └── online_retail.xlsx         # Raw dataset
│
├── notebook/
│   └── rfm_analysis.ipynb         # Full analysis notebook
│
├── visuals/
│   ├── rfm_segment_distribution.png
│   ├── recency_distribution.png
│   ├── frequency_distribution.png
│   └── monetary_distribution.png
│
└── README.md
```

---

## How to Run
```bash
# Clone the repo
git clone https://github.com/Arnoldew/customer-segmentation-rfm.git
cd customer-segmentation-rfm

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter openpyxl

# Launch notebook
jupyter notebook notebook/rfm_analysis.ipynb
```

---

## Author

**Arnoldew Ray Ruby**
- GitHub: [@Arnoldew](https://github.com/Arnoldew)
- LinkedIn: [arnoldew-ray-ruby](https://www.linkedin.com/in/arnoldew-ray-ruby/)

---

*Part of a 10-project data analyst portfolio.*
