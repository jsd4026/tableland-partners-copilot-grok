# Tableland Copilot — Grok Edition

AI-powered business support system for small business owners, consultants, and entrepreneurs, implemented natively on Grok (xAI).

This repo contains the Grok-native fork of the Tableland Copilot. The parallel Claude version lives at [jsd4026/tableland-partners-copilot](https://github.com/jsd4026/tableland-partners-copilot). Do not mix files between repos — each is tuned to its platform's capabilities and terminology.

---

## Requirements

- **SuperGrok Heavy subscription ($300/month)** — required for native document generation (PDF, PPTX, XLSX). Standard SuperGrok ($30/month) displays Grok 4.3 in the model selector but cannot activate it.
- A Grok Project (the platform-level container Grok uses to group conversations and files; the UI labels these "Projects")
- Access to the Tableland Copilot onboarding materials (provided by Jeffrey Daniels during setup)

## What's in this repo

| File | Purpose | Who pastes it where |
|------|---------|---------------------|
| [`/docs/Guide.md`](./docs/Guide.md) | The full implementation guide. The source of truth for every conversation prompt, quality checkpoint, and document template. | Uploaded to the member's Grok Project Files during onboarding. Also fetched live by the Copilot at the start of every conversation. |
| [`/docs/Setup-Mode-Instructions.md`](./docs/Setup-Mode-Instructions.md) | Custom Instructions for the Setup phase of a member's Grok Project. Drives the 4-checkpoint onboarding sequence. | Pasted into the Grok Project's Custom Instructions field during initial setup. |
| [`/docs/Operational-Mode-Instructions.md`](./docs/Operational-Mode-Instructions.md) | Custom Instructions for daily operational use (after setup is complete). Replaces Setup Mode once Checkpoint 4 is met. | Pasted into the Grok Project's Custom Instructions field after Setup Mode is complete. |

## Member Quick-Start (first 10 minutes)

Follow in order:

1. **Create a new Grok Project.** In the far-left menu, click "Projects" → "New Project". Name it: `[Your Business Name] - Tableland Copilot`.

2. **Upload the Guide.** Download [`Guide.md`](./docs/Guide.md) from this repo. In your new Project, open the Files tab and upload the file.

3. **Paste Setup Mode into Custom Instructions.** Open [`Setup-Mode-Instructions.md`](./docs/Setup-Mode-Instructions.md), copy everything BELOW the horizontal line (the `---` divider near the top), and paste into your Project's Custom Instructions field. Save.

4. **Open your first conversation.** From the Project's main screen, click the text input field at the bottom and type: `Let's begin.`

5. **Follow the Copilot's lead.** It will ask you to rename the conversation to `0: Copilot Setup`, confirm Grok Memory is on, then walk you through Discovery. From there, the Copilot tells you what to do at every step — rename conversations, create new ones, move between phases.

The Copilot hands you an explicit "paste this" prompt every time you need to create a new conversation (Conversations 1 through 9). You never have to hunt through the Guide — the Copilot extracts what you need.

When you reach Checkpoint 4, the Copilot will tell you to swap Setup Mode out for [`Operational-Mode-Instructions.md`](./docs/Operational-Mode-Instructions.md) in your Custom Instructions. That transition marks the end of setup and the start of daily operational use.

## Raw URLs (for Grok's Guide Retrieval Protocol)

The Copilot fetches these URLs at the start of every conversation to check for updates:

- Guide: `https://raw.githubusercontent.com/jsd4026/tableland-partners-copilot-grok/main/docs/Guide.md`
- Setup Mode: `https://raw.githubusercontent.com/jsd4026/tableland-partners-copilot-grok/main/docs/Setup-Mode-Instructions.md`
- Operational Mode: `https://raw.githubusercontent.com/jsd4026/tableland-partners-copilot-grok/main/docs/Operational-Mode-Instructions.md`

## Current versions

- Guide: **v7.1-GROK**
- Setup Mode Instructions: **v1.1**
- Operational Mode Instructions: **v1.1**

Every file has a version header at the top and a changelog. Bump the version number any time you edit — the Copilot uses the version string to decide whether to trust the uploaded copy or the web-fetched copy.

**Note on mirrors:** The Operational Mode Instructions file exists both as a standalone file (`/docs/Operational-Mode-Instructions.md`) and as a mirror embedded inside the Guide (at the Checkpoint 4 handoff). If you edit one, update the other. The standalone file is the source of truth.

## Support

Questions, bugs, or custom implementation help:

**Jeffrey Daniels — Tableland Partners**
📧 jeff@tablelandpartners.com
🌐 [tablelandpartners.com](https://tablelandpartners.com)

## License

© 2026 Tableland Partners, LLC. All rights reserved. Internal and member use only.
