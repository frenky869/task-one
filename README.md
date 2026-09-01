# Python for Data Science — NumPy & Pandas Basics

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.24%2B-brightgreen.svg)](https://numpy.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-blueviolet.svg)](https://pandas.pydata.org/)

An introductory data science notebook demonstrating core **NumPy** and **Pandas** operations using the classic **Titanic dataset**. This project is part of a Level 1, Day 1 task in a data science curriculum.

## 📊 Dataset

**Titanic Dataset** — passenger-level data from the RMS Titanic, containing 891 passenger records with demographic information, travel details, and survival outcomes.

### Dataset Columns

| Column | Description |
|---|---|
| `survived` | Survival indicator (0 = No, 1 = Yes) |
| `pclass` | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| `sex`, `age` | Passenger demographics |
| `sibsp`, `parch` | Number of siblings/spouses and parents/children aboard |
| `fare` | Ticket fare |
| `embarked`, `embark_town` | Port of embarkation |
| `class`, `who`, `adult_male` | Derived/descriptive fields |
| `deck`, `alive`, `alone` | Additional derived fields |

*Source: [seaborn-data / titanic.csv](https://github.com/mwaskom/seaborn-data)*

## 🎯 Learning Objectives

- **NumPy Fundamentals**: Array creation, slicing, indexing, broadcasting, and vectorization
- **Pandas Operations**: Data filtering with `.loc[]`/`.iloc[]`, grouping with `groupby()`, aggregations, and merging/joining DataFrames
- **Data Analysis**: Extract insights from the Titanic dataset using Python data science tools
- **Performance Awareness**: Understand why vectorized NumPy operations outperform Python loops

## 📁 Notebook Structure

The notebook is organized into four main sections:

### 1. NumPy Fundamentals
- Array creation (`zeros`, `ones`, `arange`, `linspace`)
- Indexing and slicing (basic, boolean/fancy, 2D)
- Broadcasting operations
- **Performance comparison**: Vectorized operations vs. Python loops

### 2. Filtering with Pandas
- Label-based selection using `.loc[]`
- Position-based selection using `.iloc[]`
- Complex filtering (women in 1st class, elderly survivors > 60)

### 3. Grouping & Aggregation
- Survival rate by passenger class
- Multiple statistics by sex (avg fare, max fare, avg age, survival rate)
- Combined class × sex breakdown with multi-index grouping

### 4. Merging & Joining
- Creating and merging lookup tables
- Comparison of `inner` vs `left` joins
- Handling missing values in merged data

## 🔍 Key Findings

1. **Overall survival rate**: **38.4%** — the majority of passengers did not survive
2. **Class mattered**: 1st class survival rate (**63.0%**) vs. 3rd class (**24.2%**)
3. **Sex mattered even more**: Female survival rate (**74.2%**) vs. male (**18.9%**), consistent with "women and children first" policy
4. **Fare distribution**: Right-skewed, average $32.20 vs. median $14.45, driven by expensive 1st-class tickets
5. **Missing data**: **19.9%** of age values missing — important consideration for age-based analysis

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/python-data-science-basics.git
   cd python-data-science-basics
