# AI-Impact_on_Student_Academic_Outcome

This project shows how students are influenced and affected by AI usage.

<img width="845" height="422" alt="AI STudent impact Dashboard" src="https://github.com/user-attachments/assets/cf25fc6d-2366-491b-860f-7377953de5fa" />

**Prepared by:**

Idowu Emmanuel

**Tool Used:**

Microsoft Excel

**Dashboard Title:**

Ai Impact on Student Academic outcomes

**Industry:**

Education

**Table of Contents**

●	Introduction

●	Story of Data

●	Data Splitting and Preprocessing

●	Pre-Analysis

●	In-Analysis

●	Post-Analysis and Insights

●	Data Visualizations & Charts

●	Recommendations and Observations

●	Conclusion

●	References & Appendices

**Objective of the Project**

The primary objective of this analysis is to evaluate the impact of Artificial Intelligence (AI) tools on student academic outcomes across five major categories, five-year levels of study, and multiple AI engagement dimensions. Specifically, the analysis aims to determine whether and how AI usage measured through weekly hours, prompt engineering skill, primary use case, tool diversity, and perceived dependency influences Post-Semester GPA, Skill Retention Score, and Burnout Risk Level. The ultimate goal is to produce data-driven insights and recommendations that institutions, educators, and students can act on to optimize AI engagement for better academic performance.

**Problem Being Addressed**

The rapid proliferation of Generative AI tools in academic settings has created a fundamental question that educators and institutions are struggling to answer: is AI helping or hurting students academically? The absence of structured, large-scale empirical data on this question has left institutional AI policies inconsistent ranging from Strict Ban to Actively Encouraged without clear evidence to justify either position. This analysis seeks to address the following core questions:

●	Which student groups benefit most from AI usage in terms of GPA improvement?

●	Does the amount of AI usage matter, or is it more about how AI is used?

●	What is the relationship between AI dependency and student burnout risk?

●	Does prompt engineering skill level influence academic outcomes?

●	Which primary use case of AI produces the best skill retention?

●	How does institutional AI policy affect student performance outcomes?

**Key Datasets and Methodologies:**

The analysis is based on a single primary dataset of 50,000 student records sourced from Kaggle. The following analytical methods were employed in Microsoft Excel:

●	Pivot Tables — for aggregating GPA change, skill retention, and tool diversity by major, year of study, use case, and prompt engineering skill level

●	Calculated Columns — GPA_Change (Post GPA minus Pre GPA) and AI_Usage_Bracket (Low/Moderate/High) derived using Excel formulas

●	IF Formula Classification — Perceived_AI_Dependency categorized into Low (1–3), Moderate (4–6), and High (7–10) using nested IF statements

●	Conditional Formatting — applied to identify performance tiers and outliers across key metrics

●	Data Slicers — for interactive filtering by Year of Study and Burnout Risk Level across the full dashboard

●	Charts and Visualizations — bar charts, pie charts, treemaps, and donut charts communicating key analytical findings

●	Dashboard Design — consolidating all KPI cards and charts into a single interactive analytical view

**Data Source**

The dataset was sourced from Kaggle.

**Data Collection Process**

The data was provided in a pre-compiled Microsoft Excel workbook.

**Data Structure**

The dataset contains 50,000 student records and 16 columns. Each row represents a unique student. The original dataset was supplemented with two calculated columns during preprocessing — GPA_Change and AI_Usage_Bracket — bringing the working dataset to 18 columns.

<img width="383" height="218" alt="Screenshot 2026-09-29 214112" src="https://github.com/user-attachments/assets/b5d0c87e-6f20-44d6-bf94-6c1c7495ad8e" />

**Important Features and Their Significance**

●	GPA_Change — the primary calculated dependent variable; a positive value indicates AI usage contributed to academic improvement while a negative value signals a decline

●	Skill_Retention_Score — a critical secondary outcome that distinguishes genuine learning from superficial task completion aided by AI

●	Burnout_Risk_Level — a psychological outcome variable that reveals whether AI usage is reducing or increasing student stress and cognitive load

●	Weekly_GenAI_Hours — the core exposure variable; enables testing of whether more AI usage produces better or worse outcomes

●	Prompt_Engineering_Skill — a quality-of-use variable; tests whether how well a student uses AI matters more than how much they use it

●	Primary_Use_Case — reveals which applications of AI are most and least associated with academic benefit

●	Institutional_Policy — a structural variable that captures the institutional environment within which AI usage occurs

**Data Limitations or Biases**

●	Self-reported data: All AI usage metrics (Weekly_GenAI_Hours, Perceived_AI_Dependency, Prompt_Engineering_Skill) are self-reported and subject to social desirability bias — students may over- or under-report usage depending on their institution's policy

●	Single-semester scope: The dataset captures one semester's performance, limiting the ability to assess long-term cumulative effects of AI usage on academic outcomes

●	No institution identifiers: The absence of institution-level identifiers prevents analysis of whether specific universities' policies are more effective than others

●	No demographic data: The dataset does not include age, gender, socioeconomic status, or prior academic history — all of which could confound the relationship between AI usage and GPA change

**Data Cleaning**

The following cleaning steps were performed before analysis commenced:

●	Duplicate check: All 50,000 Student_IDs were verified for uniqueness using Excel's Remove Duplicates function — no duplicate records were identified

●	Data type verification: All numerical columns (GPA values, hours, scores) were confirmed as numeric format; all categorical columns were confirmed as text format with consistent casing

●	Category standardization: Major_Category, Year_of_Study, Primary_Use_Case, and Institutional_Policy values were verified for spelling consistency across all 50,000 rows

●	Boolean formatting: Paid_Subscription column (TRUE/FALSE) was verified and standardized for consistent pivot table aggregation

●	Range validation: Pre_Semester_GPA and Post_Semester_GPA values were checked to confirm all entries fall within the valid 0.0–4.0 GPA scale

**Data Transformations**

●	GPA_Change column: Created using the formula =Post_Semester_GPA - Pre_Semester_GPA for every student record. This calculated column serves as the primary dependent variable for all GPA impact analyses throughout the dashboard

●	AI_Usage_Bracket column: Created using the nested IF formula =IF(Weekly_GenAI_Hours<=5,"Low Usage (0-5hrs)", IF(Weekly_GenAI_Hours<=15,"Moderate Usage (6-15hrs)","High Usage (16+hrs)")) to convert the continuous Weekly_GenAI_Hours variable into three analytical categories

●	Dependency_Level classification: The Perceived_AI_Dependency scale (1–10) was categorized using an IF formula into Low (1–3), Moderate (4–6), and High (7–10) to enable meaningful group-level analysis of AI dependency patterns

●	Anxiety_Level classification: Exam anxiety scores were similarly categorized into Low, Moderate, and High bands to support slicer-based filtering on the dashboard

**Industry Context**

This dataset belongs to the education technology (EdTech) and higher education sectors — specifically addressing the intersection of Artificial Intelligence adoption and student academic performance. The analytical findings are relevant to university administrators, curriculum designers, academic policy makers, student support services, and AI tool developers seeking to understand and optimize how AI integration affects learning outcomes at scale.

**Value to the Industry**

This analysis delivers direct value to the higher education sector by providing large-scale empirical evidence on a question that has largely been debated without data — whether AI is academically beneficial, harmful, or neutral for students. The dashboard transforms 50,000 student records into a clear, actionable intelligence framework that supports evidence-based policy reform, targeted student support, and optimized AI integration strategies across diverse academic contexts.
 

**PRE-ANALYSIS**

**Key Trends Identified**

●	The average GPA across all 50,000 students increases from 3.146 (Pre-Semester) to 3.349 (Post-Semester) — a mean GPA_Change of +0.203 — suggesting that at a population level, AI usage is associated with a modest but consistent positive academic effect

●	STEM is the largest major category with 15,059 students (30.1% of the dataset), followed by Business (25.1%), Humanities (20.0%), Medical (12.9%), and Arts (11.9%) — making STEM the dominant group whose patterns will most heavily influence aggregate findings

●	The distribution of AI usage skews toward low-to-moderate hours — average Weekly_GenAI_Hours of 8.43 — suggesting most students are not heavy AI users, which will affect interpretation of high-usage findings

●	Burnout risk is predominantly Medium (42.3%) or Low (32.7%), with High burnout affecting 25.0% of the student population — a significant minority warranting targeted intervention

●	Allowed_With_Citation is the most common institutional policy (50.4%), suggesting most students operate in a permissive-but-structured AI environment

**Potential Correlations**

●	A preliminary scan of the data suggests students with Advanced Prompt Engineering Skills have higher Post_Semester_GPAs (3.389) than Beginner-level users (3.334) — a 0.055 GPA point gap that is worth investigating at the analytical level

●	Students with High AI Dependency (7–10) appear to cluster disproportionately in the High Burnout Risk category — a pattern visible even in raw data scrolling that suggests a meaningful dependency-burnout relationship

●	Debugging/Troubleshooting as a primary use case appears in many STEM records alongside higher Skill_Retention_Scores — suggesting a correlation between problem-solving AI applications and genuine knowledge retention

●	Traditional_Study_Hours average (11.21 hours/week) is higher than Weekly_GenAI_Hours average (8.43 hours/week) — suggesting students are still using traditional study as their primary mode, with AI as supplementary

**Initial Insights**

●	Junior year students appear to have the highest AI engagement in early data exploration — which the Year of Study chart will need to confirm or contradict at the aggregate level

●	The Strict_Ban policy group (9,788 students — 19.6%) is a meaningful subpopulation that will allow direct comparison of restricted vs. permissive AI environments on academic outcomes

●	With 28,846 students (57.7%) not paying for AI subscriptions, the majority of the student population is using free-tier AI tools — raising a question about whether premium access meaningfully differentiates outcomes

 **IN-ANALYSIS**

 AI Impact by Major Category
 
STEM is the highest-benefiting major at +0.2173 GPA points, followed by Medical (+0.2014), Humanities (+0.1980), Arts (+0.1969), and Business (+0.1943). The overall spread between the highest (STEM) and lowest (Business) is just 0.023 GPA points — an extremely narrow range confirming that AI delivers broadly consistent academic benefit across all disciplines. However, the dashboard note confirms that STEM benefited most, likely due to the alignment between AI debugging and troubleshooting tools and the problem-solving nature of STEM coursework.

AI Weekly Usage Impact Analysis

Analysis of AI weekly usage revealed a non-linear relationship between usage quantity and academic benefit. Moderate Usage (6–15 hours/week) produced the highest GPA change at +0.2270, followed by Low Usage (0–5 hours/week) at +0.1947, and High Usage (16+ hours/week) at the lowest at +0.1730. This finding establishes a clear optimal usage zone — 6 to 15 hours per week — and confirms that excessive AI usage actively works against academic performance rather than enhancing it. Notably, Low Usage students outperform High Usage students, reinforcing that intentionality matters more than volume.

Year of Study Analysis — AI Dependency and Tool Diversity

Analysis of normalized AI Dependency and Tool Diversity scores by Year_of_Study revealed a counterintuitive pattern. Junior year students lead both metrics at 22.09% dependency and 22.04% tool diversity — confirming the KPI card on the dashboard. Freshmen are a close second at 22.06% and 22.00% respectively — a finding that challenges the assumption that first-year students are conservative AI users. Graduate students sit significantly lower at 14.86% tool diversity and 14.95% dependency — nearly 5 percentage points below Sophomores. Sophomore students show a notable dip below Freshmen in both metrics, forming a two-tier structure with Juniors, Freshmen, and Seniors in the upper band and Sophomores and Graduates in the lower band.

Primary Use Case Analysis — Skill Retention

Analysis of average Skill_Retention_Score by Primary_Use_Case confirmed Debugging/Troubleshooting as the strongest use case at 78.07 — significantly above all others. Ideation follows at 75.52, with Copywriting/Drafting (75.23) and Summarizing_Reading (75.22) nearly identical in third and fourth place. Direct_Answer_Generation sits at the bottom at 73.72 — the weakest use case for skill retention. The gap between Debugging (78.07) and Direct_Answer_Generation (73.72) is 4.35 points — the most analytically significant spread in the chart, confirming that asking AI to solve problems builds more knowledge than asking it for direct answers.

Prompt Engineering Skill Analysis

Analysis of Post_Semester_GPA by Prompt_Engineering_Skill level revealed that Advanced users achieve the highest average Post GPA at 3.389, while Beginner (3.334) and Intermediate (3.334) users are virtually identical and both trail Advanced users by 0.055 GPA points. The near-identical performance of Beginner and Intermediate users is a significant finding — it suggests that the meaningful skill threshold is between Intermediate and Advanced, not between Beginner and Intermediate. Students who cross into Advanced-level prompt engineering see a measurable academic uplift that the intermediate level does not deliver.

Burnout Risk and AI Dependency Analysis

This analysis revealed a strong and consistent relationship. Among High Dependency students (7–10 scale), 73.3% fall in the High Burnout Risk category and only 3.4% fall in Low Burnout. Among Low Dependency students (1–3 scale), 51.8% are Low Burnout and only 17.7% are High Burnout. Moderate Dependency students sit between these extremes. This pattern confirms that AI over-reliance is not just academically suboptimal — it is a significant driver of student psychological distress.

**Analysis Techniques Used**

●	Pivot Tables — primary aggregation tool for all GPA_Change, Skill_Retention_Score, and Post_Semester_GPA analyses by major, year, use case, and skill level

●	Nested IF Formula — used to create AI_Usage_Bracket and Dependency_Level classification columns

●	Calculated Column (GPA_Change) — derived from Post_Semester_GPA minus Pre_Semester_GPA to create the core dependent variable

●	Normalized scoring — Year of Study chart uses normalized count ratios to enable fair cross-group dependency and diversity comparison

●	Slicers — Year of Study and Burnout Risk Level slicers connected to all dashboard charts for interactive filtering
 
 
 **POST-ANALYSIS AND INSIGHT**

**Key Findings**

<img width="382" height="165" alt="Screenshot 2026-09-29 214952" src="https://github.com/user-attachments/assets/b4ee31ce-35a5-44f2-b11b-4967669c5242" />


**Comparison with Initial Findings**

The majority of pre-analysis hypotheses were confirmed through formal analysis. STEM's academic leadership, the optimal moderate usage zone, the dependency-burnout relationship, and Junior year's engagement dominance were all validated. The most counter-intuitive confirmed finding was that Freshman students have nearly identical AI engagement levels to Juniors — contradicting the assumption that first-year students are cautious adopters. The most unexpected finding was the near-identical GPA change across all five major categories (range of just 0.023 points), which suggests AI's academic benefit is remarkably consistent across disciplines rather than sector-specific.

**DASHBOARD VISUALIZATION AND CHARTS**

Dashboard Overview

All charts and visualizations were consolidated into a single interactive dashboard in Microsoft Excel titled "AI Impact on Student Academic Outcomes." The dashboard includes three KPI cards (Year of Study with highest AI dependency, Major Category benefiting most from AI, and Most Impactful Weekly GenAI Usage level) connected to Year of Study and Burnout Risk Level slicers. The following charts are featured:

<img width="382" height="129" alt="Screenshot 2026-09-29 215013" src="https://github.com/user-attachments/assets/55a510b5-da7a-4d71-b22f-7da014fce277" />


**RECOMMENDATION AND OBSERVATION**

1. Establish a Moderate AI Usage Policy as the Academic Standard

The clearest and most actionable finding from this analysis is that 6–15 hours of weekly AI usage produces the highest GPA improvement (+0.227) while High Usage (16+ hours) produces the lowest (+0.173). Institutions should establish a recommended weekly AI usage range of 6–15 hours as part of their academic AI guidelines — framing AI as a tool to be used deliberately, not habitually. This recommendation applies across all major categories since the benefit pattern is consistent regardless of discipline.

3. Make Prompt Engineering Training Mandatory for All Students

Advanced prompt engineering skill is the single most reliable predictor of higher Post-Semester GPA in this dataset — producing a 0.055 GPA advantage over Beginner and Intermediate users. Given that 18,495 students (37.0%) are still at Beginner level, the largest growth opportunity in the student population lies in moving Beginners toward Advanced skill. A structured, curriculum-embedded prompt engineering training program — delivered at induction and refreshed annually — would directly address this gap.

4. Promote Debugging and Problem-Solving as the Primary AI Use Case

Debugging/Troubleshooting produces a Skill Retention Score of 78.07 — 4.35 points above the worst-performing use case (Direct_Answer_Generation at 73.72). Institutions and educators should actively discourage Direct Answer Generation as a primary AI application and promote problem-solving, ideation, and debugging use cases through assessment design, AI usage guidelines, and student awareness campaigns. This shift in how students use AI — rather than how much — will produce the greatest improvement in genuine learning outcomes.

5. Implement High Dependency Intervention Programs

73.3% of students with High AI Dependency (score 7–10) fall in the High Burnout Risk category — the strongest and most concerning relationship in the entire dataset. A dedicated student support program targeting high-dependency students should be designed and implemented, combining AI usage monitoring, traditional study hour targets, academic counseling, and study skills coaching. Early identification of high-dependency students through self-assessment tools at the start of each semester would enable proactive rather than reactive intervention.
   
6. Reform Strict Ban Policies Using Evidence

The dataset reveals that students under Strict Ban policies are still engaging with AI — yet within a more constrained and potentially less structured way that may suppress academic benefit. Institutions maintaining Strict Ban policies should review this position in light of the evidence and consider transitioning to an Allowed_With_Citation framework — which provides accountability and academic integrity safeguards without eliminating the documented academic benefits of moderate, purposeful AI usage.

7. Redirect Freshman AI Engagement Before Poor Habits Solidify

Freshmen arrive at university with AI usage habits already established — many falling in the High Usage (16+ hours) bracket from the very first semester. This early adoption intensity, without the academic maturity to use AI purposefully, creates an immediate burnout and over-dependency risk. A targeted AI orientation program for all incoming students — focused on redirecting existing usage toward the optimal 6–15 hour moderate zone and toward problem-solving use cases — should be prioritized as a first-semester academic support intervention.

8. Support Graduate Students with Purpose-Built AI Research Tools

Graduate students show the lowest AI tool diversity (14.86%) and the most conservative usage patterns of any year group. While academic rigor appropriately limits AI dependency at postgraduate level, graduate students may be missing legitimate research productivity benefits from purposeful AI integration. A curated set of AI tools specifically vetted for postgraduate research tasks — literature synthesis, citation management, data analysis support, and academic writing refinement — delivered through supervised research seminars, would support appropriate AI adoption without compromising research integrity.

**CONCLUSION**

**Key Learnings**

This analysis of 50,000 student records has produced a clear and evidence-based picture of how AI impacts academic outcomes across multiple dimensions of student life. The most important learning is that AI's academic benefit is real but conditional — it depends critically on how much AI is used (optimal: 6–15 hours/week), how skillfully it is used (Advanced prompt engineering), and what it is used for (problem-solving and debugging, not direct answer generation). The analysis also revealed that AI dependency is not a neutral behavior — it is a significant driver of student burnout that institutions must actively monitor and manage.

A secondary learning is the remarkable consistency of AI's academic benefit across disciplines. The 0.023-point GPA change range between STEM and Business suggests that the principles of effective AI usage are universal rather than discipline-specific — making it possible to design institution-wide guidance rather than requiring bespoke approaches for each major category.

**Limitations**

●	Self-reported AI usage data is subject to social desirability bias — students under Strict Ban policies may under-report actual usage
●	Single-semester scope prevents assessment of whether AI benefits compound or diminish over multiple semesters of exposure
●	Absence of demographic variables (age, gender, socioeconomic status) limits ability to control for confounding factors in the GPA change analysis
●	No institution-level identifiers prevents granular policy effectiveness comparison between specific universities
●	Skill_Retention_Score methodology is not defined in the dataset — it is unclear whether this is a standardized test score, instructor assessment, or self-reported measure

**References**

●	Dataset: AI Student Impact Dataset — sourced from Kaggle (https://www.kaggle.com). 50,000 student records covering AI usage behavior and academic outcome metrics.

●	Tool: Microsoft Excel — used for all data cleaning, calculated column creation, pivot table analysis, chart generation, and interactive dashboard design

●	Framework: Technical Report Template for Analytical Projects — Vephla University curriculum document

**Appendix A — Dataset Column Reference**

<img width="383" height="221" alt="Screenshot 2026-09-29 215039" src="https://github.com/user-attachments/assets/d901a60c-bca6-483b-a536-f06f61781596" />


**Appendix B — Summary Statistics**

<img width="385" height="171" alt="Screenshot 2026-09-29 215059" src="https://github.com/user-attachments/assets/8ead8da3-d92d-43fc-8599-094c3c43256a" />


**Appendix C — Major Category Distribution**

<img width="383" height="72" alt="Screenshot 2026-09-29 215121" src="https://github.com/user-attachments/assets/a378031b-04f8-40dc-9c66-08adc376dd55" />

Arts	5,933	11.9%	+0.197
