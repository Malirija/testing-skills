---
name: run-events
description: Run the complete Vilnius weekly events workflow by gathering broad events with city-events, finding additional free community events with community-events, then combining both result sets with weekly-digest. Use when the user asks to run the weekly events workflow or produce the complete weekly Vilnius digest.
---

# Run the Vilnius Weekly Events Workflow

Run the three event skills in sequence and return the final `weekly-digest` report. The purpose of this workflow is to search both broad listings and less obvious community sources for the same week, then combine the verified results into one concise answer.

## Steps

1. **Set one shared scope.**
   - Use Vilnius, Lithuania, and the current Monday–Sunday calendar week in Europe/Vilnius unless the user specifies another date range.
   - Resolve and record exact dates, including year. Carry the same range and user preferences through every stage.

2. **Run `city-events`.**
   - Invoke the `city-events` skill and obtain its broad, verified Vilnius events shortlist.
   - Preserve the exact reporting dates and direct source links in its result.

3. **Run `community-events`.**
   - Invoke the `community-events` skill for the same dates and preferences.
   - Give it the `city-events` results so it can find additional community events and avoid duplicates.
   - Preserve its evidence for free admission, registration, dates, and organizer sources.

4. **Run `weekly-digest`.**
   - Invoke the `weekly-digest` skill with both completed result sets.
   - Return the report in the format and quality standard defined by `weekly-digest`.
   - The final answer must be the digest, not three separate skill reports.

## Reliability

- Complete the three stages in order; do not skip a stage just because the first result set looks comprehensive.
- If a skill cannot be activated by the host, read and follow its installed `SKILL.md` instructions directly. If an installed skill or its source results are unavailable, state that limitation instead of fabricating results.
- Use one consistent date range and location throughout. The final digest must deduplicate occurrences and preserve direct sources, event prices, and free-entry evidence.
- Do not book tickets, register the user, contact organizers, or make purchases.
