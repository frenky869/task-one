# Task 1: Python for Data Science — NumPy & Pandas Basics

## Dataset

**Titanic Dataset** — passenger-level data from the RMS Titanic (891 passengers), including
demographic info (age, sex, class), travel details (fare, embarkation port), and the outcome
of interest (survived or not).

Source: [seaborn-data / titanic.csv](https://github.com/mwaskom/seaborn-data)

| Column | Description |
|---|---|
| `survived` | 0 = No, 1 = Yes |
| `pclass` | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| `sex`, `age` | Passenger demographics |
| `sibsp`, `parch` | # siblings/spouses, # parents/children aboard |
| `fare` | Ticket fare |
| `embarked`, `embark_town` | Port of embarkation |
| `class`, `who`, `adult_male`, `deck`, `alive`, `alone` | Derived/descriptive fields |

## Approach

The notebook (`task1_numpy_pandas.ipynb`) is organized into four sections:

1. **NumPy Fundamentals** — array creation (`zeros`, `ones`, `arange`, `linspace`), indexing
   and slicing (including boolean/fancy indexing and 2D slicing), and broadcasting
   (elementwise scalar ops, matrix + vector broadcasting), with a timed comparison showing
   why vectorized NumPy operations outperform plain Python loops.
2. **Filtering** — label-based selection with `.loc[]` and position-based selection with
   `.iloc[]` to answer questions like "which women were in 1st class?" and "which passengers
   over 60 survived?"
3. **Grouping & Aggregation** — `groupby()` combined with `.agg()` to compute survival rate
   by class, multiple statistics (avg fare, max fare, avg age, survival rate) by sex, and a
   combined class × sex breakdown.
4. **Merging/Joining** — a small lookup table merged onto the main DataFrame, plus a
   side-by-side comparison of `inner` vs `left` joins to show how row counts and missing
   values differ between the two.

## Key Findings

1. **Overall survival rate: ~38%** — the majority of passengers did not survive.
2. **Class mattered a lot**: 1st class passengers survived at a much higher rate than 3rd
   class passengers (roughly 63% vs 24%).
3. **Sex mattered even more**: women survived at a far higher rate than men (roughly 74% vs
   19%), consistent with the "women and children first" evacuation policy.
4. **Fares were right-skewed**: the average fare (~$32) was notably higher than the median
   (~$14), driven by a small number of expensive 1st-class tickets.
5. **Missing data**: ~20% of passengers are missing an `age` value, which is important to
   account for before doing age-based analysis.

## How to Run

```bash
pip install numpy pandas jupyter
jupyter notebook task1_numpy_pandas.ipynb
```
