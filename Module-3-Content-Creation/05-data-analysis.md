# Data Analysis with ChatGPT

![Bonus](https://img.shields.io/badge/section-bonus%20lesson-16a34a)

## Lesson Purpose

This bonus lesson teaches how to use ChatGPT for structured data analysis on a student dataset. It applies the same prompt engineering principles from the previous lesson: give direction, specify format, provide examples, evaluate quality, and divide labor.

By the end of this lesson you will be able to: inspect a dataset, ask better analysis questions, generate summaries, compare student groups, identify relationships between variables, create useful reports, and write prompts that produce reliable analytical output.

---

## Timing Plan

| Time | Activity | Outcome |
|---:|---|---|
| 0–5 min | Understand the dataset | You know what columns exist and what they mean |
| 5–15 min | Inspect data quality and structure | You identify ranges, categories, and possible issues |
| 15–25 min | Generate descriptive statistics | You summarize the dataset clearly |
| 25–35 min | Compare groups and find patterns | You produce useful segment analysis |
| 35–45 min | Ask for insights and recommendations | You turn numbers into decisions |
| 45–55 min | Build reusable prompts | You create analysis templates for future datasets |
| 55–60 min | Review and checklist | You verify that the analysis is complete and useful |

---

## Dataset Overview

This dataset contains student-level records with academic, demographic, and behavioral information.

### Columns

| Column | Meaning |
|---|---|
| student_id | Unique student ID |
| first_name, last_name | Student name |
| gender | Gender |
| age | Student age |
| grade_level | Grade level |
| gpa | Grade point average |
| major | Primary academic focus |
| attendance_rate | Attendance percentage |
| extracurricular_activities | Main extracurricular activity |
| scholarship_status | Scholarship category |
| math_score, science_score, english_score, history_score | Subject scores |
| graduation_year | Expected graduation year |
| enrollment_date | Date of enrollment |
| parent_education | Highest parent education |
| household_income | Household income |
| study_hours_per_week | Weekly study hours |

---

## The Goal of AI-Assisted Data Analysis

When using ChatGPT for data analysis, the goal is not just to get numbers. The goal is to get:

- clean summaries
- useful comparisons
- visible assumptions
- interpretable findings
- action-oriented insights

A weak request asks:

```text
Analyze this dataset.
```

A stronger request asks:

```text
Act as an education data analyst.

Analyze the student dataset below for a school administrator.

Focus on:
1. Academic performance patterns
2. Attendance and GPA relationships
3. Study hour effects
4. Differences by grade level, gender, major, and scholarship status
5. Any findings that could help improve student outcomes

Return:
- A short dataset overview
- A descriptive statistics table
- A group comparison table
- Five key insights
- Three recommendations

Use only the provided data.
Do not invent causal claims.
If a conclusion is uncertain, label it as a pattern rather than a fact.
```

That difference matters.

---

## Part 1: Start with Direction

Before asking for analysis, tell the model:

- who it is
- who the audience is
- what the goal is
- what limits apply

### Example Prompt

```text
Act as an educational data analyst.

Audience:
A school principal and academic support team with no advanced statistics background.

Goal:
Help them understand student performance patterns and identify where intervention may be useful.

Style:
Plain English, direct, no jargon unless explained.

Boundaries:
- Use only the provided dataset.
- Do not claim causation when the data only shows correlation.
- Do not make medical, legal, or psychological judgments.
```

> **Tip:** The audience matters. If the output is for school leaders, the analysis should be practical, not overly technical.

---

## Part 2: Specify Format Before Analysis Begins

The easiest way to get messy analysis is to ask for analysis in general paragraph form.

Instead, define the exact output format.

### Useful Analysis Formats

| Format | Best use |
|---|---|
| Table | group comparisons, rankings, statistics |
| Numbered list | insights, risks, recommendations |
| Checklist | data quality review |
| JSON | technical pipelines or tool integration |
| Executive summary | short decision-ready reporting |
| Slide outline | presentations for stakeholders |

### Example Format Prompt

```text
Return the analysis in this structure:

1. Dataset overview
2. Data quality check
3. Descriptive statistics
4. Group comparisons
5. Relationships between variables
6. Key insights
7. Recommendations

Use tables wherever comparison is helpful.
Keep the executive summary under 200 words.
```

---

## Part 3: Divide the Analysis into Steps

Do not ask for everything at once. Use a staircase workflow.

### Step-by-Step Analysis Workflow

| Step | Purpose | Output |
|---|---|---|
| 1 | Inspect structure | Column summary |
| 2 | Check data quality | Error/risk table |
| 3 | Summarize numerics | Descriptive stats |
| 4 | Summarize categories | Counts by group |
| 5 | Compare performance | Group analysis |
| 6 | Explore relationships | Pattern findings |
| 7 | Produce insights | Ranked insights |
| 8 | Recommend actions | Decision table |

---

## Part 4: Step 1 – Understand the Dataset Structure

### Prompt

```text
Act as a data analyst.

Review this student dataset and first do only Step 1.

Step 1 task:
Summarize the structure of the dataset.

Return a table with:
Column name | Data type | Meaning | Likely analytical use

Then return:
- Total number of rows
- Total number of columns
- Which fields are numeric
- Which fields are categorical
- Which fields are identifiers and should not be used as predictors
```

### What This Step Achieves
It prevents the model from treating names or IDs as meaningful variables and creates a clean map of the dataset.

---

## Part 5: Step 2 – Check Data Quality

Before doing analysis, check whether the data appears usable.

### Prompt

```text
Act as a data quality reviewer.

Review the dataset and identify:
- Missing values
- Duplicate student IDs
- Numeric values outside plausible ranges
- Category inconsistencies
- Fields that may need cleaning before analysis

Return a table with:
Issue | Column | Example or count | Severity | Recommended action

Then state whether the dataset is:
- ready for analysis
- mostly ready with minor cautions
- not ready without cleaning
```

### Likely Findings for This Dataset
Based on the provided rows, the dataset appears:

- complete
- structurally consistent
- well-formed
- free of obvious missing values
- numerically plausible

That means it is likely **mostly ready or fully ready for analysis**.

---

## Part 6: Descriptive Analysis

This is where you summarize the dataset before looking for deeper relationships.

### Prompt for Descriptive Statistics

```text
Act as an educational data analyst.

Using the student dataset, calculate descriptive statistics for these numeric fields:
- age
- grade_level
- gpa
- attendance_rate
- math_score
- science_score
- english_score
- history_score
- household_income
- study_hours_per_week

Return a table with:
Variable | Minimum | Maximum | Mean | Median | Notable pattern

Then provide:
- average GPA
- average attendance rate
- average study hours per week
- highest and lowest subject average
```

---

### Likely High-Level Patterns in This Dataset

From inspection of the values, several patterns are immediately visible:

- GPA values range roughly from $3.10$ to $3.95$
- Attendance ranges roughly from $75$ to $98$
- Study hours range roughly from $5$ to $22$
- Math students tend to have the highest GPA and study hours
- Undecided and some Arts/History students trend lower on GPA, attendance, and study time
- Science scores are generally strong across Science and Math majors
- History majors tend to score relatively higher in history than in math/science
- Scholarship status appears aligned with stronger academic performance

---

## Part 7: Group Comparisons

This is often where the most useful insights appear.

### Compare by Major

#### Prompt

```text
Act as an educational data analyst.

Compare students by major:
- Science
- Math
- Arts
- History
- Undecided

Return a table with:
Major | Student count | Average GPA | Average attendance | Average study hours | Highest average subject score | Main observation

Then rank the majors from strongest to weakest overall academic profile based only on the provided data.
Explain the ranking briefly.
```

#### Likely Insight
A likely ranking is:

1. Math
2. Science
3. Arts
4. History
5. Undecided

Because Math and Science students consistently show:

- higher GPA
- higher attendance
- higher study hours
- stronger academic subject scores

---

### Compare by Scholarship Status

#### Prompt

```text
Compare students by scholarship status: Full, Partial, None.

Return a table with:
Scholarship status | Count | Average GPA | Average attendance | Average study hours | Average subject score | Pattern

Then answer:
What differences appear between scholarship groups?
Do the differences look large, moderate, or small?
```

#### Likely Insight
Students with **Full** scholarships appear to have the strongest academic profile, followed by **Partial**, then **None**.

This likely shows a strong association between scholarship status and:

- GPA
- attendance
- study hours
- subject performance

---

### Compare by Grade Level

#### Prompt

```text
Compare grade levels 10, 11, and 12.

Return a table with:
Grade level | Count | Average GPA | Average attendance | Average study hours | Average math | Average science | Average english | Average history

Then summarize:
- Which grade has the strongest academic profile
- Which grade appears most at risk
- Any notable differences in study habits
```

#### Likely Insight
Grade $12$ students appear mixed:
- top performers are very strong
- some History students pull averages down

Grade $10$ undecided students appear weaker on several metrics.

---

### Compare by Gender

#### Prompt

```text
Compare the dataset by gender.

Return a table with:
Gender | Count | Average GPA | Average attendance | Average study hours | Average subject score | Main pattern

Then answer:
Are there visible differences in performance or engagement?
Keep the answer descriptive only.
Do not overgeneralize.
```

#### Likely Insight
Female students in this dataset appear, on average, to have slightly higher GPA, attendance, and study hours than male students.

That is a dataset-specific pattern, not a universal conclusion.

---

## Part 8: Relationship Analysis

Now move from group comparisons to relationships between variables.

### Prompt: Correlation-Oriented Analysis

```text
Act as an educational data analyst.

Analyze likely relationships between:
- study_hours_per_week and gpa
- attendance_rate and gpa
- household_income and gpa
- parent_education and gpa
- scholarship_status and academic performance

Return a table with:
Variable pair | Apparent relationship (positive/negative/weak/mixed) | Evidence from dataset | Confidence level

Then write:
- the three strongest apparent relationships
- one relationship that may be weaker than it first appears
- one caution about interpreting the results
```

---

### Likely Relationship Findings

#### 1. Study Hours and GPA
Likely a **positive relationship**:
- students studying around $18$ to $22$ hours often have GPA near $3.85$ to $3.95$
- students studying around $5$ to $8$ hours often have GPA near $3.10$ to $3.38$

#### 2. Attendance and GPA
Likely a **strong positive relationship**:
- higher attendance often appears with higher GPA
- lower attendance often appears with lower GPA

#### 3. Scholarship Status and Performance
Likely a **clear positive association**:
- Full scholarship students are among the strongest performers
- None scholarship students trend lower

#### 4. Parent Education and Household Income
These may show a **moderate positive association** with stronger performance, but less directly than attendance or study hours.

#### 5. Major and Subject Alignment
There is a strong structural pattern:
- Math majors score high in math
- Science majors score high in science
- History majors score high in history
- Arts students are relatively stronger in English/history than in STEM

---

## Part 9: Ask for Insights, Not Just Summaries

A common mistake is stopping after tables. Good analysis requires interpretation.

### Prompt for Insight Generation

```text
Based only on the analysis so far, identify the five most useful insights for a school leadership team.

For each insight, return:
Insight | Why it matters | Evidence from the dataset | Suggested action

Constraints:
- Do not repeat the same idea in different words.
- Do not claim causation.
- Make each suggested action specific.
```

---

### Example Insight Types

| Insight | Why it matters |
|---|---|
| Attendance strongly aligns with GPA | attendance support may improve outcomes |
| Study hours track with stronger performance | study habit interventions may help lower-performing groups |
| Undecided students cluster near weaker outcomes | they may need advising and structure |
| Scholarship groups differ clearly | financial support may align with engagement and achievement |
| Subject strengths track major selection | advising can use interest-performance alignment |

---

## Part 10: Turn Findings into Recommendations

Good analysis ends with decisions.

### Prompt for Recommendations

```text
Act as a school improvement advisor.

Using the findings from the dataset analysis, recommend five actions for a school support team.

Return a table with:
Recommendation | Target group | Reason | Expected benefit | Priority (high/medium/low)

Rules:
- Recommendations must connect directly to the data.
- Focus on realistic school actions.
- Do not assume budget for large new programs.
```

---

### Sample Recommendation Directions

Possible recommendations may include:

1. attendance intervention for low-attendance students
2. study-skills coaching for low-study-hour students
3. advising support for Undecided students
4. targeted academic support for lower-performing non-scholarship groups
5. enrichment or retention support for high performers

---

## Part 11: Use Prompt Variations the Right Way

As in the prompt engineering lesson, use zero-shot, one-shot, few-shot, and step-by-step prompting appropriately.

---

### Zero-Shot Example

```text
Analyze the student dataset and identify the top five academic performance patterns.

Return:
- one summary paragraph
- one comparison table
- five bullet insights
```

**Best for:** quick exploration

---

### One-Shot Example

```text
Analyze the student dataset and write insights in the style below.

Example:
Insight: Students with higher attendance generally show stronger GPA outcomes.
Why it matters: Attendance is actionable and trackable.
Evidence: Students above 90 attendance often have GPA above 3.7.
Action: Review students below 85 attendance for intervention.

Now analyze the dataset and return five insights in exactly that format.
```

**Best for:** enforcing a preferred insight format

---

### Few-Shot Example

```text
Analyze the student dataset and return findings in the style of these examples.

Example 1:
Pattern: Higher study hours are associated with higher GPA.
Evidence: Students studying 18 to 22 hours often have GPA near 3.9.
Interpretation: Study time appears linked to stronger academic outcomes.

Example 2:
Pattern: Scholarship status aligns with stronger performance.
Evidence: Full scholarship students show consistently high GPA and attendance.
Interpretation: Scholarship recipients appear academically stronger in this dataset.

Example 3:
Pattern: Undecided students trend lower in attendance and GPA.
Evidence: Several undecided students cluster around lower performance indicators.
Interpretation: This group may need additional academic direction.

Now produce five more findings in the same format.
```

**Best for:** consistency across repeated outputs

---

### Step-by-Step Example

```text
Act as an educational data analyst.

Work through this task in steps.

Step 1:
Summarize the dataset structure.

Step 2:
Check for any data quality issues.

Step 3:
Calculate descriptive statistics for GPA, attendance, study hours, and subject scores.

Step 4:
Compare major, scholarship status, grade level, and gender.

Step 5:
Identify the strongest relationships between variables.

Step 6:
Return five insights and five recommendations.

Before the final answer, state:
- your key assumptions
- any limitations in the dataset
- one caution about overinterpretation
```

**Best for:** reliable, auditable analysis

---

## Part 12: Full Master Prompt for This Dataset

Here is a complete prompt that applies all five principles.

```text
Role:
Act as an educational data analyst.

Audience:
A school principal and student support team with limited statistics background.

Goal:
Help them understand student performance, engagement, and support needs using the dataset below.

Task:
Analyze the student dataset and identify patterns related to academic performance, attendance, study habits, scholarship status, major, grade level, and background variables.

Dataset:
[paste dataset]

Format:
Return your answer in this order:

1. Dataset overview
2. Data quality check
3. Descriptive statistics table
4. Group comparison tables for:
   - major
   - scholarship status
   - grade level
   - gender
5. Relationship analysis table
6. Five key insights
7. Five recommendations
8. One short executive summary under 200 words

Constraints:
- Use only the provided data.
- Do not invent missing values or external facts.
- Do not claim causation unless the data directly supports it.
- Label uncertain findings as patterns, not facts.
- Keep language plain and practical.

Quality criteria:
A strong response gives school leaders clear, evidence-based, decision-ready insights they can act on responsibly.

Step-by-step check:
Before the final answer, briefly state:
1. Your assumptions
2. Any limitations of the dataset
3. One risk in overinterpreting the results
```

---

## Part 13: Example Insights from This Dataset

Below are realistic, dataset-grounded insights based on the records you provided.

### Insight 1: Higher study hours align with stronger GPA
Students with study hours in the high teens or low twenties frequently have GPA above $3.80$, while students studying around $5$ to $8$ hours often have GPA closer to $3.10$ to $3.38$.

### Insight 2: Attendance appears strongly linked to academic success
Students with attendance in the mid-$90$s also tend to show stronger GPA and test scores, while students with attendance in the high $70$s or low $80$s tend to perform worse academically.

### Insight 3: Math and Science majors are the strongest academic groups
These students generally show:
- higher GPA
- higher attendance
- higher study hours
- strong subject-specific performance

### Insight 4: Undecided students appear most academically vulnerable
Undecided students repeatedly appear with:
- lower GPA
- lower attendance
- fewer study hours
- weaker subject scores

### Insight 5: Scholarship status is associated with stronger outcomes
Full scholarship students are consistently among the highest performers, with strong attendance and study habits.

### Insight 6: Subject performance aligns closely with major
This is visible across the dataset:
- Math majors perform strongly in math
- Science majors in science
- History majors in history
- Arts students often do relatively better in English and history than in STEM subjects

### Insight 7: Parent education and income may matter, but less clearly than study behavior
Higher parent education and income often appear alongside stronger student outcomes, but the relationship looks less direct than attendance and study hours.

---

## Part 14: Recommended Analytical Angles You Can Ask ChatGPT to Explore

Use these as follow-up prompts.

### A. Risk identification
```text
Identify students who may be academically at risk based on a combination of low GPA, low attendance, and low study hours.

Return:
Student ID | Grade | Major | Risk factors | Suggested support priority
```

### B. High performer profile
```text
Identify the common characteristics of high-performing students with GPA above 3.85.

Return:
Pattern | Evidence | Possible interpretation
```

### C. Subject weakness analysis
```text
Find which subject appears weakest overall and which student groups struggle most in it.

Return:
Subject | Group most affected | Evidence | Recommended intervention
```

### D. Advising analysis
```text
Analyze whether certain majors or student groups may benefit from additional advising support.

Focus on:
- Undecided students
- Lower-study-hour groups
- Low-attendance students
```

### E. Scholarship equity view
```text
Compare scholarship and non-scholarship students across GPA, attendance, study hours, and household income.

Return a comparison table and three careful observations.
```

### F. Principal-ready summary
```text
Write an executive summary for a principal based on this dataset.

Requirements:
- under 180 words
- plain English
- decision-focused
- include 3 key findings and 2 immediate actions
```

---

## Part 15: Using ChatGPT to Create Visual Analysis Plans

Even if ChatGPT does not draw the charts directly in your workflow, it can specify them.

### Prompt

```text
Based on the student dataset, recommend the 10 best charts to visualize the most important patterns.

Return a table with:
Chart type | Variables | What it shows | Why it matters | Audience
```

### Likely Useful Charts

| Chart type | Variables | What it shows |
|---|---|---|
| Scatter plot | study_hours_per_week vs gpa | relationship between effort and outcomes |
| Scatter plot | attendance_rate vs gpa | attendance-performance relationship |
| Bar chart | major vs average GPA | comparison by major |
| Bar chart | scholarship status vs average GPA | scholarship differences |
| Box plot | grade_level vs GPA | distribution by grade |
| Heatmap | subject scores | subject strength patterns |
| Grouped bar chart | gender vs average subject score | descriptive comparison |
| Histogram | attendance_rate | attendance distribution |
| Histogram | study_hours_per_week | study habit distribution |
| Stacked bar | major by scholarship status | group composition |

---

## Part 16: Evaluation Prompts for Analysis Quality

Do not just generate analysis. Evaluate it.

### Self-Evaluation Prompt

```text
Review your previous analysis and score it from 1 to 5 on these criteria:

1. Accuracy
2. Clarity
3. Evidence use
4. Practical usefulness
5. Risk control

Return a table with:
Criterion | Score | Reason | Improvement

Then rewrite the weakest section.
```

### Human Review Criteria

| Criterion | Weak analysis | Strong analysis |
|---|---|---|
| Accuracy | makes unsupported claims | stays inside the dataset |
| Clarity | too technical or vague | easy to understand |
| Evidence | opinions without support | cites visible patterns |
| Usefulness | only describes | recommends action |
| Risk control | overclaims causation | marks limitations clearly |

---

## Part 17: Practice Exercises

### Practice 1
Rewrite this weak prompt:

```text
Tell me about this student dataset.
```

using:
- role
- audience
- goal
- format
- constraints
- quality criteria

---

### Practice 2
Write a prompt that asks ChatGPT to identify:
- top-performing students
- at-risk students
- the strongest predictive-looking variables

without making causal claims.

---

### Practice 3
Write:
1. a zero-shot prompt
2. a one-shot prompt
3. a few-shot prompt
4. a step-by-step prompt

for comparing scholarship groups.

---

### Practice 4
Create a prompt that asks for a principal-ready report and another that asks for a counselor-ready report. Change the audience and output style accordingly.

---

## Part 18: Review Checklist

- [ ] Did you define the role clearly?
- [ ] Did you specify the audience?
- [ ] Did you name the exact analysis task?
- [ ] Did you define the output format?
- [ ] Did you constrain the model to the provided data?
- [ ] Did you avoid causal overclaiming?
- [ ] Did you divide the work into steps?
- [ ] Did you ask for insights, not just summaries?
- [ ] Did you ask for recommendations tied to evidence?
- [ ] Did you evaluate the final output for quality?

---

## Summary: Dataset-Based Insights

Based on the records you shared, the strongest broad patterns appear to be:

- higher attendance is associated with higher GPA
- higher study hours are associated with higher GPA
- Math and Science majors appear strongest overall
- Undecided students appear most at risk
- Full scholarship students show the strongest academic profile
- subject scores align strongly with declared major
- background variables may matter, but study behavior and attendance appear more directly tied to outcomes
