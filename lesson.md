# **🏃 Class 2: Core Sprint Activities**

Instructions:  
This document contains the 20-minute hands-on exercises for Sprints 1, 2, and 3\. We will complete these sections together in class.

## **🛤️ Sprint 1: The Data Pipeline**

**Goal:** Map a real-world product to the 4 stages of data: *Collection* $\\to$ *Cleaning* $\\to$ *Analysis* $\\to$ *Visualization*.

### **🧠 Theory Recap (5 mins)**

* **Collection:** Where does the raw data come from? (Sensors, forms, logs).  
* **Cleaning:** Removing errors, duplicates, and nulls. (The "Janitor work").  
* **Analysis:** Finding patterns, aggregations, and predictions. (The "Brain").  
* **Visualization:** Presenting the insight. (Dashboards, Alerts, Charts).

### **🛠️ Hands-On Activity: "The Smart Watch Breakdown" (20 mins)**

**Scenario:** You are a Data Scientist at Fitbit/Apple/Garmin. Your goal is to show a user their "Sleep Quality Score" every morning.

**Task:** Fill in the blanks below with your group.

| Pipeline Stage | What happens here? (Specific to a Smart Watch) |
| :---- | :---- |
| **1\. Collection** | *Example: Heart rate sensor records BPM every 5 seconds...* |
| **2\. Cleaning** | *(What if the user takes the watch off? What if the battery dies mid-night?)* |
| **3\. Analysis** | *(How do we turn raw heartbeats into a "Sleep Score"? What is the math?)* |
| **4\. Visualization** | *(What does the user actually see on their phone screen?)* |

**Discussion Question:**

If the "Cleaning" stage fails (e.g., we count the time the watch was on the nightstand as "Deep Sleep"), how does that ruin the "Visualization"?

## **📄 Sprint 2: Types of Data**

**Goal:** Distinguish between Structured and Unstructured data.

### **🧠 Theory Recap (5 mins)**

* **Structured Data:** Fits in rows and columns (Excel, SQL). Highly organized, easy to search.  
* **Unstructured Data:** No predefined format (Images, Emails, Audio, Video). Hard to search, requires complex processing (AI).

### **🛠️ Hands-On Activity: "Data Binning" (20 mins)**

**Task 1:** Categorize the following data points from a Hospital System into "Structured" or "Unstructured".

1. Patient Name ("John Doe")  
2. X-Ray Image (chest\_scan\_001.jpg)  
3. Doctor's handwritten notes on a clipboard  
4. Patient Age (34)  
5. Blood Type (O+)  
6. Audio recording of a patient consultation  
7. JSON log from a heart monitor ({"bpm": 80, "time": "12:00"}) *(Tricky\! Discuss)*

Task 2 (AI Assistant):  
Open NotebookLM and ask:  
"How can I convert Unstructured text (like a doctor's note) into Structured data? Give me an example."

## **⚖️ Sprint 3: The Role of Ethics**

**Goal:** Understand how "Clean Data" can still be "Biased Data".

### **🧠 Theory Recap (5 mins)**

* **Selection Bias:** The data you collected doesn't represent the whole world.  
* **Historical Bias:** The data reflects past prejudices (e.g., hiring data from the 1970s).  
* **Garbage In, Garbage Out:** Perfect code cannot fix broken data.

### **🛠️ Hands-On Activity: "The Hiring Bot" (20 mins)**

Scenario:  
You build an AI to screen resumes for a tech company. You train it on the company's "Top Performer" data from the last 10 years.

* **The Data:** 10 years of resumes from employees promoted to Manager.  
* **The Result:** The AI starts rejecting all candidates from a nursing background and downgrades resumes containing the word "Women's College".

**Group Discussion:**

1. **Why did the AI do this?** (Was the AI sexist, or was the *data* sexist?)  
2. **Was this a "Data Collection" error or an "Analysis" error?**  
3. **How would you fix this?** (Hint: Can you simply "delete" the gender column? Why might that not be enough?)

Output:  
Write a 1-sentence "Warning Label" that should be placed on this dataset before any Data Scientist uses it.