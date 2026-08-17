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
Absence of Demographic Bellabeat builds wellness hardware specifically targeted at woemn. Because gender is not specified in the FitBit dataset, insights must be framed as generalized smart tracker behavior and validated against Bellabeat's target audience.
Temporal Limitation: The 2016 timeframe rrepresents legacy tracker patterns. Recommendations will focus on fundamental human habits (e.g., sedentary working hours vs. rest periods) rather than short-term app engagement trends.

