# Titanic Dataset — Exploratory Data Analysis (EDA)

- **Name:** Titanic Passenger Data
- **Source:** [kaggle.com/c/titanic/data](https://www.kaggle.com/c/titanic/data)
- **Domain:** History / Survival analysis
- **Shape:** 891 rows × 12 columns
- **Loaded via:** a public GitHub CSV mirror of the same Kaggle schema (`PassengerId`, `Survived`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, `Embarked`), so the notebook runs end-to-end with no API key or manual download required.

## 🧭 Notebook Structure

1. **Section 1 — Dataset Introduction**
   Why this dataset was chosen and what makes it a good EDA sandbox.

2. **Section 2 — The 7-Command First-Look Protocol**
   - `df.shape` — dataset dimensions
   - `df.dtypes` — column data types
   - `df.info()` — non-null counts & memory usage
   - `df.describe()` — summary statistics
   - `df.isnull().sum()` — missing value counts
   - `df['col'].value_counts()` — class balance check
   - `df.duplicated().sum()` — duplicate row check

3. **Section 3 — 22+ Additional EDA Commands**
   Includes `head`/`tail`/`sample`, `nunique`, `unique`, `corr`, histograms, `groupby`, `value_counts(normalize=True)`, `select_dtypes`, `str.contains`, `sort_values`, conditional filtering, `pivot_table`, `skew`, `kurt`, `mode`, `memory_usage`, `cov`, multi-key `groupby`, and regex-based title extraction from passenger names.

4. **Section 4 — Key Findings**
   Three data-backed takeaways in plain English:
   - Missing data (`Cabin` ~77%, `Age` ~20%) directly affects the reliability of summary statistics.
   - Survival strongly follows `Sex` and `Pclass` — 1st class women had near-100% survival, 3rd class men the lowest.
   - The target variable is imbalanced (~62% vs ~38%) and `Fare` is heavily right-skewed, both of which have direct implications for model evaluation and preprocessing.

