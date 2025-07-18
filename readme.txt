# Aave V2 Wallet Credit Scoring

## 📌 Overview

This project analyzes transaction behaviors of wallets interacting with the Aave V2 DeFi protocol and assigns a **credit score between 0 and 1000** to each wallet.

**Goal:**  
Identify reliable vs. risky wallets based purely on historical usage patterns.

---

## 📊 Approach

- **Input Data:** JSON file with transaction-level data.
- **Process:**
  - Load and parse transaction logs.
  - Feature engineering:
    - Deposits, borrows, repayments, liquidations, transaction frequency.
  - Behavior-based scoring:
    - Positive signals boost score.
    - Negative signals reduce score.
  - Normalize and scale results between 0 and 1000.

- **Output:** CSV file mapping each wallet to its credit score.

---

## 📁 Folder Structure

```
aave-wallet-credit-scoring/
├── data/
│   └── sample_transactions.json
├── notebooks/
│   └── wallet_scoring.ipynb
├── wallet_scoring.py
├── wallet_scores.csv
├── README.md
└── analysis.md
```

---

## 📋 Usage Instructions

1. Place your JSON file in the `/data/` folder.
2. Install required libraries:
```bash
pip install pandas numpy scikit-learn
```
3. Run:
```bash
python wallet_scoring.py
```

4. Check `wallet_scores.csv` for results.

---

## 📊 Sample Output

| wallet_address      | credit_score |
|---------------------|--------------|
| 0xabc123...         | 55           |
| 0xdef456...         | 312          |
| 0xghi789...         | 405          |

---

## 📊 Score Distribution

See [`analysis.md`](analysis.md) for score interpretation and wallet behavior insights.
