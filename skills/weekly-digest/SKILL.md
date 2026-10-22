---
name: weekly-digest
description: Combine verified results from the city-events and community-events skills into one concise, useful weekly report for Vilnius. Use when the user asks for a weekly events digest, roundup, or combined report; gather mainstream city events and additional free community events, deduplicate them, and present dates, links, costs, and useful picks together.
---

# Weekly Events Digest for Vilnius

Create one concise weekly report by combining the verified output of `city-events` and `community-events`. The city-events results provide a broad range of events; community-events adds less obvious, explicitly free public activities. Keep both contributions, make their status clear, and remove duplicates.

## Workflow

1. **Set the shared reporting period.**
   - The location is Vilnius, Lithuania.
   - Default to the current calendar week, Monday through Sunday, in Vilnius local time (Europe/Vilnius). Resolve the current date at request time and state the exact start and end dates, including the year.
   - If the user requests another date range, use it consistently for both source skills and the digest.
   - Carry through user preferences such as family suitability, budget, accessibility, or event type.

2. **Collect both sets of results.**
   - Use the `city-events` skill for the broad Vilnius events shortlist and `community-events` for additional free, public, locally organized events.
   - When either result is already present in the conversation, reuse it and obtain only the missing set. Do not repeat a completed search without reason.
   - If results are not yet available, follow each skill's instructions to obtain them for the same date range. If a skill or its results are unavailable in the current environment, state that limitation and do not fabricate or silently substitute its findings.
   - Preserve direct source links and the evidence each source provides. Do not upgrade an unverified date, price, free-entry claim, or ticket status while combining results.

3. **Normalize and deduplicate.**
   - Treat entries as duplicates when they refer to the same event occurrence, even if the title, organizer wording, or source differs. Preserve genuinely separate sessions on different dates or at different times.
   - Merge useful complementary details from both sources into one row and retain the strongest direct source link for each claim. Include a second link only when it supports a distinct important detail.
   - Keep the community label for qualifying free community events. Mark an event “nemokamas” only when the community-events evidence confirms no required payment; label voluntary donations or required registration separately.
   - Keep unclear prices as “kaina nenurodyta” and do not imply tickets are available without supporting evidence.
   - Check that every event is in Vilnius and within the shared reporting period. If source results use different date ranges, exclude incompatible entries or resolve the mismatch before including them.

4. **Build a concise, useful report.**
   - Answer in the user's language. Start with the exact Vilnius reporting period.
   - Select a balanced shortlist, normally 6–12 distinct events if enough verified candidates exist. Return fewer rather than pad the report. Prefer variety across days, event types, neighborhoods, and price levels.
   - Order the main list chronologically. Include only the details that help the user decide: event, date and local time, venue or district, price/free status, registration or ticket note, and direct source.
   - Highlight up to three practical picks when the evidence supports them, for example a free community option, a family-friendly option, or a strong paid event. Respect the user's stated preferences; do not manufacture rankings.
   - Briefly note missing details, source limitations, or the absence of one source set. Avoid repeating the same event in separate sections.

## Output format

# Vilniaus savaitės renginių suvestinė
**Laikotarpis:** [exact dates, Monday–Sunday]

**Trumpai:** [one sentence describing the mix, including free community options if any are verified]

| Renginys | Data ir laikas | Vieta / rajonas | Kaina ir registracija | Šaltinis |
|---|---|---|---|---|

**Verta atkreipti dėmesį:** [up to three distinct picks, only when useful and supported]

**Pastaba:** [include only if a relevant limitation or uncertainty needs explanation]

Use clear labels such as **Nemokamas · bendruomenės renginys**, **Mokamas**, or **Kaina nenurodyta**. Omit empty sections. Link event names directly to their event or organizer pages.

## Quality check

Before sending the digest, confirm that:

- Both skills' results were considered, or a missing source set is disclosed.
- Every event has the same Vilnius location and requested date scope.
- Duplicate occurrences appear once, while distinct sessions remain distinct.
- Free entry, prices, ticket availability, and registration status reflect the evidence and are not guessed.
- Direct links support the claims shown, and unknown details are identified.
- The report is concise, chronological, varied, and does not repeat recommendations as duplicate event entries.

Do not book tickets, register the user, contact organizers, or make purchases.
