---
name: story-pitch
description: Write a compelling story pitch for editors. Provide a topic, angle, or rough idea and get a polished pitch with headline, summary, news hook, and why-now rationale.
---

Write a compelling story pitch for an editor based on the user's idea or topic.

Structure the pitch as follows:

**Headline:** A sharp, specific working headline (not clickbait — precise and newsworthy).

**The Story in One Sentence:** Distill the story to its single most compelling sentence. This is the lede if you had only one sentence.

**The News Hook:** Why does this story matter *right now*? Tie it to a recent event, trend, or data point. Be specific — vague hooks get rejected.

**The Angle:** What's the fresh perspective or counterintuitive take that makes this story worth telling over the hundred others on this topic? Name the tension, surprise, or revelation at the center.

**Key Characters or Sources:** Who are the 2–3 people central to this story? What makes them the right voices — not just experts, but people with lived stakes in the outcome?

**The Nut Graf:** Two to three sentences that would appear in paragraph 3 of the published piece — the "here's why you should care" passage that contextualizes the specific story within a broader significance.

**Proposed Length and Format:** Suggest a word count and format (breaking news brief, long-form narrative, Q&A, data piece, etc.) appropriate to the story's scope.

**Competing Coverage:** Name one or two existing pieces on this topic and explain specifically how this story goes further, corrects the record, or reaches a different audience.

Use the user's supplied details. If they've given only a vague topic, make reasonable journalistic assumptions and flag them clearly so the reporter can verify. Write in active voice. Be direct. Editors receive dozens of pitches — make every word justify its presence.

## Live Data Sources

Use these sources to ground the pitch in real, current data:

- **NewsAPI** (`newsapi.org/v2/everything`): Query for recent articles on the topic to establish the news hook and competing coverage. Use `sortBy=publishedAt` for recency and `sortBy=relevancy` for depth. Free tier supports 100 requests/day.
- **Google Trends API** (`trends.google.com/trends/api/explore`): Validate that search interest supports the "why now" angle. Rising queries signal audience appetite; declining trends may undercut urgency.
- **Media Cloud** (`mediacloud.org`): Open-source dataset of millions of news stories across outlets. Use to map which publications are covering the topic, identify coverage gaps, and find underreported angles that differentiate this pitch.
