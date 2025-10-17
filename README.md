# 🌐 Global Cyberattack Pattern Analysis (Data Mining Project)

This project analyzes global cyberattack patterns using the **CISA Known Exploited Vulnerabilities (KEV)** dataset (2021–2025).  
It applies **data mining techniques** including **Exploratory Data Analysis (EDA)**, **Clustering (K-Means)**, **Association Rules**, and **Classification (Random Forest, SVM)**  
to identify vulnerability trends and predict response speed.

---

## 📊 Dataset Overview
- **Source:** `data/cisa_kev.csv` (CISA KEV)
- **Records:** ~1,400+
- **Columns:** `vendorProject`, `product`, `vulnerabilityName`, `dateAdded`, `cwe_primary`, `ransomware_known`, etc.
- **Top Vendors:** Microsoft, Adobe, Apple, Cisco, Google

---

## 🧠 Methods
| Category | Description |
|-----------|-------------|
| **Exploratory Data Analysis (EDA)** | Year-wise vulnerability counts, vendor distribution, top CWE weaknesses |
| **Clustering** | K-Means (optimal K = 3, silhouette = 0.183) |
| **Association Rules** | Apriori algorithm to discover vendor + CWE relationships |
| **Classification** | Random Forest and SVM predicting `response_speed` (Fast / Medium / Slow) |

---

## 📈 Model Performance
| Model | Accuracy | Precision | Recall | F1-Score |
|--------|-----------|------------|----------|-----------|
| **Random Forest** | **0.91** | 0.94 | 0.90 | 0.91 |
| **SVM (Linear)** | 0.85 | 0.87 | 0.84 | 0.83 |

> 🏆 **Best model:** Random Forest achieved the highest accuracy for predicting response speed.

---

## 🧩 Visualizations
- 📊 **Confusion Matrices:** `reports/supervised/rf_confusion.png`, `reports/supervised/svm_confusion.png`
- 🧭 **Clustering Plot:** `reports/unsupervised/kmeans_svd2d.png`
- 📅 **Trend Charts:** `reports/eda_visuals/vulns_by_year.png`

> To display inline visuals, you can uncomment this line:  
> `![Random Forest Confusion](reports/supervised/rf_confusion.png)`

---

## ⚙️ Setup & Execution
### 🧱 Option 1 — Conda
```bash
conda env create -f environment.yml
conda activate cyberdm
jupyter lab


### 🔎 Key Insights 🔎
<p>
<strong>Top Vendors:</strong> Microsoft &gt; Adobe &gt; Apple &gt; Cisco &nbsp;&nbsp; •
</p>
<p>
<strong>Frequent CWE Codes:</strong> CWE-20 (Input Validation), CWE-119 (Buffer Overflow) &nbsp;&nbsp; •
</p>
<p>
<strong>Best Model:</strong> Random Forest (≈ 91% accuracy) &nbsp;&nbsp; •
</p>

</div>

<hr>

<!-- Future work (centered + bullet-like dots on the right) -->
<div align="center">

### 🚀 Future Work
<p style="margin:6px 0;">.Extend dataset with post-2025 vulnerabilities for trend forecasting &nbsp;&nbsp; •</p>
<p style="margin:6px 0;">.Use <strong>Deep Learning</strong> (e.g., BERT / LSTM) for text-based CWE description modeling &nbsp;&nbsp; •</p>
<p style="margin:6px 0;">.Build an <strong>interactive dashboard</strong> (Streamlit / Dash) for real-time visualization &nbsp;&nbsp; •</p>
<p style="margin:6px 0;">.Experiment with <strong>DBSCAN / Hierarchical Clustering</strong> for richer group separation &nbsp;&nbsp; •</p>
<p style="margin:6px 0;">.Apply <strong>time-series forecasting</strong> (Prophet) to predict future attack waves &nbsp;&nbsp; •</p>

</div>

<hr>

<!-- References (centered) -->
<div align="center">

### 📚 References
<p style="margin:6px 0;">• CISA Known Exploited Vulnerabilities (KEV)</p>
<p style="margin:6px 0;">• CWE™ (Common Weakness Enumeration) — MITRE</p>
<p style="margin:6px 0;">• Libraries: Scikit-Learn, MLxtend, Matplotlib, Seaborn</p>

</div>

<hr>

<p align="center">👩‍💻 <strong>Author:</strong> Raghad A. &nbsp;&nbsp; 🔒 Academic / Educational Use</p>

