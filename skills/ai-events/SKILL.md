---
name: ai-events
description: Research and summarize AI news and product updates published in the current calendar month, whenever the user asks for the latest AI developments, this month's AI news, new AI tools/models/features, or independent reactions to official AI announcements. Pair primary announcements from AI labs and technology companies with independent hands-on tests, expert commentary, bug reports, and positive or negative user experiences. Use this skill even when the user says “what's new in AI?” without naming a month.
---

# AI Events — Current-Month AI News and Independent Reviews

## Goal

Produce a reliable, balanced overview of noteworthy AI news from the **current calendar month**, pairing official announcements with independent analysis of how the announced products or capabilities behave in practice. The useful question is not only “what did the company announce?” but also “what happened when other people tried it?”

## Workflow

### 1. Define the time window

- Resolve the current date and the local date relevant to the user. State the exact month and year being covered.
- Default to the first through the current date of the current calendar month. Do not silently use the last 30 days or the previous month.
- Prioritize announcements, releases, updates, and independent tests published in this month.
- An older official announcement may be included only if a meaningful hands-on test, bug report, correction, or follow-up appeared this month. Label the original announcement date and the newer review date separately.
- If the user specifies a different month or date range, follow that scope instead.

### 2. Search across a broad but relevant set of AI topics

Search multiple categories so the roundup does not become a single-company news feed. Select the categories with meaningful developments this month:

- New foundation models, reasoning models, multimodal models, and model/API releases.
- AI assistants, agent features, coding tools, developer platforms, and productivity tools.
- Image, video, audio, speech, search, and creative-generation tools.
- Open-source models, weights, benchmarks, and developer frameworks.
- Enterprise, cloud, hardware, robotics, and AI infrastructure.
- Safety, security, privacy, reliability, evaluations, copyright, regulation, and major research findings.

Search official sources and independent sources separately. Use varied queries for announcements, release notes, changelogs, hands-on tests, limitations, bugs, benchmarks, and user feedback. Search current reporting from company blogs and documentation, research labs, reputable technology publications, independent reviewers, developer blogs, GitHub issues, forums, and public posts where accessible.

### 3. Establish the official facts first

For each candidate story, look for the most direct primary source available, such as:

- The maker's official announcement or blog.
- Release notes, product documentation, model cards, API documentation, or changelog.
- A research paper or official evaluation report.
- An official repository or issue tracker.

Record the publication date, product/model name, what changed, who can access it, and any stated limitations, rollout restrictions, pricing, or availability. Distinguish a research preview, waitlist, limited rollout, beta, and general availability. Do not describe a feature as generally available unless the source supports that claim.

Treat official performance claims as claims from the publisher, not independently established facts. Check whether benchmarks have disclosed methodology, comparison models, prompting, compute, and other relevant conditions when that information is available.

### 4. Find independent real-world reactions

For every major official update, search for credible independent analysis published after or around the announcement. Prefer sources where the author explains what they actually tried and shows enough evidence to understand the result:

- Hands-on reviews, demonstrations, walkthroughs, and side-by-side comparisons.
- Developers' experiments, reproducible prompts, code, benchmark results, and repository issues.
- Expert commentary that identifies strengths, weaknesses, or implications.
- Reports of failures, regressions, hallucinations, safety gaps, privacy concerns, latency, cost, or confusing behavior.
- Positive reports showing that a feature works reliably or meaningfully improves a workflow.

Use original posts and test reports when possible rather than summaries of summaries. A public post from an individual can be valuable, but identify it as an individual experience, not a representative study. For social posts, forums, and GitHub discussions, confirm the author, date, context, and whether the claim is supported by reproducible evidence or merely anecdotal.

Do not equate “independent” with automatically correct. Prefer multiple independent reports for consequential claims. If evidence is thin or conflicting, say so. Look for sponsorship, affiliate links, access provided under embargo, or other disclosed conflicts when visible; do not infer undisclosed conflicts.

### 5. Match reactions to the exact update

Connect the official announcement and independent reactions only when they concern the same product, model version, feature, or clearly identified comparison. Check release dates and version numbers carefully.

For each notable update, seek at least one independent hands-on reaction. For the most important or disputed stories, seek more than one perspective, including both praise and criticism where available. Do not force a negative/positive balance if evidence does not support it. If no credible independent test can be found, say **“Nepriklausomo praktinio vertinimo rasti nepavyko”** and do not invent one.

Separate these evidence types:
- **Official fact:** directly supported by the publisher or primary documentation.
- **Independent observation:** what a reviewer or tester says they observed.
- **Interpretation:** the skill's synthesis of the evidence.
- **Unverified claim:** a claim for which evidence is insufficient or contradictory.

Do not describe a vulnerability as confirmed solely because a commenter calls it a “security hole.” State what was demonstrated, what the potential impact is, and whether the vendor or another source has confirmed it. Avoid reproducing exploit steps that would enable abuse; summarize the issue safely.

### 6. Verify dates, links, and significance

- Open the original pages and verify the publication date and relevant details before including a story.
- Prefer primary sources for official facts and direct links to the independent review or test.
- Do not rely on search-result snippets alone when the page can be opened.
- Exclude old or recycled stories unless there is a substantive update this month.
- Avoid duplicate coverage of the same release. Combine reports when they cover one underlying development.
- Prefer consequential and actionable developments over minor marketing announcements.
- If sources disagree, describe the disagreement and link both sides.
- Never invent dates, prices, model capabilities, access conditions, benchmarks, or test results.

### 7. Rank and summarize

Normally return 5–10 stories if enough well-supported developments exist. Return fewer rather than pad the list. Prioritize a mix of companies and topics, practical user impact, novelty, independent test quality, and whether the update is accessible now.

Write in the user's language; if no language preference is evident, use the language of the request. Use concise explanations and avoid hype.

## Output format

Start with a heading such as:

# AI naujienos — [mėnuo, metai]
**Apžvalgos laikotarpis:** [exact start date]–[as-of date]

For each story, provide:

1. **News / product update** — name and one- or two-sentence summary.
2. **Official announcement** — publication date, what was announced, availability/access, and direct primary-source link.
3. **What independent testers say** — the author's name or channel when available, publication date, what they tested, and direct link.
4. **What worked well** — concrete positive observations, if supported.
5. **Problems or limitations** — concrete failures, caveats, or open questions, if supported.
6. **Evidence status** — one of: multiple independent tests; one hands-on test; commentary only; official claim not independently verified; conflicting evidence.
7. **Practical takeaway** — who should care and whether it is worth trying now, clearly marked as synthesis rather than fact.

Use a compact table for an overview when it improves scanability, with columns:
**Naujiena | Oficiali informacija | Nepriklausomas testas / komentaras | Kas pasitvirtino / problemos | Prieiga ir šaltiniai**

Follow the table with a short section:
- **Svarbiausios 3 naujienos** — only if the evidence supports ranking.
- **Bendros tendencijos ir neatsakyti klausimai** — separate observations from interpretation.
- **Šaltinių ribotumai** — mention missing hands-on coverage, access restrictions, conflicting reports, or date uncertainties.

Link directly to the relevant official release and independent review. Include publication dates for both. Cite every material claim close to the claim.

## Quality checklist

Before responding, verify:

- [ ] The month and year are explicit, and the time window matches the current calendar month or the user's requested range.
- [ ] Each item is genuinely relevant to AI and has a credible source.
- [ ] Official announcements and independent reactions are distinguishable and directly linked.
- [ ] Independent reports are actually independent where claimed, dated, and tied to the right product/version.
- [ ] Positive findings and bugs/limitations are both represented when evidence exists, without false balance.
- [ ] Marketing claims, individual anecdotes, verified facts, and the skill's interpretation are clearly separated.
- [ ] No dates, prices, availability, test results, or conclusions have been invented.
- [ ] The list prioritizes meaningful developments and avoids duplicate stories.
