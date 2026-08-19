# 📊 Case study: Bellabeat Data Analysis

## Introduction 
Bellabeat is a high-tech manufacturer of health-focused smart products designed specifically for women. While Bellabeat is an established player in the wellness industry, analyzing consumer smart device habits presents an opportunity to unlock new growth avenues and expand its global market footprint.


## Phase 1: Ask

### 1. Selected Product Focus: Bellabeat Leaf
The **Leaf** is Bellabeat's classic wellness tracker that can be worn as a bracelet, necklace, or clip. It can be connected to the Bellabeat app to monitor activity, sleep, and stress levels. Because the Leaf is designed for versatile 24/7 wearability across different occasions, analyzing non-Bellabeat smart tracker data offer insights into daily wearing consistency, sedentary patterns, and sleep tracking habits.

### 2. Business Task Statement 
Analyze non-Bellabeat smart device data to identify behavioral patterns in physical activity, sedentary time, and sleep monitoring. Apply these insights to optimize marketing campaigns, highlight the product's versatility, and improve user retention within the Bellabeat app ecosystem.

### 3. Key Business Questions 
        1. What are some key trends in smart device usage? 
        2. How could these trends apply to Bellabeat customers? 
        3. How could these trends help influence Bellabeat's marketing strategy? 

### 4. Key Stakeholders
        Urška Sršen: Cofounder and Chief Creative Officer
        Sando Mur: Mathematician and Bellabeat Cofounder
        Bellabeat Marketing Analytics Team:** Core team guiding overall campaign and positioning strategies

## Phase 2: Prepare

### 1. Data Source Information
Dataset Name: Fitbit Fitness Tracker Data (Public Domain / CC0, available via Mobius on Kaggke)
Contents: Minute-,hour-, and daily-level tracker records from 30 eligible Fitbit users who consented to share activity, heart rate, step count, and sleep logs.
Key Files Selected for Analysis: 
    `dailyActivity_merged.csv`: Tracks overall daily steps, distances, intensities, and calories.
    `sleepDay_merged.csv`: Tracks sleep records, total minutes asleep, and total time in bed.

### 2. Data Credibility & Integrity (ROCCC Analysis)
Reliability (Low): The sample contains only 30 individual users, which is the minimum sample threshold for the Central Limit Theorem but limits statistical power and broader generalization.
Originality (Low): Gathered via third-party distributed survey through Amazon Mechanical Turk rather than first-party collection.
Comprehensiveness (Medium): Captures essential daily physical health metrics (steps, sleep, calories, active vs. sedentary minutes), but lacks demographic details such as user age and gender.
Currentness (Low): The data was collected over a one-month window in March-May 2016. Tracking technology and consumer daily habits have evolved since the collection.
Citation (High) Dedicated open dataset under CC0: Public Domain license.

### 3. Data Limitations & Business Implications
Absence of Demographic Bellabeat builds wellness hardware specifically targeted at women. Because gender is not specified in the FitBit dataset, insights must be framed as generalized smart tracker behavior and validated against Bellabeat's target audience.
Temporal Limitation: The 2016 timeframe represents legacy tracker patterns. Recommendations will focus on fundamental human habits (e.g., sedentary working hours vs. rest periods) rather than short-term app engagement trends.

## Phase 3: Process
1. Tools Used:
Python (NumPy, Pandas): Used for data transformation, manipulation, deduplication, and datetime parsing.
Matplotlib & Seaborn: Data visualization and exploratory charts.

2. Data Cleaning & Transformation Steps
Deduplications: Identified and removed 3 duplicate records found within `sleepDay_merged.csv`.
Missing Value Audit: Confirmed 0 null or missing values across both primary tables.
Datetime Standardization: Parsed `ActivityDate` and `SleepDate` from object strings to formal ISO datetime formats.
Feature Engineering: Extracted `DayOfWeek` from activity timestamps to evaluate day-specific user habits.
Data Integration: Performed an inner merge on `Id` and `ActivityDate` to combine daily physical metrics with sleep duration records.

## Phase 4: Analyze

Key findings
Dominant Sedentary Behavior: Users spend an overwhelming **81.3%** of their daily recorded time inactive/sedentary, with high-intensity active time accounting for only **1.7%
Sub-Optimal Daily Activity: Users average ~7,600 steps per day, consistently falling short of the recommended 10,000-step baseline. 
Weekly Fluctuations: Activity levels peak mid-week (Tuesday) and on Saturdays, followed by a noticeable drop on Sundays.
Sleep vs. Time in bed: Users average ~419 minutes (~7 hours) of actual sleep out of ~458 minutes spent in bed, indicating approximately 39 minutes of latency/wakefulness before falling asleep or getting up.


## Phase 5: Share

1. Daily User Activity Breakdown (`visualization/activity_distribution.png`)

   What is shows: A proportional breakdown of walking minutes across four intensity levels: Sedentary, Lightly Active, Fairly Active, and Very Active.
   Takeaway: Smart device users spend the vast majority of they day sedentary (over 81%), highlighting a major opportunity to convert idle desk/screen time into light movement.

2. Weekly Step Patterns (`visualization/daily_steps_trend.png`)

   What it shows: Average total steps logged across each day of the week, benchmarked against the standard 10,000 steps a day target.
   Takeaway: Users maintain steady engagement from Tuesday through Sunday (~7,500 - 8,100 steps) but drop significantly on Sundays (~6,900 steps), indicating a clear weekend drop-off in routine                tracking and movement.
3. Calorie Expenditure vs. Total Steps (`visualization/steps_vs_calories.png`)

   What it shows: Scatter plot with an overlay linear regression trend line that measures caloric burn relative to total daily steps.
   Takeaway: Confirms a strong positive correlation ($R > 0.5$) between daily step volume and calories burned, validates that consistent low-to-moderate activity yields steady caloric output.


## Phase 6: Act

Based on behavioral patterns identified in the data, here are three strategic marketing and product recommendations for the Bellabeat Leaf

1. Promote Discreet Sedentary Alerts
   
   Insights: Over 80% if daily tracker time is sedentary
   Strategy: Leverage the Bellabeat Leaf as an everyday fashion accessory (necklace, bracelet, or clip) designed to provide subtle, silent vibration reminders during long work hours to break up                sedentary stretches
   
2. Gamified Weekend & Mid-Week Step Challenges

   Insights: Step volume dips toward the end of the workweek and hits a low on Sunday.
   Strategy: Introduce an app-based "Sunday Reset" and "Mid-Week Boost" streak challenges via the Bellabeat App to incentivize users to hit 10,000 steps consistently across all seven days

3. Bedtime Relaxation & Sleep Optimization Content

   Insights: Users spend nearly 40 minutes awake or restless in bed before falling asleep.
   Strategy: Leverage Leaf's lightweight, screen-free form factor
