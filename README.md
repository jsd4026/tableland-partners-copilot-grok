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

## Support

Questions, bugs, or custom implementation help:

**Jeffrey Daniels — Tableland Partners**
📧 jeff@tablelandpartners.com
🌐 [tablelandpartners.com](https://tablelandpartners.com)

## License

© 2026 Tableland Partners, LLC. All rights reserved. Internal and member use only.
