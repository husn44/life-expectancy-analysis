# Global Life Expectancy Analysis

Exploring which health, economic and social factors drive differences in life expectancy across 193 countries (2000–2015).

## Dataset
[Life Expectancy (WHO)](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) (Kaggle): 2,938 records, 22 health, economic and demographic indicators.

## Key Findings
- **Schooling** has the strongest positive correlation with life expectancy (r = 0.75)
- **Adult mortality** has a strong negative correlation (r = −0.70)
- **GDP** shows a logarithmic pattern: life expectancy rises quickly at low income levels, then levels off
- GDP and health expenditure are almost perfectly linked (r = 0.90)

## Data Preprocessing
- **Missing values:** two-step mean imputation, first by country across years, then by development status (Developed/Developing)
- **Outliers:** IQR-based capping (winsorization) on selected variables only, keeping real-world extremes like GDP and population
- **Transformation:** encoded development status and applied Min-Max normalisation
- **Data reduction:** removed redundant features (e.g. infant deaths, already included in under-five deaths)

## Tech Stack
Python · Pandas · Matplotlib · Seaborn · scikit-learn

## Files
| File | Description |
|---|---|
| `life_expectancy_analysis.ipynb` | Business understanding, EDA and data preprocessing |
| `Life_Expectancy_Data.csv` | Dataset |
