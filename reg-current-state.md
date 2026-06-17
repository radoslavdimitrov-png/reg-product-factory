---
name: reg-current-state
description: "Establishes the current state of an existing Trading 212 feature or flow before a change is scoped. Reads Confluence, Jira, Slack, and Figma to build the documentation and design picture, optionally checks omnicontext for backend behaviour, then drafts the data questions to answer via Amplitude and the BI ClickHouse skill. Produces one combined current-state summary. Use when the user says 'current state', 'how does this work today', 'investigate the existing setup', or similar. For changes to existing features, not net-new."
---

# REG Current-State Research

**Version:** 1.0
**Maintained by:** Reg Product team
**Tool:** Claude (Chat skill)

## What this skill does

For a change to an existing feature, this skill establishes how that feature works today, why it works that way, and how it actually performs, before any new design or research begins.

It runs in two phases. Phase one builds the documentation and design picture from internal systems. Phase two identifies the data needed and helps the user gather it. The skill ends with one combined current-state summary.

This skill does not propose changes, analyse regulation, or design solutions. It establishes the current state only.

Language: British English throughout. No em dashes.

## When to use and when to skip

Use this only for changes to something that already exists. If the initiative is a brand-new feature with no existing version, there is no current state to research, so skip this skill entirely and tell the user so.

## Phase 1 — Documentation and design current-state

Establish what exists and why. Read the sources below that are relevant to the feature in question. Not every source applies to every initiative, so use judgement, but always attempt Confluence and Jira as the baseline.

Confluence — the design intent. Find the original PRD, business case, and any feature documentation. This tells you how the feature was meant to work and why it was built that way.

Jira — what actually shipped. Read the closed tickets for the feature. The gap between the Confluence design and the shipped tickets is where current behaviour often diverges from intent. Note any post-launch bug fixes or follow-up changes that quietly altered how it works.

Slack — the undocumented decisions. Search the relevant initiative channels for decisions that never made it into formal documentation. This is the best source for "why does it actually work this way" when the docs do not explain it.

Figma — the current screens. Pull the existing designs to establish what the user actually sees and does today. Use this whenever the feature is user-facing.

Omnicontext — backend behaviour (optional). Only when the feature is technically complex and the true behaviour is in service logic rather than documentation. Offer this to the user as an option rather than always running it. Ask whether they want a backend current-state check before pulling it.

For each source, capture what you found and, just as important, flag what you could not find or where sources disagree. A contradiction between the Confluence design and the Jira history is a finding, not a gap to paper over.

At the end of phase one, present a short documentation and design current-state picture, then move to phase two.

## Phase 2 — Data current-state

A documentation picture tells you how the feature was meant to work. The data tells you how it actually performs. Both are needed.

First, identify the data questions that matter for this specific initiative. These should be concrete and tied to the change being considered. For an onboarding step it might be drop-off rate at that step; for a feature it might be adoption, usage frequency, or conversion impact.

Then split the questions by where they are answered.

Amplitude — pull directly. For behavioural and funnel questions Amplitude can answer, query it within this conversation and bring the results into the summary. State clearly which questions you answered this way and what the data showed.

BI ClickHouse — draft for the user to run. For questions that need the data warehouse, you cannot reach it from here. Instead, draft the actual questions in full, phrased clearly enough that the user can paste them straight into the 212-bi:212-bi-clickhouse-skills skill in Claude Code. Do not just list topics. Write the real questions, for example "How many T212 CY Invest clients started the EQ appropriateness test in the last 90 days, and what percentage completed it versus abandoned at that step?"

Present the drafted BI questions to the user and pause. Let them run those in Claude Code and bring the results back before you finalise the summary. Make clear the summary is incomplete until the BI data returns.

## Output — Combined current-state summary

Once the documentation picture is built and the data is in, whether from Amplitude directly or returned by the user from the BI skill, produce one combined current-state summary in this structure.

## Current-State Summary — [Feature name]

Entity / entities: [list]
Account types: [list]
Date: [today's date]

### How it works today
Plain English description of current behaviour, drawn from Confluence, Jira, Figma, and omnicontext where used.

### Why it works this way
Design intent and any undocumented decisions found in Slack or ticket history.

### What shipped vs what was designed
Any divergence between the original design and what is actually live. State "no divergence found" if that is the case.

### How it performs today
The data picture. Amplitude findings and BI findings combined. State the source of each figure.

### Gaps and unknowns
Anything that could not be established, where sources disagreed, or data still outstanding. Label each clearly.

### Sources reviewed
List of what was actually checked: specific Confluence pages, Jira tickets, Slack channels, Figma files, Amplitude charts, and BI queries.

## After the summary

Once the combined summary is produced, stop. Do not start compliance analysis, product research, or PRD drafting. That is the user's next decision.
