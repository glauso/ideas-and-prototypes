---
name: feature-brief-generator
description: Turn a rough, one-line feature idea into a structured, backlog-ready product brief — user stories, acceptance criteria, edge cases, and a success metric. Use this skill whenever someone describes a feature, capability, or product idea, however vague or casually phrased (a hallway ask, a Slack one-liner, a sticky note), and wants it shaped into something a team could actually pick up. Trigger it for requests like "turn this into user stories," "write up this feature," "draft a brief/spec for X," "what would acceptance criteria look like for…," or any time a Product Owner or PM needs a fuzzy idea turned into a spec — even if the word "brief" is never used.
---

# Feature Brief Generator

A Product Owner's first move when an idea arrives is to give it shape: who is it for, what problem does it solve, what does "done" look like, and how will we know it worked. This skill does that first draft. The goal is not a finished specification — it's a clean, specific starting point that a team could discuss, refine, and pull into a backlog.

## When to use this

Use it the moment a feature idea shows up in rough form. Ideas rarely arrive as specs; they arrive as "can we let people save stuff for later?" The value of this skill is turning that sentence into structure quickly, without losing the original intent.

Do **not** use it for ideas that are already fully specified, for pure bug reports, or for questions that aren't about building something (e.g. "how is feature X performing?"). Those need different work.

## What to produce

Always return the brief in this exact structure. Keep every line tight and specific — vague filler is the main failure mode of a brief, so prefer one concrete sentence over three hedged ones.

```
# [Feature name — crisp and polished, not a restatement of the input]

## The problem
[1–2 sentences on the real user problem this solves. Name the user, name the pain.]

## User stories
[2–3 stories, each in the form below]
- As a [specific role], I want [goal], so that [benefit].
  Acceptance criteria:
  - [criterion 1 — testable, not aspirational]
  - [criterion 2]
  - [criterion 3 — optional]

## Edge cases to consider
- [edge case 1 — the awkward states a developer will hit]
- [edge case 2]
- [edge case 3]

## How we'll know it worked
[One measurable success metric. A number or a clear signal, not "users are happy."]

## Effort
[S, M, or L — a rough t-shirt size, with half a sentence of why.]
```

## Quality bar

- **Be specific.** "As a user, I want the feature to work" is useless. Name the actual role and the actual goal. Specificity is what separates a real brief from a generated-looking one.
- **Acceptance criteria must be testable.** Someone should be able to read each one and say yes/no whether it's met. "Loads fast" fails; "results appear within 2 seconds" passes.
- **Edge cases earn their place.** Surface the states a developer will actually hit — empty states, conflicts, permissions, offline, the item that no longer exists. Skip the obvious.
- **One metric, chosen well.** Resist listing five. Pick the single signal that would tell a PO this feature did its job.
- **Preserve intent.** Polish the framing, but don't quietly redesign the idea into something the person didn't ask for.

## Example

**Input:** "Let users save articles to read later"

**Output:**

```
# Read-It-Later

## The problem
Readers often find a good article at a bad time — mid-commute, between meetings — and lose it before they can read it. They need a way to set it aside and come back without hunting through history.

## User stories
- As a reader, I want to save an article with one tap, so that I can return to it later without copying links.
  Acceptance criteria:
  - A save control is visible on every article view.
  - Saving gives immediate visual confirmation.
  - A saved article appears in the reading list within 1 second.
- As a reader, I want a dedicated list of saved articles, so that I can find them in one place.
  Acceptance criteria:
  - The list shows title, source, and date saved.
  - Articles can be removed from the list.
  - The list persists across sessions and devices.

## Edge cases to consider
- The article is edited or deleted after being saved.
- The same article is saved twice.
- The user is offline when they tap save.

## How we'll know it worked
At least 20% of weekly active readers save one or more articles, and a third of saved articles are opened within 7 days.

## Effort
M — straightforward UI, but cross-device sync and the offline case add real work.
```

## Tone

Write the way a sharp Product Owner talks: plain, concrete, and confident. No buzzwords, no "leverage synergies," no apology. The brief should read like something a person would be glad to find waiting in their inbox.
