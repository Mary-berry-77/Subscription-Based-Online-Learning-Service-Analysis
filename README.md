# 📘 Day 1 Revisit Drives Long-Term Retention  
**Early Behaviour Analysis in a Subscription-Based Learning Platform**

## 🧭 TL;DR — Project Summary at a Glance

### 🎯 Issue Found  
1-month retention dropped steadily despite growing new sign-ups.

### 🔍 Root Cause  
Early drop-off concentrated within 1–2 days after lesson start.  
**Day 1 revisit** emerged as the key engagement inflection point.

### 🧩 Analysis Design  
- Compared **0-day drop-offs** with **Day 1 returners** based on their behavioural patterns during the **initial lesson experience (Activation)**:  
  - Lesson completion count  
  - Clicks on lesson Q&A or content reviews  
  - Time taken to complete a lesson  
  - Drop-off timing during lesson   

### 💡 Key Insight  
Day 1 returners showed the strongest engagement:
- 43.5% of returners revisited on Day 1
- Higher exploration, interaction, and lesson completions over time

### 🛠️ Strategic Recommendation  
#### 1. Reduce early exits after first lesson entry
- Optimise lesson length for quick completion
- Place interactive elements (Q&A, reviews) earlier to encourage bonding

#### 2. Drive lesson completion and immersion
- Break long lessons into short, completable units
- Highlight progress milestones to reinforce achievement

#### 3. Encourage Day 1 revisit
- Use follow-up nudges (notifications, emails) within 24 hours
- Remind users of unfinished lessons or recommended content


### 📈 Expected Impact  
- Goal: Raise Day 0 "8+ lesson completers" from 38% → 50%
- Impact: +1.2%p increase in Day 1 revisit rate (from 15.9% → 17.1%)
  -  Estimated +951 more early returners — purely from content restructuring, no extra cost


---

## 🔍 Background & Objective

Despite steady growth in new user sign-ups, 1-month retention rates have been falling.  
The platform offers video-based lessons and a 7-day free trial before conversion.  
Our goal was to understand **when and why users drop out early**, and what behaviours are linked to long-term retention.

---

## 🔬 Data & Methodology

- **Dataset**: 13 raw user log tables (lesson views, clicks, trial start, lesson completions, etc.)
- **Scope**: 98,452 users who signed up after November 2022 (Korea only)
- **Tools**: Python (Pandas, Seaborn), AARRR funnel, cohort analysis, statistical tests

### AARRR Funnel Summary


| Stage       | Criteria                                      | Users    | Conversion Rate |
|-------------|-----------------------------------------------|----------|-----------------|
| Acquisition | New sign-ups (Nov 2022 – Nov 2023)            | 98,452   | -               |
| Activation  | Started at least one lesson                   | 62,339   | 63.3%           |
| Retention   | Returned at least once after first lesson     | 9,925    | 15.9%           |
> ℹ️ *Revenue* stage was excluded due to missing payment logs for approx. **40% of actual paying users**, making conversion inference unreliable.


---

## 🔎 Insight 1: Sign-up volume ↑, Retention ↓

Despite higher sign-up volume, 1-month retention has continued to decline.  
Most cohorts lose more than half of users in the first week.
![코호트별0일차유입수 1개월차리텐션율+추세선](https://github.com/user-attachments/assets/e19e1144-3bd4-4d9d-9e39-0e99f49fec04)


> 📊 **Chart Explanation**  
- **Grey bars** represent the number of new users in each monthly cohort  
- **Black dotted line** shows the upward trend in sign-ups over time  
- **Blue line** represents each cohort’s 1-month retention rate (%)  
- **Red dotted line** shows the downward trend in retention

> 🔍 The diverging trends suggest a clear retention issue:  
Even as more users sign up, fewer are staying beyond the first month,  
indicating gaps in early onboarding and initial value delivery.

---

## 🔎 Insight 2: Day 1 Revisit is the Turning Point

Among users who activated (i.e., started a lesson), 9,925 returned within 30 days.  
**Day 1 revisit** emerged as a behavioural breakpoint — a signal of stronger future retention and engagement.

| Segment        | Users  | Share of Retained Users | Revenue Conversion Rate |
|----------------|--------|--------------------------|--------------------------|
| Day 1 Return   | 4,319  | 43.5%                    | 50.6%                    |
| Day 2+ Return  | 5,606  | 56.5%                    | 62.9%                    |

> 🧠 **Why Day 1 matters**  
> Nearly **half of all returning users** revisit on Day 1.  
> Among them, **1 in 2 convert to revenue**, meaning **Day 1 behaviour is the earliest and most reliable signal** of conversion intent.

📌 Compared to later returners, Day 1 users:
- Showed higher long-term survival
- Explored and completed more lessons
- Interacted more with Q&A and reviews

> 🔄 Retention curves also show that Day 1 returners drop off more slowly, making them **ideal targets for early engagement nudges**.

---
## 🔎 Insight 3: What Differentiates Day 1 Returners from Early Drop-offs?

To understand what drives users to return — and ultimately convert —  
we compared **Day 0 (activation day)** behaviours between:

- **Day 1 Returners**  
- **0-day Drop-offs** (users who never came back after first visit)


### 📘 Lesson Completion Count (Day 0)

| Segment         | Mean Completed | Median |
|-----------------|----------------|--------|
| 0-day Drop-offs | 3.35 lessons   | 2      |
| Day 1 Returners | 10.45 lessons  | 8      |

> Day 1 returners completed **3× more lessons** on average.  
> Difference is statistically significant (**p < 0.001**).



### ⏱ Time Spent on Completed Lessons

| Segment         | Mean Duration |
|-----------------|---------------|
| 0-day Drop-offs | 3.05 mins     |
| Day 1 Returners | 3.85 mins     |

> Day 0 drop-offs completed lessons **~48 seconds faster** on average.  
> This suggests they were more likely to **skip, fast-forward, or rush through** the content.



### ❌ Drop-out Time (for Incomplete Lessons)

| Segment         | Median Drop-out |
|-----------------|------------------|
| 0-day Drop-offs | 96.8 sec         |
| Day 1 Returners | 134.2 sec        |

- 25% of 0-day drop-offs quit in **under 13 seconds**  
- 50% quit within **1 minute 37 seconds**

> Day 1 returners stayed **~37 seconds longer** before dropping out.  
> Even when not completing, **longer on-screen time** signals more patience or effort.  
> Difference is statistically significant (**p < 0.001**)



### 💬 Q&A / Review Clicks

| Interaction Type         | Return Rate |
|--------------------------|-------------|
| No interaction           | 17.5%       |
| Clicked Q&A or Review    | 30–35%      |

> Users who clicked on Q&A or review sections were **~2× more likely to return**.  
> Statistically significant (**p < 0.001**)


### Summary

> Day 1 Returners didn't just come back earlier — they showed **more patience**, **more engagement**, and **more interaction** on their first visit.  
> These behavioural signals can be used as **early predictors** of conversion intent.

👉 Use this as a **baseline** for nudging early drop-offs  
(e.g., goal-setting, soft checkpoints, or interactive prompts).

---
## 🛠️Strategy Details

### ① Prevent Early Drop-off

**Rationale**  
- 25% of drop-offs quit within **13 seconds**  
- 50% quit within **1 minute 37 seconds**  
→ The beginning of the lesson is the most fragile point.

**Action Plan**  
- **0–15 seconds**: Use a strong hook or preview to spark curiosity  
- **1:00–1:30**: Gently prompt users with *Like* or *Save* options to build personal attachment

**Objective**  
Keep users engaged beyond the initial exit window (first 2 minutes), increasing chances of completing at least one lesson.



### ② Optimise Lesson Length for Completion

**Rationale**  
- Average drop-out time: **~2 min 33 sec**  
- Average completion time: **~3 min**  
- Median completed lessons (Day 1 returners): **8**

**Action Plan**  
- Restructure key lessons to stay within **3 minutes**  
- Design Day 0 journey to allow **6–8 short, completable lessons**

**Objective**  
Deliver a fast sense of achievement on Day 0 → more likely to return on Day 1



### ③ Encourage In-Lesson Interaction

**Rationale**  
- Users who clicked Q&A or review sections were **2× more likely** to return  
- Those who clicked both had the highest revisit rate (**34.7%**)

**Action Plan**  
- **Before playback**: Display a short preview of existing reviews  
- **During playback**: Show related Q&A prompts at relevant moments  
- **After playback**: Add a visible button to post a question or comment

**Objective**  
Shift passive viewers into active learners, increasing engagement and Day 1 revisit likelihood

---

## 📈 Expected Impact

### 🎯 Objective  
Increase the proportion of users who complete 8+ lessons on Day 0  
→ from **38%** to **50%** among activated users (n = 62,339)



### 🔁 Why it matters  
8+ completers show a **Day 1 revisit rate of 64.7%**  
Those who complete fewer than 8 show a much lower revisit rate  
→ Completion behaviour is a **strong early signal** of retention intent



### 📊 Impact Projection

| Metric                       | Current        | After Strategy | Change     |
|-----------------------------|----------------|----------------|------------|
| 8+ lesson completers        | 4,737 (38%)    | 6,234 (50%)    | +1,497     |
| Expected revisit rate       | —              | 64.7%          | —          |
| Additional Day 1 returners  | —              | +951 users     | —          |
| Overall Day 1 revisit rate  | 15.9%          | 17.1%          | ▲ +1.2%p   |



### ✅ Strategic Takeaway  
All improvements are achieved **without any changes in acquisition strategy or paid marketing**  
→ driven purely by **content restructuring** and **behavioural nudges**

