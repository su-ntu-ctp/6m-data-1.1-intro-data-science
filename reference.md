# 📖 Reference: Intro to Data Science

> A quick-reference companion for Lesson 1.1. Bookmark this and return to it throughout the course.

---

## Glossary

| Term | Definition |
|------|-----------|
| **Data Analytics** | The process of examining historical data to explain past events and identify trends. Answers: *"What happened?"* |
| **Data Science** | An interdisciplinary field covering the full data lifecycle — collection, cleaning, analysis, and modelling — to predict future outcomes. |
| **Artificial Intelligence (AI)** | Systems that can perform complex tasks autonomously by learning from data, without explicit step-by-step programming. |
| **Data Pipeline** | A sequence of data processing steps: Collect → Clean → Analyse → Visualise. |
| **Structured Data** | Data with a predefined schema stored in rows and columns (e.g., spreadsheets, SQL tables). |
| **Unstructured Data** | Data with no fixed format — images, audio, video, free text. Requires specialised tools to process. |
| **Semi-Structured Data** | Data that has some organisational structure but no rigid schema (e.g., JSON, XML, email). |
| **Selection Bias** | A distortion that occurs when the data collected does not represent the full population of interest. |
| **Historical Bias** | Bias encoded in data that reflects past inequalities or societal prejudices. |
| **Garbage In, Garbage Out (GIGO)** | The principle that flawed input data produces flawed outputs, regardless of how sophisticated the analysis is. |

---

## The Data Science Hierarchy of Needs

*(Based on Monica Rogati's framework)*

```
        ┌─────────────────────┐
        │        AI / ML      │  ← Tier 5: Automated intelligence
        ├─────────────────────┤
        │    Data Science     │  ← Tier 4: Prediction & modelling
        ├─────────────────────┤
        │   Data Analytics    │  ← Tier 3: Reporting & insight
        ├─────────────────────┤
        │   Data Engineering  │  ← Tier 2: Pipelines & infrastructure
        ├─────────────────────┤
        │   Data Collection   │  ← Tier 1: Raw data capture
        └─────────────────────┘
```

You must build each level before the next becomes possible.

---

## The 4-Stage Data Pipeline

| Stage | Purpose | Common Tools | Failure Point |
|-------|---------|--------------|---------------|
| 1. Collection | Capture raw data from sources | APIs, sensors, forms, scraping | Missing data, connection errors |
| 2. Cleaning | Fix errors, handle gaps, standardise | Pandas, SQL, OpenRefine | Biased imputation, lost records |
| 3. Analysis | Explore patterns, test hypotheses | Python, R, SQL, Excel | Spurious correlations, overfitting |
| 4. Visualisation | Communicate findings clearly | Matplotlib, Tableau, Power BI | Misleading charts, wrong audience |

---

## Bias Types Quick Reference

| Bias Type | What it means | Example |
|-----------|--------------|---------|
| Selection Bias | Sample doesn't represent the population | Surveying only smartphone users |
| Historical Bias | Past inequalities encoded in the data | 1970s hiring data (95% male managers) |
| Confirmation Bias | Only collecting data that confirms existing belief | Cherry-picking positive customer reviews |
| Reporting Bias | Some outcomes are more likely to be recorded | Only capturing hospital deaths, not recoveries |
| Automation Bias | Over-trusting AI decisions without human review | Amazon's scrapped hiring tool (2018) |

---

## Key Readings

- Monica Rogati — *"The AI Hierarchy of Needs"* (2017, Hackernoon)
- Cathy O'Neil — *Weapons of Math Destruction* (book, 2016) — on algorithmic bias
- MIT Technology Review — *"AI can be sexist and racist"* — on real-world bias cases

---

## Milestone Timeline in Data Science

| Year | Event |
|------|-------|
| 1960s–70s | John W. Tukey advocates data analysis as a distinct discipline |
| 1990s | C.F. Jeff Wu proposes renaming statistics to "data science" |
| 2005–2015 | Apache Hadoop revolutionises big data; "data scientist" becomes a job title |
| 2015–present | Deep learning integrates AI into mainstream data workflows |
| 2018 | Amazon scraps AI hiring tool due to gender bias |
| 2022–present | Large Language Models (ChatGPT, Claude) bring AI to non-technical users |
