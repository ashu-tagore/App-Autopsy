# App Autopsy — Decoding the Google Play Store

Exploratory data analysis of 2.3M+ Google Play Store apps across 15 strategic questions for app developers and product teams.

---

## Project Structure

```
app-autopsy/
├── data/
│   ├── raw/                  # Original dataset (not tracked by git)
│   └── processed/            # Cleaned & feature-engineered outputs
├── notebooks/
│   └── eda.ipynb             # Master notebook (all 15 questions)
├── outputs/
│   └── charts/               # Saved visualizations (PNG)
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Dataset

**Source:** [Google Play Store Apps — Kaggle](https://www.kaggle.com/datasets/gauthamp10/google-playstore-apps) by Gautham Prakash (scraped June 2021)

Place the CSV inside `data/raw/` before running the notebook.

---

## Setup

```bash
git clone https://github.com/ashu-tagore/App-Autopsy
cd google_play_eda
python -m venv venv && source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter lab notebooks/eda.ipynb
```

**Stack:** Python · Pandas · NumPy · Matplotlib · Seaborn · SciPy

---

## Analysis Questions (15 Total)

### Market Strategy — Before You Build
| # | Question |
|---|----------|
| Q1 | Which categories are oversaturated vs underserved? |
| Q2 | What monetization model dominates the top 10% of installs — and does it differ by category? |
| Q3 | Does the IAP model correlate with higher median installs than purely free apps? |

### Launch Strategy — Early Traction
| # | Question |
|---|----------|
| Q4 | What minimum review count makes a rating statistically trustworthy (SE < 0.1)? |
| Q5 | Does review volume correlate more strongly with installs than star rating? |
| Q6 | Do more frequently updated apps have higher ratings? |

### Growth & Distribution
| # | Question |
|---|----------|
| Q7 | What is the install-to-review conversion rate by category? |
| Q8 | Does the install distribution follow a power law? |
| Q9 | Which category has the highest bar for a "good" rating? |

### Quality Signals
| # | Question |
|---|----------|
| Q10 | Does developer portfolio size predict individual app rating? |
| Q11 | Do ad-free apps have higher ratings than ad-supported apps? |
| Q12 | What content rating produces the most median installs per category? |

### Standing Out
| # | Question |
|---|----------|
| Q13 | What does a top 1% install app look like vs a median app? |
| Q14 | Do apps with shorter names get more installs? |
| Q15 | What share of apps are "zombie apps" — not updated in 2+ years? |

---

## Key Findings

- **Category selection** is the highest-leverage pre-build decision; underserved categories yield structurally more installs per unit effort.
- **Free+Ads dominates** the top 10% by installs. Paid models reduce reach by 10–50× vs free alternatives.
- **IAP correlates with higher installs** — it signals product maturity rather than acting as a paywall.
- **Review count (ρ ≈ 0.7)** is a far stronger install predictor than star rating (ρ ≈ 0.1).
- **~100 reviews** is the practical threshold for a statistically trustworthy rating.
- **Zombie-heavy categories** (not updated in 2+ years) present easier ranking opportunities for maintained apps.

---

## License

For educational and analytical use only. Dataset rights belong to respective owners.
