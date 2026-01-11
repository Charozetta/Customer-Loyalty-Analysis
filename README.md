# Yandex.Afisha Customer Loyalty Analysis

## Project Overview

This project analyzes customer behavior and loyalty patterns on Yandex.Afisha, a popular ticketing platform. The goal is to identify key factors that drive customer retention and understand the characteristics of loyal vs. one-time customers.

**Dataset:** 290,611 orders from 64,979 unique users during 2024
**Analysis Period:** 2024
**Return Rate:** 62% of customers make repeat purchases

---

## Key Questions Addressed

1. **What proportion of users make repeat purchases?** 
   - 62% of users (13,308) make 2+ purchases
   - 29% of users (6,251) make 5+ purchases

2. **Which characteristics of the first order predict customer retention?**
   - Event type significantly impacts return rate (Theater: 64.5%, Sport: 55%)
   - Device type shows minor but notable effect (Desktop: 64.9%, Mobile: 61.3%)

3. **How does transaction value relate to retention?**
   - Surprisingly, higher first purchase value does NOT guarantee return
   - Average revenue difference: only 5.5% between loyal and one-time customers
   - **Key insight:** Number of tickets (2-3 tickets = 74% return rate) matters more than amount spent

4. **What are the temporal patterns in purchases?**
   - Day of week effects are moderate (Saturday: 63.7%, Friday: 60.7%)
   - Significant retention patterns by purchase interval

5. **How to segment customers effectively?**
   - 2-3 ticket purchases show healthiest retention (73.98%)
   - 5+ tickets indicate one-time bulk purchases (18.5% return rate)
   - Clear correlation between purchase frequency and loyalty

---

## Main Findings

### Finding 1: The Retention Paradox
Contrary to expectations, **customers who spend more on their first purchase are NOT more likely to return**. The mean transaction value is only 5.5% higher for returning customers (561 RUB vs. 532 RUB). This suggests that building purchasing habits matters more than initial transaction size.

### Finding 2: Ticket Count is the True Predictor
The number of tickets in a purchase is a much stronger predictor than revenue amount:
- **2-3 tickets:** 73.98% return rate (healthy purchasing pattern)
- **5+ tickets:** 18.5% return rate (likely bulk/group purchase)
- Single tickets show moderate retention (around 50%)

### Finding 3: Event Type Drives First-Time Conversion
Certain event categories have higher return rates:
- **Theater:** 64.52% return rate
- **Exhibitions:** 63.21% return rate
- **Concerts:** 62.87% return rate
- **Sports:** 55% return rate

This suggests these categories should be emphasized in marketing and onboarding.

### Finding 4: Distribution Insights
The revenue distribution follows a classic long-tail pattern:
- Peak concentration: 100-300 RUB (majority of first-time buyers)
- Gradual decline through 500-800 RUB
- Extended tail with rare high-value purchases (800-1600 RUB)
- Outliers were identified and removed (95th percentile filtering)

---

## Repository Structure

```
├── project.ipynb            
├── .env.example              
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Quick Start

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Run the Analysis
```bash
jupyter notebook
```

---

## Data Privacy & Security

- Database credentials are managed through environment variables (.env file)
- Sensitive information is excluded from version control (.gitignore)
- No personal user data is exposed in analysis outputs
- All data handling follows data protection best practices (anonimous data)

---

## License

This project is provided for portfolio demonstration purposes. The analytical methodology and code structure can be adapted for similar business intelligence projects involving customer behavior analysis.

---

**Last Updated:** January 2026  
**Status:** Complete - Ready for Review  
**Language:** English (Notebook translated from Russian)
