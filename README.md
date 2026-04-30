## Market Basket Analysis — Online Retail UK

This project applies the **Apriori algorithm** to over 1 million real-world transactions from a UK-based online gift retailer (2009–2011) to discover meaningful product associations — the kind that answer "people who buy X also buy Y."

### What this project does
- Cleans and preprocesses 1,067,371 raw transactional records (removes cancellations, returns, and missing values)
- Builds a basket matrix across 30,794 unique UK customer invoices
- Mines frequent itemsets at 1% minimum support using a custom Apriori implementation (no external ML libraries)
- Generates 538 association rules ranked by lift, confidence, and support
- Exports analysis-ready CSVs and visualizes results in an interactive Tableau dashboard

### Key findings
- Strongest association: lift of 53.95 (54× more likely than random chance)
- Average rule confidence: 39.1%
- Top product families: Poppy's Playhouse sets, Red Spotty party ranges, Scandinavian Christmas decorations

### Tech stack
Python · pandas · NumPy · Tableau Public

### Files
| File | Description |
|------|-------------|
| `Market_Basket_Analysis.ipynb` | Full Jupyter notebook with cleaning, Apriori, and export |
| `association_rules.csv` | 538 rules with support, confidence, lift |
| `heatmap_data.csv` | 20×20 item-pair matrix for Tableau heatmap |
| `item_frequency.csv` | Top 600 frequent items |
| `network_edges.csv` | Top 80 rules for network graph |

### Dataset
UCI Online Retail II — available on [Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)
