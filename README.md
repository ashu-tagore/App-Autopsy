# Google Play Store EDA — 500K+ Apps

A structured exploratory data analysis of the Google Play Store dataset, organized around four strategic lenses for app developers and product strategists.

---

## Project Structure

```
google_play_eda/
├── data/
│   ├── raw/                  # Original dataset files (not tracked by git)
│   └── processed/            # Cleaned & feature-engineered outputs
├── notebooks/
│   └── eda_google_play.ipynb # Single master notebook (all 15 questions)
├── outputs/
│   ├── charts/               # Saved visualizations (PNG/HTML)
│   └── reports/              # Summary markdown/HTML reports
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Dataset

**Source:** [Google Play Store Apps (500K+) — Kaggle](https://www.kaggle.com/datasets/)

Place the raw CSV(s) inside `data/raw/` before running the notebook.

---

## Setup

```bash
# 1. Clone the repo
git clone <your-repo-url>
cd google_play_eda

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter lab notebooks/eda_google_play.ipynb
```

---

## Analysis Questions (15 Total)

### 🔍 Before You Build — Market Strategy
| # | Question |
|---|----------|
| Q1 | Which categories are oversaturated vs underserved? |
| Q2 | What monetization model dominates successful apps? |
| Q3 | Is there a price sweet spot for paid apps? |

### 🚀 Launch Strategy — Maximizing Early Traction
| # | Question |
|---|----------|
| Q4 | What minimum rating count makes a star rating trusted? |
| Q5 | Does review volume matter more than star rating for installs? |
| Q6 | What app size (MB) maximizes installs? |

### 📈 Growth — What Keeps Apps Relevant
| # | Question |
|---|----------|
| Q7 | Do apps that update more frequently get better ratings? |
| Q8 | How long after launch do successful apps release their first update? |
| Q9 | Is there a seasonal pattern to app launches? |

### ⭐ Quality Signals — What Makes Users Rate You Well
| # | Question |
|---|----------|
| Q10 | Which category has the highest bar for a "good" rating? |
| Q11 | Do apps with privacy policy, website & email get better ratings? |
| Q12 | What content rating produces the most installs per category? |

### 🏆 Standing Out — Getting Featured & Going Viral
| # | Question |
|---|----------|
| Q13 | What profile does an Editor's Choice app have? |
| Q14 | Do ad-free apps outperform ad-supported apps in ratings? |
| Q15 | What does a top 1% install app look like vs a median app? |

---

## Output

Each question produces:
- A chart saved to `outputs/charts/Q{N}_<slug>.png`
- A brief written finding in the notebook cell below the chart

---

## License

For educational and analytical use only. Dataset rights belong to respective owners.