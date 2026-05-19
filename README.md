# 🔧 Smart Condition-Based Maintenance System (CBMS)

## 📋 Project Overview
An intelligent maintenance system that reads technician daily observations written in natural language and automatically classifies them into actionable maintenance priorities using NLP and Machine Learning.

---

## 🚨 The Problem
Traditional maintenance systems rely on fixed periodic schedules (every 3 or 6 months). This approach has two major flaws:
- **Over-maintenance** — servicing engines that don't need it yet
- **Under-maintenance** — missing critical issues that appear between scheduled dates

This project solves this by analyzing what the technician **actually observes** every morning.

---

## 💡 The Solution
Every morning the technician writes a statement about each engine:
- *"everything looks fine today"*
- *"noticed small oil stain under engine"*
- *"massive oil leak engine cannot start"*

The system reads these statements and instantly:
1. **Classifies** the severity level
2. **Recommends** the exact action to take
3. **Archives** every intervention for future reference

---

## 🎯 Classification Labels

| Label | Meaning | Example |
|-------|---------|---------|
| 🟢 Normal | No action needed | *"engine running smoothly"* |
| 🟡 Intervention Later | Schedule soon | *"belt shows signs of wear"* |
| 🔴 Urgent Intervention | Stop engine now | *"oil leak detected"* |

---

## 🛠️ Technical Approach

### Step 1 — Data Simulation
- Generated 210 labeled technician statements
- 70 per category — perfectly balanced dataset
- Covers 44 engines across 5 categories

### Step 2 — NLP Pipeline
- Text cleaning and preprocessing
- TF-IDF Vectorization (134 features)
- Train/Test split (80/20)

### Step 3 — Model Training
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 93% |
| **Random Forest** | **95%** ✅ |

### Step 4 — Recommendation Engine
- Maps classification → specific action
- Identifies affected component (oil/coolant/belt/battery)
- Assigns correct priority level

### Step 5 — Archive System
- Records every intervention with date and engine ID
- Identifies most problematic engines
- Generates next maintenance recommendations

---

## 📈 Results
- ✅ 95% classification accuracy
- ✅ Normal statements never confused with Urgent
- ✅ Component-specific recommendations
- ✅ Full intervention history archived

---

## 🗂️ Repository Structure
cbms-nlp-classifier/
├── cbms_nlp_classifier.ipynb
├── data/
│   ├── daily_checks.csv
│   └── interventions_archive.csv
└── visuals/
├── label_distribution.png
├── top_words_per_category.png
└── confusion_matrix_cbms.png
---

## 🧰 Tools Used
- **Python** — Pandas, Scikit-learn, Matplotlib, Seaborn
- **NLP** — TF-IDF Vectorization, Text Classification
- **ML Models** — Logistic Regression, Random Forest
- **GitHub** — Version Control

---

## 🔗 Related Project
This project is a continuation of:
[Smart Engine Maintenance System](https://github.com/teachermarouane-ops/engine-maintenance-portfolio)

---

## 👤 Author
**teachermarouane-ops**
ALX Data Science Program — Portfolio Project 2026
