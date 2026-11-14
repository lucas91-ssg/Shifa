# Clinical Safety Posture

## Positioning (non-negotiable)
SHIFA is an educational tool. It is not a medical device, does not diagnose, does not dose,
does not override a physician, and never presents itself as care.

## Guardrails implemented in the MVP
1. No diagnosis: outputs are bands, points and swaps — population-level, not individual prescriptions.
2. No dosing: medication content is adherence-only (reminders), never quantity or timing changes.
3. Red-flag escalation: emergency patterns bypass the AI and instruct calling local emergency services.
4. Screener language: results say "book a test / bring this to your clinician", never "you have X".
5. Disclaimers: persistent footer, per-report line, per-chat-answer framing.

## Governance of content
- Corpus v1 = heuristic bands from public glycemic-load references, labeled as estimates.
- Corpus v2 = sign-off by a clinical advisory board (2 endocrinologists + 2 dietitians) before
  any B2B deployment; versioned file + changelog per revision.
- User flag → review loop for any dish or answer reported as wrong or harmful.

## What we will not ship
Symptom triage, drug-interaction calculators, insulin titration, pregnancy guidance,
pediatric dosing — each requires regulatory pathway and clinical ownership we do not claim.
