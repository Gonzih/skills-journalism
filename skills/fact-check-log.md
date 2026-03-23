---
name: fact-check-log
description: Create a structured fact-checking log for a draft article. Paste in the article text and get a line-by-line checklist of claims requiring verification, with source suggestions.
---

Analyze the provided article draft and produce a structured fact-checking log.

For the article text provided, identify every claim that requires independent verification and organize them into the following log format:

---

**FACT-CHECK LOG**
Article: [title or slug if provided]
Date prepared: [today's date]
Checker: [leave blank for journalist to fill]

---

For each checkable claim, produce a log entry:

**Claim #[N]**
- **Text:** Exact quote or paraphrase of the claim as it appears in the draft
- **Location:** Paragraph number or section
- **Claim type:** Statistical / Attribution / Historical / Legal / Scientific / Biographical / Geographic / Other
- **Verification status:** [ ] Unverified / [x] Verified / [!] Disputed / [~] Approximation acceptable
- **Recommended primary source:** The most authoritative source to confirm this (e.g., "CDC WONDER database", "SEC filing", "on-record quote from named source")
- **Fallback sources:** 1–2 secondary sources if primary is unavailable
- **Risk level:** High (if wrong, causes legal, reputational, or factual harm) / Medium / Low
- **Notes:** Any context — conflicting sources, known areas of dispute, caveats to add if claim can only be partially verified

---

After all claims, add:

**SUMMARY TABLE**
| # | Claim (short) | Type | Risk | Status |
|---|--------------|------|------|--------|
(populate for all claims)

**HIGH-PRIORITY FLAGS:** List any claims that are High risk and currently Unverified. These must be resolved before publication.

**ATTRIBUTION AUDIT:** List every named source in the piece. For each, note whether they are quoted on-record, on background, or anonymously, and flag any anonymous claims that carry significant weight without named corroboration.

Be exhaustive — include numbers, dates, names, titles, organizational affiliations, historical events, scientific claims, and legal characterizations. Do not skip claims that seem obvious; obvious errors are the ones that slip through.

## Live Data Sources

Use these sources for claim verification:

- **PolitiFact RSS feed** (`politifact.com/rss/all`): Query for prior rulings on similar political claims. If a claim matches a previously rated statement, cite the ruling and note any context differences that may change the rating.
- **Snopes API patterns** (`snopes.com`): Search by claim keyword via the site's search endpoint. Useful for viral misinformation, historical myths, and recurring false narratives that resurface in news cycles.
- **OpenSecrets** (`opensecrets.org`): Authoritative source for political finance claims — candidate fundraising totals, PAC donors, lobbying expenditures, and revolving-door employment. Required for any claim about political money or influence.
- **FactCheck.org** (`factcheck.org`): Nonpartisan fact-checking for statements by U.S. political figures. Cross-reference against PolitiFact to identify consensus verdicts vs. disputed ratings.
