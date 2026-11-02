# ga4-ecommerce-audit-cro
Full-funnel e-commerce audit of 1.08M+ sessions using GA4 data to diagnose acquisition attribution leaks and landing page drop-offs

---

## 📊 Project Scope & Dataset Overview

* **Dataset:** Google Analytics 4 Demo Account (Google Merchandise Store - Web Data)
* **Timeframe:** Jan 1 – Oct 30, 2026
* **Data Scale:** 1,079,479 Sessions | 13,472,268 Events | 799,544 Active Users
* **Total Revenue:** $2,041,275.02 USD
* **Sitewide Purchase Conversion Rate:** 1.06%
* **Average Engagement Duration:** 45 seconds

---

## 🔍 Key Findings

### 1. Channel Acquisition Leak: The Unassigned Attribution Trap
* **Data Observation:** The `Unassigned` channel generated **73,864 sessions** and **1,515,000 events (11.25% of all site activity)**, but accounted for only **$34,834.67 (1.71% of total revenue)**.
* **Conversion Gap:** `Unassigned` traffic converted at **0.43%**, more than 59% below the site average of 1.06%.
* **Diagnosis:** Missing or malformed UTM parameters (`utm_source`, `utm_medium`) on external campaigns cause GA4 to dump active traffic into default unassigned fallback, creating attribution loss and disconnected user experiences.

### 2. Landing Page Drop-Offs: 4-Metric Screening Framework
Pages were evaluated using a 4-metric matrix: **Traffic Scale (New Users) × Purchase Conversion Rate × Average Engagement Duration × Commercial Intent**.

| Landing Page Path | New Users | Avg. Engagement Time | Purchase Rate | vs. Site Benchmark (1.06%) | Diagnostic Verdict |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **`/` (Root Homepage)** | 586,022 | 43s | **0.89%** | -16.0% | **Volume Leak:** 78% of entries; unfocused navigation. |
| **`/shop/lifestyle/bags`** | 10,108 | 43s | **0.47%** | **-55.7%** | **Critical Drop-Off:** High intent; 99.5% leave without buying. |
| **`/shop/shop-by-brand/youtube`** | 10,729 | **35s** | **0.60%** | **-43.4%** | **Critical Drop-Off:** Lowest engagement duration sitewide. |
| **`/shop/new` (Benchmark)** | 7,530 | **1m 21s** | **2.35%** | **+121.7%** | **Top Performer:** Deep engagement & clear conversion focus. |
| **`/shop/apparel/mens` (Benchmark)** | 2,127 | **1m 21s** | **2.33%** | **+119.8%** | **Top Performer:** Converts at over 2x site benchmark. |

---

## 💡 "If I Were Marketing Executive" Action Plan

1. **Standardize UTM Parameter Governance:** Implement a strict link-building taxonomy and pre-launch URL validators to eliminate unattributed sessions and restore ROAS transparency.
2. **Reallocate Untracked Spend:** Shift 20% of unmonitored promotional budget into high-performing **Cross-network** campaigns (which deliver an 80.26% engagement rate and $81K+ in revenue).
3. **Deep-Link Traffic Away from `/`:** Stop routing paid campaigns to the root homepage; direct traffic into top-performing category routes (`/shop/new` and `/shop/apparel/mens`).
4. **Redesign Leaky Category Pages:** Introduce above-the-fold filters, verified customer reviews, and clear product pricing on `/shop/lifestyle/bags` and brand hubs to lift engagement duration toward the 1-minute benchmark.


