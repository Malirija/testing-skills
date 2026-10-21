---
name: city-events
description: Find concerts, exhibitions, festivals, theatre, family activities, markets, and other public events in a specified city for specified dates. Use whenever the user asks what is happening in a city, what to do on a certain date or weekend, or asks to discover local events—even if they do not say “events” explicitly.
---

# City Events

Find useful, date-specific public events in the city the user requests. Prioritize accuracy, relevant variety, and direct links over a long list.

## Workflow

1. **Confirm the search scope.**
   - Identify the city and date or date range from the request.
   - If either the city or dates are missing and cannot be reasonably inferred from the current conversation, ask one concise clarifying question before searching.
   - Interpret relative dates using the current date, and use the city's local time zone. State the interpreted dates explicitly.
   - If the user gives interests, budget, language, age group, accessibility needs, or preferred event types, apply them as filters. Otherwise, search across a varied mix of event types.

2. **Search the web.**
   - Search for events in the requested city and exact date range.
   - Prefer primary sources: official venue calendars, organizer pages, museums, festival websites, city cultural calendars, and official ticketing pages.
   - Use reputable event listings to discover candidates, then verify each event and date against a primary source when possible.
   - Search more than one source and vary the queries by category (for example, concerts, exhibitions, festivals, theatre, and family events) so the results are not limited to one listing site.
   - Open the event page and confirm the event is scheduled for the requested date. For multi-day events, make sure the requested date falls within the event dates.
   - Include an event only when there is a credible source for its name, date, and location. Never invent events, dates, venues, ticket availability, or prices.

3. **Select and organize results.**
   - Return a useful, varied shortlist, normally 5–10 events when enough verified options exist. Return fewer rather than pad the list with weak or unverified results.
   - Avoid duplicates and distinguish separate sessions of the same event when dates or times differ.
   - Prefer specific, actionable information: event name, date and local start time if published, venue or area, brief description, price or ticket information if verified, and a direct source link.
   - If a price or time is not published, say “not listed” rather than guessing. Do not imply tickets are available unless the source confirms it.
   - If only a secondary listing can be found, label it accordingly. If no credible events can be verified for a date, say so and suggest broadening the date range or nearby area.

4. **Present the answer in the user's language.**
   - Start with the city and exact dates searched.
   - Use a compact table with columns: Event, Date and time, Venue, Price/tickets, Details/source.
   - Link event names or source text directly to the most relevant event page, not just a generic homepage.
   - After the table, highlight 2–3 picks for different interests or budgets only when the evidence supports those recommendations.
   - Briefly note any limits, such as unavailable prices, incomplete listings, or dates that could not be independently confirmed.

## Quality checks

Before responding, verify that:
- Every listed event falls within the requested dates and city/area.
- Every event has a source link that supports the details shown.
- Date, time, venue, and price claims are not inferred from unrelated pages.
- Results are not all from a single category when varied options are available.
- Uncertainty and missing information are clearly marked.

Do not book tickets, register the user, or make purchases unless the user explicitly asks and the available tools support that action.
