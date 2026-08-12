# Tableland Copilot for Grok

Your AI-powered business assistant. It guides you step by step through building a complete business foundation, then runs alongside you for daily operations.

Built by [Tableland Partners](https://tablelandpartners.com) for AI Essentials Roundtable members.

**Current release: v7.5-GROK (August 12, 2026)**

> Running Claude instead? The Claude edition lives at [tableland-partners-copilot](https://github.com/jsd4026/tableland-partners-copilot). The two editions share version numbers and stay in sync.

---

## What It Does

Ten conversations, each with a job. Four checkpoints keep you honest about progress.

| # | Conversation | What it produces |
|---|---|---|
| 0 | Copilot Setup | Discovery. The Copilot learns your business |
| 1 | Strategic Planning | 11 foundation documents (business model, financials, personas, brand, legal templates) |
| 2 | Go-to-Market Strategy | 5 documents (GTM strategy, tech plan, campaign and social calendars) |
| 3 | Technical Infrastructure | Verified setup guides for the tools you actually need |
| 4 | Customer Experience | Onboarding playbook, proposal tracker, content standards |
| 5 | Content Creation | Blogs, social, email, decks, plus full campaign atomization |
| 6 | Proposals and Agreements | Custom proposals and SOWs from your own templates |
| 7 | Prospecting | Qualified leads with verified contact info |
| 8 | Receipt Capture | Expense tracking from receipt photos |
| 9 | Field Support | Technical support agent for field employees |

Setup takes 2 to 4 weeks at your own pace. Conversations 5 through 9 are ongoing tools you keep using afterward.

---

## Requirements

**Grok plan:** SuperGrok ($30/month) or X Premium+, running Grok 4.3 or newer. Document generation (PDFs, spreadsheets, slides) ships with Grok 4.3 on these tiers. SuperGrok Heavy also works and adds higher limits.

**Grok Memory:** turn it on. It lets the Copilot carry decisions across conversations without you repeating yourself.

**A Grok Workspace.** Workspaces are Grok's project containers, each with its own files, custom instructions, and conversation history. Newer builds label them Workspaces; older ones say Projects. Same thing.

---

## Setup

**Step 1. Create your Workspace.**
Open Workspaces in the left sidebar at [grok.com](https://grok.com), create a new one, and name it `[Your Business Name] - Tableland Copilot`.

**Step 2. Add the Setup Mode Instructions.**
Open [`docs/Setup-Mode-Instructions.md`](docs/Setup-Mode-Instructions.md). Copy everything inside the gray box, then paste it into your workspace settings under Custom Instructions and save.

**Step 3. Attach the Guide.**
Download [`docs/Guide.md`](docs/Guide.md) and upload it to your workspace's Files tab. This is the backup copy. Your Copilot fetches the latest version from this repo automatically at the start of every conversation, so the attached file only gets used if that fetch fails.

**Step 4. Start Conversation 0.**
Open a new conversation in the workspace, then paste the prompt from [`docs/conversation-0-prompt.md`](docs/conversation-0-prompt.md). The Copilot will ask you to rename the conversation, then begin discovery.

That's it. From there the Copilot hands you each next prompt as you finish a phase.

> **One gotcha worth knowing:** Grok applies custom instruction changes to new conversations only. If you edit them mid session, start a fresh conversation before judging the result.

---

## After Setup

Once all 4 checkpoints are met, swap Setup Mode for Operational Mode. Copy the contents of [`docs/Operational-Mode-Instructions.md`](docs/Operational-Mode-Instructions.md) and replace your Setup Mode text in Custom Instructions.

The Copilot shifts from "build your business" to "run your business." Your execution conversations are ready for daily use.

---

## Repo Contents

| File | Version | Purpose |
|---|---|---|
| [`docs/Guide.md`](docs/Guide.md) | v7.5-GROK | The brain. Every prompt, phase, checkpoint, and standard |
| [`docs/Setup-Mode-Instructions.md`](docs/Setup-Mode-Instructions.md) | v3.2-GROK | Custom Instructions for the build phase |
| [`docs/Operational-Mode-Instructions.md`](docs/Operational-Mode-Instructions.md) | v3.3-GROK | Custom Instructions for daily operations |
| [`docs/conversation-0-prompt.md`](docs/conversation-0-prompt.md) | v7.5-GROK | Your starting prompt |

---

## What Changed in v7.5-GROK

- Aligned to the Claude edition's version numbering. Both platforms now ship v7.5 Guides together.
- **Plan requirement dropped from $300/month to $30/month.** Document generation now ships with Grok 4.3 on standard tiers, so SuperGrok Heavy is no longer required.
- **Renaming got less annoying.** Conversation 0 still waits for you to rename before continuing. Conversations 1 through 9 ask once, then get to work.
- **Faster routine work.** A single quick output no longer triggers the full nine-step file workflow. That stays reserved for foundation and template documents.
- Added the Chat Continuity Protocol. When a conversation fills up, the Copilot writes a context summary and names the follow-up conversation `5b`, `5c`, and so on, so your workspace stays organized.
- Guide retrieval hardened with an authenticity check and date-based comparison.
- Model update notifications now happen only when you ask.
- Fixed several duplicated sections in the content atomization workflow.

---

## FAQ

**Does the Copilot update automatically?**
Yes, for the Guide. Your Custom Instructions tell the Copilot to fetch the latest Guide from this repo at the start of every conversation. When we publish improvements, you get them on your next new conversation.

The two instruction files are different. Those live in your Custom Instructions field, so they only change when you paste in a new version. We email members when that happens.

**Do I need a GitHub account?**
No. Every link here opens in a browser and you copy from the page.

**Grok down, or want a second opinion?**
Say "Switch to Claude" in any conversation and the Copilot will point you to the Claude edition. A paid Claude plan is required.

**Why does it keep asking me questions before writing a document?**
By design. The Copilot asks 3 to 7 focused questions before drafting anything substantial, because documents built on assumptions are worse than documents built on facts. If you're in a hurry, say "just draft it" and it will proceed, flagging every assumption inline so you can correct them.

**Can I fork this and modify it?**
Roundtable members are welcome to adapt it for their own business. It is not licensed for resale or redistribution.

**Something isn't working.**
Say "I need Jeff's help" in any conversation. The Copilot will draft a support email with your context attached. Or email [jeff@tablelandpartners.com](mailto:jeff@tablelandpartners.com) directly.

---

## Support

**Jeffrey Daniels, Tableland Partners**
[jeff@tablelandpartners.com](mailto:jeff@tablelandpartners.com)

Available for custom development, implementation support, and strategic consulting.

- Tech Stack Setup
- Custom Development
- Strategic Consulting
- Done-For-You Implementation
- Fractional CMO

---

© 2026 Tableland Partners, LLC
