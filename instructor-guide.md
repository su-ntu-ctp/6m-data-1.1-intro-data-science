# 🎓 Instructor Guide — Lesson 1.1: The Data Landscape

> **Branch:** `feature/instructor-guide`
> **Audience:** Instructors and teaching assistants
> **Companion to:** `lesson.md`, `pre-class.md`, `assignment.md`

---

## 1. Lesson Overview & Instructor Objectives

| | |
|---|---|
| **Duration** | 3 hours |
| **Format** | Flipped Classroom + Discussion |
| **Learner entry point** | No technical background; may have used Excel or basic BI tools |

By the end of this lesson learners should be able to:

1. Classify a business scenario as Data Analytics, Data Science, or AI — and justify the classification.
2. Map a real-world problem to the 4 stages of a data pipeline.
3. Distinguish Structured, Unstructured, and Semi-Structured data with examples from their own industry.
4. Identify at least two types of data bias and explain why clean data ≠ unbiased data.

**Instructor's primary job this lesson** is not to teach definitions — those were in the pre-class reading. Your job is to surface misconceptions, provoke discussion with good questions, and make the abstract tangible through the activities.

---

## 2. Concept Analogies

Use these when learners look confused or when you want to check understanding quickly. Each analogy is paired with a common misconception it addresses.

### Analytics → Data Science → AI

**The Kitchen Analogy** *(already in lesson.md — deepen it here)*

| Tier | Kitchen Action | Key Point |
|------|---------------|-----------|
| Analytics | Check the fridge, write down what's missing | Backward-looking; answers "what happened?" |
| Data Science | Plan next week's meals from the fridge history | Forward-looking; a human still decides |
| AI | A robot chef that reorders groceries automatically | Autonomous action; no human per-decision |

**Extending the analogy if learners ask "but GPT does everything — isn't it all AI?":**
Point out that GPT was *built* by a massive Data Science effort. The model is the robot chef. The training pipeline — cleaning trillions of tokens, evaluating quality, handling biases — that was the Data Science work. Most companies are still at the "check the fridge" stage; very few have a working robot chef yet.

**The Netflix Extension** *(great for engagement)*
Ask: "How does Netflix use all three in the same product?" Let learners answer first, then confirm:
- Analytics: "Which shows have the highest completion rate?" → Report.
- Data Science: "Which show will *this* user want to watch next?" → Recommendation model.
- AI: "Which thumbnail image should we show *this* user for the same show?" → Fully autonomous personalization.

---

### Data Structures

**The Hospital Filing Room Analogy**

| Type | Analogy | Why It Clicks |
|------|---------|--------------|
| Structured | A standard patient intake form — every box is labelled, every box expects a specific format | Easy to search, sort, query |
| Unstructured | A surgeon's voice memo recorded during rounds | Rich in meaning, but no machine-readable schema |
| Semi-Structured | A WhatsApp message with some fields (timestamp, sender) but free-form content | Partially organised — some structure, no rigid schema |

**The "Tricky" JSON question:** Learners almost always say JSON is structured because it *looks* organised. Use the counter-example: ask two learners to both write JSON for a product listing. They'll use different key names (`product_name` vs `name`), different nesting, different types for price (string vs number). That's the semi-structured problem — no *enforced* schema.

---

### Data Pipeline

**The Water Treatment Analogy**

| Stage | Water Treatment | Data Equivalent |
|-------|----------------|-----------------|
| Collection | Rain into reservoir | Sensors, forms, transactions |
| Cleaning | Filtration & treatment | Remove nulls, fix types, handle outliers |
| Analysis | Testing water quality | Statistical analysis, modelling |
| Visualisation | Reading the report | Dashboard, chart, executive summary |

Ask: "What happens if a filter in stage 2 breaks?" → All downstream outputs (the "clean" reports) are built on dirty data. Garbage In, Garbage Out.

---

### Ethics & Bias

**The Inheritance Analogy**

> "Imagine a company hired mostly men in the 1970s–2000s, promoted them, and now has 10 years of 'top performer' data. That data didn't walk in saying 'I'm biased.' It looks perfectly formatted. But it *inherited* the hiring practices of a different era."

Follow with: "The AI isn't sexist — the *historical record* is. The AI is just a very accurate mirror of that record."

**The Map Analogy for Selection Bias:**
Old maps of the world made Europe appear larger than Africa (Mercator projection). The map wasn't *wrong* about Europe — it was just drawn from a European perspective. Similarly, a training dataset isn't wrong — it just reflects who collected it and who they thought to include.

---

## 3. Real-World Use Cases

Use these during discussions or to ground abstract concepts in learners' own industries.

### Analytics vs. Data Science vs. AI — Industry Parallels

| Industry | Analytics Example | Data Science Example | AI Example |
|----------|-------------------|----------------------|-----------|
| Banking | Monthly fraud report | Churn prediction model | Real-time transaction blocking |
| Retail | Last quarter's top-selling SKUs | Demand forecasting for inventory | Dynamic pricing algorithm |
| Healthcare | Average length of stay per ward | Readmission risk model | Automated CT scan anomaly detection |
| HR | Headcount report by department | Attrition prediction | CV screening bot |

Prompt: "Which tier is your current organisation at? What would it take to move to the next level?"

### Why the Pipeline Matters — The Production Cost of Bad Cleaning

Share the real stat: IBM estimates that bad data costs the US economy ~$3.1 trillion per year. The reason is almost always Stage 2 failure — the cleaning step was skipped, rushed, or nobody owned it. The "80% cleaning" figure isn't a complaint — it's a feature of professional data work.

### Ethics in the Wild

- **Amazon's scrapped hiring AI (2018):** Trained on 10 years of internal promotion data → systematically downgraded women's CVs. The system was retired. This is the *exact* scenario in Activity 3 ("The Hiring Bot").
- **COMPAS recidivism algorithm (USA):** Used to predict re-offending risk in criminal sentencing. Found to be biased against Black defendants. The data reflected historic sentencing patterns, not objective risk.
- **Facial recognition in policing:** Systems trained primarily on lighter-skinned faces have higher error rates on darker-skinned faces — directly caused by Selection Bias in the training set.

---

## 4. Activity Facilitation Notes

### Part 1: The Company Diagnostic (40 min)

**What to watch for:**
- Learners often misclassify the "bank fraud flagging" scenario as Data Science (because it involves a model). The key distinguisher is *automation* — if a human reviews each flag, it's Data Science. If the system *acts* autonomously (blocks the transaction), it's AI. Push them on this distinction.
- Some learners want to say "it depends" for everything. That's fine — but ask them *what it depends on*. The action/automation criterion usually resolves it.

**Discussion prompt to spark engagement:**
> "If a CEO says 'I want to build a GPT-4 for my company' but all their data is in paper files — what would you say to them?"

Expected direction: They're trying to skip levels 1–2 of the pyramid. You need Collection and Cleaning before you can do Science, let alone AI.

**The Python Peek:**
Don't spend more than 5 minutes on the code. The point is to show learners that "prediction" is really just a formula applied to data — not magic. If learners are intimidated by the code, remind them they don't need to understand every line today; they just need to see the difference between printing a table (Analytics) and computing a forecast (Data Science).

**Time management:** 40 min can run long if discussion is lively. Use the reflection questions to land the conversation rather than opening new threads.

---

### Part 2: The Smart Watch Pipeline (20 min)

**Setup (1 min):** Tell learners to write their own Stage 2–4 answers *before* opening the details block. The exercise value is in the attempt, not just reading the answer.

**Common mistakes learners make:**

| Stage | Common Mistake | Correction |
|-------|---------------|-----------|
| Cleaning | "We'd throw away data where the watch was removed" | Ask: "Is 'watch removed' a data quality issue or a valid data point?" (It's valid — it tells you the user took a shower, went to gym without watch, etc.) |
| Analysis | "We'd calculate average heart rate" | Push further: "How do you get from BPM to a *Sleep Score*? What's the formula?" Forces them to think about the model |
| Visualisation | "Show a chart" | Ask: "What does a *user* want to see — a raw BPM graph, or something actionable?" |

**The "Garbage In" question** is the most important one in this activity. Use it to preview the ethics section: even a beautiful app UI can mislead if the cleaning step is wrong.

---

### Part 3: Data Binning (20 min)

**The JSON trap** is the most useful teaching moment here. Most learners will classify it as "Structured" on first pass. Steps to guide them:

1. Ask a learner to read the JSON out loud: `{"bpm": 80, "time": "12:00"}`.
2. Ask: "Is `bpm` always the key name in every heart monitor?" (No — different manufacturers use different field names.)
3. Ask: "Can JSON have nested objects, arrays, missing fields?" (Yes.)
4. Reveal: "That's why JSON is Semi-Structured. It has *some* organisation, but no *enforced* schema."

**Pair this with the conversion question:** NLP techniques like Named Entity Recognition can extract medication names and symptoms from free-text doctor's notes and populate structured columns. This is called *information extraction* and is a real production use case at hospitals.

---

### Part 4: The Hiring Bot Post-Mortem (40 min)

**This is the most emotionally engaged activity.** Some learners may have personal experiences with bias — create a respectful tone before starting.

**Facilitation flow:**
1. Read the scenario aloud together (3 min).
2. Individual reflection (5 min) — write answers before discussing.
3. Pair discussion (10 min).
4. Full group debrief (15 min).
5. Warning label writing (5 min).
6. Share 2–3 warning labels with the group (5 min).

**Expected learner answers and where to push:**

| Question | Likely First Answer | Push Toward |
|----------|-------------------|------------|
| "Was the AI sexist?" | "Yes, the AI was biased" | "The AI was accurate — it accurately reflected biased historical data. The *data* is the problem." |
| "Was this a Collection or Analysis error?" | "Analysis" | "Both — the data collection excluded certain candidates (Selection Bias), AND the analysis didn't audit for demographic fairness." |
| "Can you just delete the gender column?" | "Yes, that fixes it" | "Proxy variables: job titles, university names, hobbies can all encode gender even without the column. Simply deleting one field rarely solves structural bias." |

**What makes a good Warning Label:**
A good label names four things: (1) the time period, (2) the source/context, (3) the specific bias risk, (4) the required action before use.

**If learners ask "what's the solution?":**
Point them toward demographic auditing (checking model performance across subgroups), re-sampling training data to balance representation, and the emerging field of Responsible AI / Model Cards.

---

## 5. Timing & Pacing Notes

| Part | Planned | Common Overrun | Mitigation |
|------|---------|---------------|-----------|
| Part 1: The Hierarchy | 60 min | Runs long if Python Peek generates questions | Keep code demo to 5 min max; park deep Python questions for 1.6 |
| Part 2: The Pipeline | 60 min | Activity 1 runs long if groups get into detailed cleaning debates | Cap Stage 2–4 group work at 10 min, then debrief together |
| Part 3: Ethics | 60 min | Hiring Bot discussion can run 60+ min on its own | Hard stop at 40 min; any unfinished debate becomes an assignment prompt |

---

## 6. Common Learner Questions (and How to Handle Them)

**Q: "If AI is so powerful, why does the hierarchy matter?"**
A: Because AI is only as good as the data it's trained on. The hierarchy is the *dependency chain*. Skipping levels doesn't make them go away — it makes them invisible and dangerous.

**Q: "Can we use AI to clean data automatically?"**
A: Yes — and this is an active area (e.g., LLM-assisted data labelling). But the AI doing the cleaning was also trained on data, which needs *its* own cleaning. At some point, a human has to define what "correct" looks like.

**Q: "Is everything AI now?"**
A: Marketing says yes; engineers say no. The word is overloaded. In this course we use the precise hierarchy: if a human still makes the final decision, it's Data Science. If the system acts autonomously, it's AI.

**Q: "What programming language do I need for this?"**
A: We'll learn Python from Lesson 1.6 onwards. Today's lesson is about thinking, not coding. The one code demo in Part 1 is just for exposure.
