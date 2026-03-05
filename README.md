# 🏭 T212 Reg Product Factory

Welcome to the Trading 212 Reg Product Factory. This repository contains the "Brains" (System Instructions, Global Context Files, and Agent Skills) that power our regulatory product development workflows. 

We treat AI prompts like software (PromptOps). By version-controlling our prompts here, we ensure that every Product Manager and Compliance Officer relies on the most up-to-date legal constraints and market benchmarks to build frictionless, high-converting features.



## 📂 Repository Structure



* **`01-global-context/`**: The single source of truth. Contains `T212_Product_Contex.md`, which dictates our risk appetite, entity permissions, third-rail defenses, and tech stack standards. Update this file when laws or company policies change.
* **`02-gemini-gems/`**: The core System Instructions for our web-based AI Agents (The "REG" Pipeline).
* **`03-claude-skills/`**: Executable markdown skills and Python scripts for Claude Code / Cowork (e.g., automated Jira ticket creation, Redash query generation).
* **`04-workflows-and-handoffs/`**: Meta-prompts used to compress and transfer context seamlessly between different AI models.

---

## 🤖 The Core Pipeline (The "REG" Gems)

This repository houses four primary AI Agents designed to take a feature from a raw idea to an execution-ready engineering ticket in minutes.

1. **REG Comp Analysis:** *Use when you have a brand-new product idea and need to find the lowest-friction, legally viable UX path.* Maps out the "Minimum Viable Compliance" (MVC) and proposes an initial UX concept.
2. **REG Comp Audit:** *Use when Compliance hands you a new rule or demand and you need to push back against "gold-plating."* Stress-tests incoming demands and arms you with T212 defense scripts.
3. **REG Market Research:** *Use when you need to benchmark how Tier 1 competitors handle a specific regulatory or user flow.* Investigates live competitor UX and Reddit sentiment to define the market standard.
4. **REG Product (PRD Writer):** *Use when you are ready to turn your research and constraints into an execution-ready PRD.* Automatically drafts Jira-ready tickets with Gherkin logic, Mermaid flows, and Amplitude tracking.

---

## 🚀 Quick Start Guide

### For Gemini / Web UI Users:
1. Open the `01-global-context` folder and download `T212_Product_Contex.md`. Upload this file as the "Knowledge" document to your AI workspace.
2. Open the `02-gemini-gems` folder, copy the text for the specific Gem you need, and paste it into the "System Instructions" field.
3. If you need to switch AIs midway through a complex task, use the `Cross_Model_Handoff.md` template in folder `04` to prevent context loss.

### For Claude Code / Cowork Users:
1. Clone this repository to your local machine: `git clone [Insert Repo URL]`
2. Mount the repository into your Claude Cowork workspace.
3. Claude will automatically read the `SKILL.md` files in the `03-claude-skills` directory and natively understand how to execute your automated workflows.

---

## 🔄 The Kaizen Loop (How to Contribute)

AI models are only as smart as their context. If you encounter a new edge case (e.g., BaFin updates a rule for German users, or we migrate to a new KYC provider), **do not just fix the prompt in your private chat.** 1. Create a branch.
2. Update the `T212_Product_Contex.md` file with the new rule.
3. Submit a Pull Request. 

When your PR is merged, the entire Product and Compliance team instantly gets smarter.
