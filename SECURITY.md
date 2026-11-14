# Security & Data Governance

SHIFA treats health-adjacent data as the most sensitive payload on the device.

## Defaults
- On-device first: meals, vitals and reminders live in localStorage until the user opts into sync.
- Optional sync uses Supabase Row-Level Security: each tenant reads only their own rows.
- No training on user data. No sale or sharing of personal data. Ever.
- LLM calls (when a key is configured) send only the user's question text plus a clinical
  system prompt. Meal logs, vitals and identifiers are never included in the request.

## Clinical guardrails (enforced in code)
- The chat refuses diagnosis, dosing and medication changes; it redirects to clinicians.
- A red-flag pattern list (chest pain, breathlessness, bleeding, unconsciousness, stroke
  signs, self-harm, in EN/UR/AR) short-circuits the AI and returns emergency guidance.
- Every report and answer carries the "education, not medical advice" disclaimer.

## Deletion
- Right to be forgotten = clear localStorage, or delete tenant rows (RLS-scoped).

## Reporting
- Security concerns: neuralfocusai@gmail.com — response target < 72h.
