# 📊 Exploratory Data Analysis Portfolio

> From predicting Titanic survivors to decoding Netflix's content strategy — two data stories, one data journey.

---

## 🎯 The Mission

This portfolio showcases **two comprehensive EDA projects** demonstrating end-to-end data analysis skills — from raw data to actionable insights. Each project tells a different story: one about survival on the infamous Titanic, the other about the streaming giant that redefined entertainment.

---

## 📊 Project Overview

| Project | Dataset | Records | Focus |
|---------|---------|---------|-------|
| **Day1: Titanic EDA** | Titanic-Dataset.csv | 891 passengers | Survival factors & passenger demographics |
| **Day2: Netflix Strategy** | netflix_titles.csv | 7,787 titles | Content strategy & global distribution |

---

## 🔑 Key Findings

### Titanic — Who Survived the Unsinkable Ship?

> *"Women and children first" wasn't just a saying — it was the data speaking.*

- **Only 38.4% survived** the disaster
- **Class mattered enormously**: 1st class passengers survived at 60%+ rate vs. <25% in 3rd class
- **Gender was the biggest predictor**: 75% of women survived, but less than 20% of men
- **Having a cabin mattered**: Passengers with recorded cabin numbers had dramatically higher survival rates
- **Small families survived best**: Groups of 2-4 had the highest survival rates; solo travelers and large families suffered
- **Children were prioritized**: Infants and young children had the highest survival chance

### Netflix — Inside the Streaming Giant's Playbook

> *Netflix isn't just streaming — it's a global content machine with calculated strategy.*

- **Movies dominate the library** — nearly 70% of content is movies vs. 30% TV shows
- **"International Movies" is #1 genre** — highlighting Netflix's global content strategy
- **US leads production**, followed by India, UK, Japan, and South Korea
- **Mature audience rules** — TV-MA and TV-14 are the most common ratings
- **Movies run 80-120 minutes** — the sweet spot for viewer engagement
- **Most TV shows = 1 season** — Netflix's pilot-heavy, renewal-selective approach
- **2020 saw a dip** in new movie additions (hello, pandemic)
- **Same-year releases are common** — but Netflix also builds library with licensed classics

---

## 🛠️ Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-FF9F1C?style=for-the-badge&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-40AEF0?style=for-the-badge&logoColor=white)
![WordCloud](https://img.shields.io/badge/WordCloud-FF0099?style=for-the-badge&logoColor=white)
![ydata-profiling](https://img.shields.io/badge/ydata--profiling-FF6B6B?style=for-the-badge&logoColor=white)

</div>

---

## 📁 Project Structure

```
EDA-Projects/
├── Day1_TitanicEDA/
│   ├── Day1_TitanicEDA.ipynb    # Complete EDA notebook
│   └── data/
│       └── Titanic-Dataset.csv   # 891 passenger records
│
├── Day2_Netflix_content_strat/
│   ├── Day2_Netflix_content_strat.ipynb  # Complete EDA notebook
│   └── data/
│       └── netflix_titles.csv   # 7,787 show/movie records
│
└── README.md                     # This file
```

---

## 🔬 What I Did

### Day 1: Titanic EDA

1. **Data Loading & Inspection**
   - Loaded 891 passenger records with 12 features
   - Identified missing values in Age (177), Cabin (687), Embarked (2)

2. **Data Cleaning**
   - Filled missing Ages with median (28) — resistant to outliers
   - Filled missing Embarked with mode ('S' — Southampton)
   - Created binary `Has_Cabin` feature from 77% missing Cabin data

3. **Univariate Analysis**
   - Explored distributions: Age, Fare, Pclass, Sex, Embarked
   - Found: 3rd class dominated, more males than females, Southampton was primary port

4. **Bivariate Analysis**
   - Survival vs. Pclass, Sex, Embarked, Cabin, Age
   - Discovered: Female > Male, 1st class >> 3rd class, Cabin presence = higher survival

5. **Feature Engineering**
   - Created `FamilySize = SibSp + Parch + 1`
   - Created `IsAlone` binary feature
   - Extracted titles from Names (Mr, Mrs, Miss, Master, Rare)
   - Binned Age into categories

6. **Multivariate Analysis**
   - Pclass × Sex × Survival heatmap
   - Age distribution by Sex and Survival (violin plot)
   - Correlation matrix revealing Fare ↔ Pclass relationship

7. **Auto-Profiling**
   - Generated comprehensive YData profiling report

### Day 2: Netflix Content Strategy

1. **Data Loading & Inspection**
   - 7,787 titles with 12 features
   - Converted date strings to datetime for time analysis

2. **Data Cleaning**
   - Handled missing values in director, cast, country, date_added, rating
   - Converted string dates to datetime objects
   - Extracted year/month added for temporal analysis

3. **Content Distribution Analysis**
   - Movies vs. TV Shows pie chart (69.6% vs 30.4%)
   - Content growth over time — exponential rise until 2020 dip

4. **Genre Analysis**
   - Exploded multi-value genre column
   - Identified top 15 genres — "International Movies" leads

5. **Duration Analysis**
   - Movies: 80-120 minute sweet spot
   - TV Shows: Most have only 1 season (pilot strategy)

6. **Geographic Analysis**
   - Top content-producing countries identified
   - US dominates, India #2, UK/Japan/South Korea follow

7. **Rating Analysis**
   - Maturity ratings distribution
   - TV-MA and TV-14 dominate (mature audience focus)

8. **Feature Engineering**
   - Created `age_on_netflix = year_added - release_year`
   - Revealed acquisition strategy: same-year releases + licensed classics

9. **Multivariate Analysis**
   - Genre × Duration box plots
   - Top genres vs. movie duration patterns

10. **Text Analysis**
    - Word clouds for descriptions
    - Common keywords: Love, Life, Family, World, Story

---

## 📈 Visualizations

> *Run the notebooks to see all interactive charts!*

The notebooks contain:
- Correlation heatmaps
- Violin plots & box plots
- Bar charts & pie charts
- Histograms & KDE plots
- Time series trends
- Word clouds

---

## ▶️ How to Run

```bash
# Clone the repository
git clone https://github.com/thesibaram/eda-projects.git

# Navigate to project
cd eda-projects

# Launch Jupyter Notebook
jupyter notebook
```

Then simply open and run:
- `Day1_TitanicEDA/Day1_TitanicEDA.ipynb`
- `Day2_Netflix_content_strat/Day2_Netflix_content_strat.ipynb`

---

## 🧠 What Makes These Projects Different

| What most beginners do | What I did instead |
|---|---|
| Drop missing values blindly | Converted 77% missing Cabin data into a survival signal via binary encoding |
| Use mean for imputation | Used median for Age (skewed data), mode for Embarked (categorical) — with reasoning |
| Treat genres as single values | Exploded multi-value genre column to get accurate frequency counts |
| Ignore time columns | Engineered `age_on_netflix` to reverse-engineer Netflix's acquisition strategy |
| Stop at bar charts | Used violin plots, KDE density plots, bigram word clouds, and YData auto-profiling |

---

## 📝 Conclusion

> *The best EDA doesn't just describe data — it changes how you see the problem.*

**Titanic** taught me that the most powerful signals are often hiding inside missing values and indirect proxies — not the obvious columns.

**Netflix** taught me that business strategy leaves fingerprints in data. A timestamp column revealed an entire content acquisition playbook.

More EDA projects coming as the challenge progresses. Each one a different domain. Each one a different story.

---

<div align="center">

### 🙋‍♂️ Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sibaram-eng)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/thesibaram)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sibaram.work@gmail.com)

---

*Part of the [GFG 21 Days 21 Projects](https://www.geeksforgeeks.org/courses/twenty-projects-in-twenty-days) challenge*

*Built by **Sibaram** — 2nd Year EE @ Parala Maharaja Engineering College*

</div>
