# 90-Day Pilot Design (Lahore first, Riyadh mirror)

## Sites & cohort
2 diabetes clinics + 2 pharmacy chains in Lahore · 500 families recruited via clinic WhatsApp
groups and pharmacy counters · informed consent at enrollment · no control group denied care
(all participants keep standard care; SHIFA is additive).

## Primary metrics
- WAU > 40% of enrolled · logs per active user per day > 1.5
- Screener completion → test-booked CTR > 25%
- Reminder adherence (doses marked done / doses due) > 60% by week 8
- D30 retention > 35%

## Secondary / business
- 2 B2B letters of intent (insurer or chain) by day 90
- Corpus v2 signed by advisory board · cost per enrolled family < $2

## Data handling
On-device default; aggregates anonymized and consent-gated for clinic dashboards;
raw logs never leave the tenant's RLS scope; deletion on request within 72h.

## Kill / pivot criteria
If WAU < 20% and D30 < 15% at day 45 → pivot channel (pharmacy-first) before scaling spend.
