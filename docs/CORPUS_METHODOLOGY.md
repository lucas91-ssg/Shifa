# Glycemic Corpus: Methodology & Limits

## Structure
Each dish = { name, band (0 low / 1 medium / 2 high), swap }. Points: low=1, med=2, high=3.
Daily budget default = 6 points (heuristic allowance for starch-heavy days; user-adjustable in v0.3).

## How bands were set (v1)
Standard-portion glycemic-load estimates from public GL tables and regional food-composition
references, banded: GL low <10, med 10-19, high ≥20 per portion [per-dish sources to be
itemized and verified in v2]. Swaps are portion/sequence changes (half plate, veg+protein first,
ralta/salad pairing), never eliminations — adherence beats perfection.

## Known limits (stated, not hidden)
- Individual glycemic response varies (microbiome, timing, activity); bands are population averages.
- Restaurant portions vary; "full plate" entries assume common street/restaurant serving.
- v1 is a behavioral nudge tool, not a clinical instrument; CGM-linked personalization is v2 research.

## Validation pipeline (v2)
Dietitian review → endocrinologist sign-off → versioned corpus file → changelog → re-deploy.
Every band change is traceable to a reviewer and a source.
