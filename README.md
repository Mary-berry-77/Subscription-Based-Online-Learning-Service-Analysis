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
- a +5%p increase in Day 1 revisit rate (from 43.5% → 48.5%)
  - +1,177 more early returners  
  - ~600 more revenue-converting users  



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
| Acquisition | New sign-ups (Nov 2022 – Dec 2023)            | 98,452   | -               |
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

Among users who activated (i.e., started a lesson), 23.3k returned within 30 days.  
**Day 1 revisit was the strongest differentiator** of future retention and revenue.

| Segment      | Users   | Revenue Conversion Rate |
|--------------|---------|--------------------------|
| Day 1 Return | 10,139  | 50.6%                    |
| Day 2+       | 13,194  | 62.9%                    |

> 43.5% of returners came back **exactly on Day 1**  
> These users stayed longer, completed more content, and interacted more than later returners.

---

## 🌐 Behavioural Comparison: Day 1 vs Later vs Drop-off

| Metric                   | Day 1 Returners | Day 2–7 Returners | Day 8–30 Returners | 0-day Drop-offs |
|--------------------------|----------------|--------------------|--------------------|-----------------|
| Avg. lesson completions  | 117.4          | 82.6               | 60.8               | 0               |
| Avg. lesson exploration  | 83.7           | 51.4               | 32.2               | 1.2             |
| Avg. time on first visit | Long           | Medium             | Short              | Very short      |
| Q&A / Review clicks      | High           | Medium             | Low                | Near zero       |

Day 1 returners didn’t just come back earlier —  
they showed **greater intent, patience, and engagement** on Day 0.

---

## 🧠 Interpretation

Early revisit ≠ coincidence  
→ It's a **signal of intent and quality of first experience**.  
Without a good Day 0, users don't return — regardless of future potential.

---

## 🛠️ Strategic Recommendations

1. **Prevent early exits**: Simplify the start of the first lesson; make value obvious within the first few minutes  
2. **Shorten initial lessons**: Break long content into quick wins to build momentum  
3. **Nudge interactions early**: Move Q&A and reviews earlier in the experience to spark curiosity  
4. **Send follow-up messages at +24h**: Target users who did not return within 1 day

---

## 📊 Estimated Impact

Simulation shows:
- Improving Day 1 revisit by +5%p
→ Overall retention increases by **+3.5%p**
→ Thousands more users pass the trial barrier and convert to revenue

---

## 👥 Team & Role

- 3-person team, 4-week sprint
- I led planning, schema design, and log integration (13 raw tables → unified session dataset)
- Designed cohort/funnel logic, conducted behavioural analysis, and quantified strategic impact

---

## 🧰 Tools

- Python (Pandas, NumPy, Seaborn)
- Jupyter / Google Colab
- Markdown, Lucidchart

---

## 📄 Appendix

Full report includes:
- AUC analysis
- Segment-specific retention curves
- Behavioural breakdown tables
- Strategy impact simulations

👉 [Contact me](mailto:your.email@example.com) for the full report or walkthrough.

