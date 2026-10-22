---
name: city-events
description: Find and verify public events happening in Vilnius during the current calendar week, including concerts, exhibitions, festivals, theatre, family activities, and markets. Use whenever the user asks what is happening in Vilnius this week or what to do in Vilnius, even if they do not explicitly say “events”.
---

# Vilnius City Events This Week

Find a useful, varied shortlist of public events taking place in Vilnius during the current calendar week. Verify dates and details with direct sources, and make the date range explicit.

## Workflow

1. **Set the week.**
   - The city is always Vilnius, Lithuania. Do not ask the user which city and do not include events in other cities.
   - Default to the current calendar week, Monday through Sunday, using Vilnius local time (Europe/Vilnius). Resolve the current date at the time of the request; do not assume the week from a stale example or file timestamp.
   - State the exact start and end dates, including the year. If the user explicitly gives another date range, follow it while keeping the search limited to Vilnius.
   - Apply any stated preferences such as event type, budget, language, age group, or accessibility.

2. **Search for Vilnius events.**
   - Search the web for Vilnius and the exact date range. Search multiple categories, such as concerts, exhibitions, festivals, theatre, family activities, talks, and markets, to find a varied set.
   - Prefer primary sources: official venue calendars, organizer pages, museums, festival sites, city cultural calendars, and official ticket pages. Use reputable listings to discover events, then verify candidates on primary sources when possible.
   - Open each event's source and confirm its date falls within the stated week and its location is in Vilnius. Do not include events in other cities or nearby towns.
   - Include an event only when a credible source supports its name, date, and Vilnius location. Never invent events, dates, times, venues, ticket availability, or prices.

3. **Choose and verify results.**
   - Return a varied shortlist, normally 5–10 events when enough verified options exist. Return fewer rather than pad the list with weak or unverified results.
   - Remove duplicates. Distinguish separate sessions when their dates or times differ.
   - Include the event name, date and local start time when published, venue, a short description, and verified price or ticket information when available.
   - If a time or price is not published, say “nenurodyta”. Do not imply tickets are available unless the source confirms it.
   - If only a secondary listing supports an event, identify it as a secondary source. If no credible events can be verified, say so; do not fill the list with events from outside Vilnius.

4. **Present the findings.**
   - Answer in the user's language.
   - Start with Vilnius and the exact Monday–Sunday date range searched (or the explicitly requested range).
   - Use a compact table with columns: Renginys, Data ir laikas, Vieta, Kaina / bilietai, Informacija / šaltinis.
   - Link each event directly to its most relevant event or ticket page, not only to a generic homepage.
   - After the table, highlight 2–3 picks for different interests or budgets only when supported by the evidence.
   - Briefly state material limitations, such as unlisted prices or dates that could not be independently confirmed.

## Quality checks

Before responding, verify that:

- Every event is in Vilnius and within the stated date range.
- Every event has a source link that supports the details shown.
- Times, venues, prices, and ticket availability are not inferred from unrelated pages.
- The list includes different event types when verified Vilnius options exist.
- Unknown or uncertain details are clearly marked.

Do not book tickets, register the user, or make purchases unless the user explicitly asks and the available tools support that action.
