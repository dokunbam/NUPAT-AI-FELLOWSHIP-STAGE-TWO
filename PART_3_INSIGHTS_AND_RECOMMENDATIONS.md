# NUPAT AI Fellowship – Stage Two Case Study

## PART 3 INSIGHTS AND RECOMMENDATIONS

---

#### Question:

The product team wants to launch a 'Low-Volume Trader' marketing campaign in
Kenya. Using the data, how would you define the target audience for this campaign? Describe
2-3 data points you would use to create this user segment."

## 1. Low-Volume Trader Campaign – Target Audience Definition (Kenya)

To support the launch of a "Low-Volume Trader" marketing campaign in Kenya, the target
audience can be defined using user-level trading behavior restricted to Kenyan markets
(e.g., trading pairs quoted in KES such as ETHKES).

### Target Audience Definition

Low-volume traders are users who engage with the platform but trade infrequently or with
small transaction values, indicating growth potential through targeted incentives and
education.

### Key Data Points for Segmentation

1. **Total Trading Volume (USD)**

   - Users whose cumulative trading volume falls below a defined threshold (e.g., bottom
     30–40% of USD trading volume among Kenyan users).
   - This captures users with limited financial engagement.

2. **Trade Frequency**

   - Users with a low number of executed trades over the analysis period.
   - Helps distinguish occasional traders from active participants.

3. **Market Participation**
   - Users who trade in only one or two currency pairs (e.g., ETHKES only).
   - Indicates limited product exploration and potential for cross-market engagement.

### Campaign Rationale

By targeting low-volume Kenyan traders, the campaign can focus on education, fee incentives,
and localized messaging to increase trading confidence and long-term platform engagement.

#### Insights, Risks, and Recommendations

## 1. Key Market and User Insights

### Market Concentration

Analysis of trading activity reveals that a small number of trading pairs account for the
majority of total USD trading volume. This concentration suggests that liquidity and risk
exposure are highly dependent on a few dominant markets. Any disruption in these pairs
could have an outsized impact on overall platform stability.

### User Activity Patterns

User deposit behavior exhibits clear temporal trends, with higher activity during specific
hours of the day and on particular days of the week. These patterns indicate predictable
usage cycles that can be leveraged for system capacity planning and enhanced fraud
monitoring during peak periods.

### Market Volatility

The BTCNGN trading pair shows noticeable short-term volatility when analyzed using rolling
statistical measures. This volatility highlights the importance of continuous market
monitoring, particularly for high-volume pairs where rapid price changes may increase
risk exposure.

---

## 2. Fraud Detection Findings

A subset of users demonstrates unusually high trading frequency and large cumulative
transaction amounts relative to the broader user population. In the absence of explicit
fraud labels, heuristic rules were applied to flag extreme behaviors as potential indicators
of fraudulent activity.

Using these proxy labels, a supervised classification model was trained to distinguish
high-risk users based on aggregated behavioral features. The results suggest that user-level
trading patterns can provide meaningful signals for fraud risk identification, even with
limited labeling information.

---

## 3. Limitations

### Proxy Labeling

Fraud labels were generated using percentile-based heuristics rather than confirmed fraud
cases. While this approach enables model training, it may introduce noise and does not
guarantee true fraud identification.

### Feature Scope

The analysis relies on aggregated user-level features and does not account for
transaction-level sequencing, burst behavior, or rapid directional changes in trading
activity.

### Exchange Rate Assumptions

A fixed currency conversion rate was used for all trades, which simplifies analysis but may
not reflect real-world exchange rate fluctuations.

---

## 4. Recommendations and Future Improvements

### Enhanced Feature Engineering

Future work should incorporate temporal and behavioral features such as inter-trade time,
trade frequency spikes, and buy/sell imbalances to improve fraud detection accuracy.

### Advanced Modeling Approaches

Unsupervised and semi-supervised anomaly detection techniques, including Isolation Forests
and autoencoder-based models, could reduce reliance on heuristic labels and better capture
previously unseen fraud patterns.

### Real-Time Fraud Monitoring

Deploying streaming data pipelines would enable near real-time detection of suspicious
behavior, allowing faster intervention and reduced financial risk.

### Model Governance and Monitoring

Establishing processes for model explainability, performance monitoring, and periodic
retraining would support long-term reliability and regulatory compliance.

---

## 5. Conclusion

This case study demonstrates a structured AI engineering workflow spanning exploratory data
analysis, feature engineering, and machine learning. Despite data and labeling limitations,
the proposed approach provides a scalable foundation for monitoring market activity and
detecting potential fraud within a digital asset trading platform.
