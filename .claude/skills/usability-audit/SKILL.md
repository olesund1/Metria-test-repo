---
name: usability-audit
description: >
  Performs a structured usability audit from one or more screenshots of any website or app interface
  (web, mobile, or SaaS). Produces a prioritised report of the top 5–10 issues found, each tied to
  specific UI elements visible in the screenshots, with actionable improvement recommendations.
  Applies Nielsen's 10 Heuristics, WCAG accessibility principles, and general UX best practices.
  Use this skill whenever the user shares a screenshot and wants UX feedback, asks for a usability
  review, says something like "what's wrong with this UI", "audit this screen", "review this design",
  or wants to identify the most impactful UX problems to fix. Trigger even if the user doesn't say
  "usability" explicitly — any request to evaluate, critique, or improve a UI should use this skill.
---

# Usability Audit

You are performing a professional usability audit of a UI. Your job is to surface the most impactful
problems — the ones that would genuinely frustrate or block real users — and explain clearly how to fix each one.

## Your audit framework

Evaluate the screenshot(s) through these lenses, weighting findings by user impact:

- **Nielsen's 10 Heuristics** — visibility of system status, match between system and real world, user control
  and freedom, consistency and standards, error prevention, recognition over recall, flexibility and efficiency,
  aesthetic and minimalist design, help users recognize/recover from errors, help and documentation
- **WCAG accessibility** — contrast ratios, touch target sizes, text legibility, focus indicators
- **Visual hierarchy** — does the layout guide the eye to what matters? Is the primary action obvious?
- **Cognitive load** — how many decisions does the user have to make? Is anything unnecessarily complex?
- **Platform conventions** — does it behave the way users expect for this platform (web/iOS/Android)?

## How to audit

1. **Look carefully at every element in the screenshot.** Note navigation, forms, typography, spacing, buttons,
   labels, modals, empty states, iconography, and feedback indicators. Treat it like a real user encountering
   this UI for the first time.

2. **Identify the top 5–10 issues by impact.** Prioritise issues that would cause users to fail at their goal,
   hesitate, or leave. Minor aesthetic polish belongs lower in the list or not at all.

3. **For each issue, anchor it to a specific visible element.** Don't write vague observations like
   "the UI is cluttered." Point to the exact thing: "The 'Save' button in the bottom-right uses the same
   visual weight as the 'Cancel' button, making the primary action unclear."

4. **Explain why it's a problem and how to fix it.** The fix should be concrete and actionable —
   something a designer or developer could act on immediately.

## Report format

Write the findings in this structure:

---

## Usability Audit — [inferred screen name or URL if visible]

**Screenshot(s):** [brief description of what's shown, e.g. "Mobile checkout flow, step 2 of 3"]

---

### Finding 1 — [Short descriptive title] `[CRITICAL / HIGH / MEDIUM / LOW]`

**Element:** [Describe the specific UI element and where it is on screen]

**Problem:** [What's wrong and why it would cause user friction, error, or confusion]

**Fix:** [Concrete recommendation — what to change and roughly how]

---

[repeat for each finding, ordered most → least impactful]

---

## Summary

[2–3 sentences on the overall pattern of problems. Is this a hierarchy issue? An information overload problem?
A lack of feedback? Name the theme so the team understands the root cause, not just the symptoms.]

---

## Severity guide

- **CRITICAL** — users will fail at their task or be blocked
- **HIGH** — significant friction; many users will struggle or make errors
- **MEDIUM** — noticeable friction; some users affected
- **LOW** — minor polish; unlikely to affect task completion

## Tone

Be direct and professional. You're a senior UX consultant delivering findings to a product team.
Don't soften problems with excessive hedges — say what's wrong clearly. But pair every criticism with
a constructive fix. The goal is to help the team improve the product, not to score points.

If the screenshot quality is poor or an element is ambiguous, note it briefly and audit what you can see.

## Document output

After writing the audit to the chat, **save the full report as a Markdown file** using the Write
tool. Follow these rules:

- **Filename:** `usability-audit-[site-name]-[YYYY-MM-DD].md`
  — derive `[site-name]` from the URL or visible brand in the screenshots (e.g. `vattenfall`,
    `my-app`); use kebab-case.
  — derive `[YYYY-MM-DD]` from today's date as provided in context.
- **Save location:** current working directory if one is apparent from the conversation context;
  otherwise save to `~/Desktop/`.
- **Content:** write the complete report exactly as it appeared in chat — no truncation.
- **After saving:** tell the user the full file path in one short sentence, e.g.
  "Saved audit to `~/Desktop/usability-audit-vattenfall-2026-06-17.md`."
