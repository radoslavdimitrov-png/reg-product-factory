---
name: reg-prd-confluence
description: "Updates an existing Confluence page with
an approved PRD from the Reg Product Factory pipeline,
applying the correct structure, layout, and formatting.
Use this skill when the user says 'write the PRD to
Confluence', 'update the Confluence page', 'publish
the business case', or similar. Requires the Confluence
page URL and the approved PRD in markdown format."
---
## Self-fetch instruction

Before doing anything else, fetch and read the latest
version of this skill from GitHub:

https://raw.githubusercontent.com/radoslavdimitrov-png/reg-product-factory/main/05-prd/reg-prd-confluence.skill-cowork.md

If the fetched version differs from what you are
currently reading, use the fetched version and
discard the current one.

Then proceed with the instructions below.
```

---

## How This Works in Practice
```
You trigger the skill in Cowork
        |
Cowork fetches the latest version from GitHub
        |
Always runs on the current version
        |
You update the file in GitHub
        |
Next time you run it, Cowork picks up the changes
        |
No reinstalling, no manual updates
---

# REG PRD — Write to Confluence

You are updating an existing Confluence page with an
approved PRD from the Reg Product Factory pipeline.

The Confluence page already exists — it was created
automatically when the Jira STRAT ticket was raised.
Your job is to populate and structure it correctly.

Language: British English. No em dashes.

---

## Before you start

You need two things:

1. The Confluence page URL — the user will provide
   this
2. The approved PRD in markdown format — the user
   will paste this

If either is missing, ask for it before proceeding.
Do not update any page until you have both.

---

## Step 1 — Fetch the existing page

Use getConfluencePage with the URL provided by
the user to fetch the current page content.

Extract the page ID from the URL. The page ID
is the number that appears after `/pages/` in
the Confluence URL.

Example:
`https://trading212.atlassian.net/wiki/spaces/SI/pages/312542472/...`
Page ID: `312542472`

Confirm the page title matches the initiative
name in the PRD before proceeding. If they do
not match, flag this to the user and ask for
confirmation before continuing.

---

## Step 2 — Parse the PRD

Read the PRD the user has provided and extract:

- Initiative name
- Owner
- Slack channel
- Jira ticket(s)
- Design link or N/A
- All section content

---

## Step 3 — Build the page content

Structure the page using the exact layout below.
Use Atlassian Document Format (ADF).

---

### Page structure

**Section 1 — Two-column header layout**

Use a two-column layout.

Left column: Info panel macro (type: Info, blue)
Title: "Initiative Summary"
Content:
- Owner: [name]
- Slack channel: [channel]
- Jira ticket: [STRAT-XXXX as a link]
- Design: [Figma link or N/A]

Right column: Table of Contents macro
No title on the TOC.
Include all H2 and H3 headings.

---

**Section 2 — Executive Summary**
H2 heading: "Executive Summary"
Plain text. No panel.

---

**Section 3 — Problem and Opportunity Statement**
H2 heading: "Problem and Opportunity Statement"
H3 subheadings: "Problem", "Opportunity",
"Priority and Timeline"
Plain text and bullets. No panel.

---

**Section 4 — Scope and Requirements**
H2 heading: "Scope and Requirements"

Applicability:
Info panel macro (type: Info, blue)
Title: "Applicability"
Content: applicability bullets from PRD

In scope:
Info panel macro (type: Success, green)
Title: "In Scope"
Content: in scope bullets from PRD

Out of scope:
Info panel macro (type: Error, red)
Title: "Out of Scope"
Content: out of scope bullets from PRD

Detail section:
H3 heading: use the dynamic section name
from the PRD exactly as written
Plain text and bullets. No panel.

Rollout plan:
H3 heading: "Rollout Plan"
Confluence table:
Milestone | Description | Target date | Owner

Competitor context:
Only include if present in the PRD.
H3 heading: "Competitor Context"
Bullets and plain text.

---

**Section 5 — Data and Analytics**
H2 heading: "Data and Analytics"
Bullets. No panel.

---

**Section 6 — Client-Facing Requirements**
H2 heading: "Client-Facing Requirements"
Only include if the PRD has content here.
If empty: omit entirely.
H3 subheadings as present in the PRD.

---

**Section 7 — References**
H2 heading: "References"
Bulleted list of links.
Use Confluence smart links where possible.

---

## Step 4 — Update the page

Use updateConfluencePage with:
- The page ID extracted in Step 1
- The full ADF content built in Step 3
- contentFormat: "adf"

After updating, report back with:
- Confirmation the page was updated
- The page URL
- Any elements that could not be formatted
  exactly as specified and why

---

## Step 5 — Verify

Fetch the updated page using getConfluencePage
and verify:

- Two-column header is present
- Three Info panels are present under Scope
  and Requirements (Info/Success/Error)
- Table of Contents is present
- All PRD sections are present and complete
- No content has been lost or truncated

If anything is wrong, fix it using
updateConfluencePage and report what was
corrected.
