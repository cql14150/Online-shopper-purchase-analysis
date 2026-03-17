# Online-shopper-purchase-analysis
# Who Will Buy? Predicting Online Shopper Purchase 
<!-- Example: "Predicting Hotel Cancellations: A Data-Driven Approach to Revenue Protection" -->
<!-- Example: "Who Will Buy? Predicting Online Shopper Conversions" -->
<!-- Example: "Smarter Outreach: Predicting Bank Marketing Campaign Success" -->

**One-line hook:** Using machine learning to identify which e-commerce visitors are most likely to purchase — so the store can act before they leave.

---

## The Business Problem

An online retailer faces a critical challenge: only 1 in 6 website visitors actually completes a purchase, yet the store has no reliable way to distinguish serious buyers from casual browsers in real time. Without this insight, marketing budgets are wasted on visitors who were never going to buy, while high-intent customers leave without a personalized nudge. Building a predictive model to identify likely buyers before they exit could meaningfully increase revenue without increasing traffic.


<!--
Tip: Lead with the pain, not the data.
Instead of "This project analyzes a dataset of 119K hotel bookings..."
Try: "A Portuguese hotel chain loses an estimated millions annually to last-minute cancellations..."
-->

## The Data

The dataset contains 12,330 website sessions collected over one year from a real e-commerce store, sourced from the UCI Machine Learning Repository. Each session captures how visitors behaved — how many product pages they viewed, how long they stayed, how often they bounced — along with contextual details like the time of year, visitor type, and traffic source. The target variable is whether the session ended in a purchase (15.47% did).

<!--
Tip: Translate technical details into human terms.
Instead of "The dataset has 32 features and 119,390 rows..."
Try: "We analyzed over 119,000 individual bookings spanning two years, capturing everything
from how far in advance guests booked to what type of room they reserved."
-->

## Key Discoveries

- **Engaged browsers are buyers:** Visitors who purchased had PageValues nearly 14x higher than non-buyers (27.26 vs 1.98) — deeper browsing is the single strongest signal of purchase intent.
- **Holiday shopping drives conversions:** Conversion rates spike to 25% in November and 21% in October, compared to a flat 1–10% across most other months.
- **New visitors punch above their weight:** New visitors convert at 24.91% — nearly double the 13.93% rate of returning visitors — despite making up only 14% of total traffic.
- **Special days don't drive purchases:** Sessions near holidays convert at only 6.16%, compared to 16.53% on normal days — holiday traffic brings browsers, not buyers.

<!--
Tip: Write findings as "headlines" a newspaper editor would approve.
Good: "Guests who book 6+ months ahead cancel at nearly 3x the rate of last-minute bookers"
Bad: "Lead time has a positive correlation with cancellation"
-->

## Visualizing the Story

<!-- Embed your most compelling chart. Pick the ONE visual that best captures your main finding. -->

![Description of your chart](my_chart.png)

*Conversion rates spike sharply in November and December — Q4 is the store's highest-opportunity window and where marketing budgets should be concentrated.*
*

## Prediction Model

A Gaussian Naive Bayes classifier achieved 79.72% overall accuracy. Out of 411 actual buyers in the test set, the model correctly identified 253 and missed 158 — representing roughly $7,900 in unaddressed revenue per cycle at a $50 average order value. A Logistic Regression model tested in the bonus section achieved 87.10% accuracy, suggesting room to improve buyer detection with a more powerful model.

<!--
Tip: Translate model metrics into business impact.
Instead of "The model achieved 78% accuracy..."
Try: "Our model correctly flags 8 out of 10 at-risk bookings, giving the hotel front desk team
enough lead time to proactively reach out and offer flexible rebooking options."
-->

## Recommendations

1. **Concentrate Q4 marketing spend:** Shift at least 50% of the annual budget to November and December — conversion rates more than double during this window.
2. **Invest in new visitor acquisition:** [New visitors convert at nearly twice the rate of returning ones yet make up only 14% of traffic — reallocating spend toward paid search or referral programs could significantly increase overall sales.
3. **Trigger real-time offers for high-PageValue sessions:** PageValues was the single strongest predictor of purchase — flagging high-value sessions and delivering a personalized offer could recover an estimated $3,950+ in missed revenue per cycle.

## Tools & Techniques

Python | Pandas | Scikit-Learn | Matplotlib | Seaborn | Gaussian Naive Bayes | Google Colab

---

*This project was completed as part of ISOM 835: Predictive Analytics at Suffolk University's
Sawyer Business School.*
