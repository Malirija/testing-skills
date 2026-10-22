---
name: community-events
description: Discover additional free, public, community-oriented events in Vilnius during the current calendar week, especially events from neighborhood groups and other less obvious sources that broad city event listings may miss. Use alongside city-events when the user wants more local, grassroots, library, community-center, neighborhood, volunteer, or low-key activities, or asks for free community events in Vilnius.
---

# Community Events in Vilnius

Find additional free public events in Vilnius for the current calendar week, with a focus on grassroots and community sources that broad event listings may overlook. Complement the `city-events` skill: check its results in the conversation when available, remove duplicates, and prioritize distinct discoveries.

## Workflow

1. **Set the scope.**
   - Search only in Vilnius, Lithuania. Do not ask which city.
   - Default to the current calendar week, Monday through Sunday, in Vilnius local time (Europe/Vilnius). Resolve the current date at request time and state the exact dates, including year.
   - Follow an explicitly requested date range while keeping the location limited to Vilnius.
   - Apply preferences such as family suitability, accessibility, language, or event type.

2. **Look beyond major event listings.**
   Search a varied set of community-oriented sources, prioritizing the organizer's own calendar or announcement:
   - Public libraries, local branches, and reading or cultural clubs.
   - Vilnius neighborhood associations, community groups, and district or seniūnija announcements.
   - Community and cultural centers, local museums, and small independent venues.
   - Volunteer organizations, civic initiatives, environmental groups, and neighborhood projects.
   - Universities, student groups, makerspaces, hobby clubs, and public workshops.
   - Public park, walking, gardening, repair, swap, board-game, and other locally organized activities.
   - Public social media posts or event pages from identifiable organizers when they are accessible and contain enough detail to verify the event.

   Use broad city calendars and ticketing platforms mainly to discover leads or check for duplicates; do not let them crowd out local sources. Search in Lithuanian and, when useful, in English or other languages used by local organizers. Vary queries by district, venue type, and activity so the search is not limited to central Vilnius or one platform.

3. **Verify that each event qualifies.**
   - Confirm from a credible, preferably organizer-controlled source that the event occurs within the chosen dates and physically takes place in Vilnius or is a clearly described public online event organized by a Vilnius community group.
   - Include only events open to the public. Exclude private, members-only, or invitation-only gatherings.
   - Treat an event as free only when the source explicitly says it is free, lists a zero price, or otherwise clearly confirms there is no required payment. If a suggested donation is voluntary, label it as such. If cost is unclear, omit it from the free-event list or put it in a clearly separated “kaina nepatvirtinta” note; never imply it is free.
   - Check whether registration is required, whether places are limited, and any age or accessibility restrictions when the source states them. Do not equate “free” with “no registration required.”
   - Verify the event name, date, location, and free admission from the source itself. Never invent details or rely on a search-result snippet when the page can be opened.
   - If a source is an organizer's social post or a secondary listing, identify it accurately and link directly to it. If details are incomplete, state what could not be confirmed.

4. **Deduplicate and select.**
   - Compare candidates with the `city-events` results already present in the conversation. Exclude events already listed there unless the community source adds a meaningful detail; if included for that reason, explain the added detail.
   - Prefer smaller, locally organized, participatory, or neighborhood-based events over large headline events. Include a useful mix of activities when evidence supports it.
   - Return a concise shortlist, normally 3–8 verified events. Return fewer when few qualify; do not fill the list with paid, uncertain, or weakly sourced events.
   - If no qualifying events can be verified, say so and briefly describe the source types checked.

## Response format

Answer in the user's language. Begin with **Vilnius** and the exact date range searched. Use a compact table:

| Renginys | Data ir laikas | Vieta / rajonas | Nemokamumas ir registracija | Organizatorius / šaltinis |
|---|---|---|---|---|

Link each event to its direct organizer announcement or event page. Include a short note on what makes the event community-oriented when that is not obvious. Mark missing times as “nenurodyta”; distinguish confirmed free entry from voluntary donations, registration requirements, and unconfirmed cost. End with a brief note that these are additional discoveries beyond the main city-events list when that list is available.

## Quality check

Before responding, confirm that every listed item:

- Is in Vilnius (or clearly identified as an eligible public online event organized by a Vilnius group) and within the stated date range.
- Is open to the public and explicitly confirmed as free or clearly free of required payment.
- Has a direct, credible source supporting its date, location, organizer, and cost status.
- Is not a duplicate of the city-events list already shown.
- Clearly marks registration, voluntary donations, restrictions, and unknown details when relevant.

Do not register the user, contact organizers, or make bookings or purchases.
