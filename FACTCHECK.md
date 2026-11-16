# Fact-check of the blue-bonds session

The transcript stays as it was: its mistakes are part of the record. This file checks the factual claims Claude made in it against primary sources, seven months later. Evan's own statements (including the hackathon result) were not checked.

**Checked 17 November 2026.** 27 claims: 2 wrong, 6 partly right, 2 with no source found, 17 confirmed. Each was judged twice: as of early April 2026, when it was said, and as of today. No verdict differs between the two dates.

Every row in the tables cites a page and a short verbatim quote. [`check_quotes.py`](./check_quotes.py) fetches each page and confirms the quote is still on it (`python3 check_quotes.py FACTCHECK.md`; needs `curl` and `pdftotext`). That proves the quote exists, not that the conclusion drawn from it is right.

This check was done by AI agents too. Three Claude subagents did the first pass, one per topic, and curl-checked their own quotes. The quote checker then re-fetched every source in the tables. GLM-5.3 (a different model family) reviewed the verdicts as a skeptic. Changes that came from it: A6 had cited a June 2026 source for an April 2026 judgment and now cites a 2023 one, the B14 wording now credits Claude's hedge, A6 was moved from wrong to partly right because adoption was never checked, and B12 was moved to confirmed. Treat all of this as a stronger second opinion, not as ground truth.

## What changes the story

Two errors and one overstatement bear on the session's own argument:

- **The "sleeper agent" problem is two papers merged into one** (C1). Line 305 names "the sleeper agent problem" (a model that performs good values only while evaluated, a fair gloss) and in the same sentence adds that training on a narrow task can trigger broad misalignment. By line 326 the two have fused: "the sleeper agent concern" is said to be about training a separate model on a narrow task. The narrow-task finding is the *Emergent Misalignment* paper (Betley et al., 2025). *Sleeper Agents* (Hubinger et al., 2024) is a different result: a deliberately planted backdoor survives safety training. Evan's next turn (line 314) builds on the merged version ("due to the sleeper agent problem … it doesn't make sense to train a model on a narrow task"), and Claude's MoE answer (line 326) accepts that premise. The README lists this thread as "sleeper agents and the MoE-vs-single-model question".
- **Blue-bond frameworks already existed** (A6, partly right). Line 35 says blue bonds have no framework equivalent to green bonds and issuers make up their own definitions. In September 2023 ICMA, IFC, ADB, UNEP FI and the UN Global Compact published a practitioner's guide with a blue-economy typology and eligibility criteria, building on the Green Bond Principles and on earlier blue-specific guidance from UNEP FI and the UN Global Compact. These are voluntary, and how widely issuers follow them was not checked, so "no binding blue taxonomy" would have been fair, and "making up their own definitions" may still describe practice. "No equivalent" was not right. The README's "definitional murkiness" opening rests on the stronger claim.
- **Cursor did have a multi-agent demo** (B14). Evan asked about Claude and Cursor swarm demos. Line 113 said its search found no Cursor demo, which was honest, but then called Claude Code's TeammateTool "the big swarm story in the coding space" and suggested he may have heard about Cursor "in a related context". Cursor's blog had described hundreds of concurrent agents building a web browser on 14 January 2026, almost three months earlier. The search miss was followed by a suggestion that Evan had heard about Cursor in some other context, when he had it right.

The MoE answer that resolved Evan's question (C5) also leans on a claim that holds for Mixtral but not for MoE models in general: OLMoE found experts specialising by data domain.

The README's lesson that Anthropic's position is "closer to corrigible" for now, with autonomy expected to grow (C3), checks out against Anthropic's constitution, published on 21 January 2026, before the session.

## Wrong

| id | line | claim | what the source says | source | quote |
|---|---|---|---|---|---|
| C1 | 326 | "The sleeper agent concern" is about training a separate model on a narrow task (set up at 305) | The narrow-task result is Emergent Misalignment | [arXiv 2502.17424](https://arxiv.org/abs/2502.17424) | "Training on the narrow task of writing insecure code induces broad misalignment." |
| C1 | 326 | (same) | Sleeper Agents is about planted deception persisting through safety training | [arXiv 2401.05566](https://arxiv.org/abs/2401.05566) | "standard techniques could fail to remove such deception and create a false impression of safety" |
| B14 | 113 | Search found no Cursor swarm demo; "the big swarm story in the coding space right now is specifically Claude Code's TeammateTool" | Cursor's 14 Jan 2026 post ran hundreds of agents to build a browser. The search missed it; the claim was hedged, but the framing that followed was wrong | [Cursor blog](https://cursor.com/blog/scaling-agents) | "The agents ran for close to a week, writing over 1 million lines of code across 1,000 files." |
| B14 | 113 | (same) | (same) | [Cursor blog](https://cursor.com/blog/scaling-agents) | "Hundreds of workers run concurrently" |
| B14 | 113 | (same) | (same) | [Cursor blog](https://cursor.com/blog/scaling-agents) | "Jan 14, 2026" |

## Partly right

| id | line | claim | correction | source | quote |
|---|---|---|---|---|---|
| A6 | 35 | Blue bonds have no "equivalent widely-adopted taxonomy"; issuers make up their own definitions | A 2023 multi-institution guide defines a typology and eligibility criteria, so "no equivalent" was wrong; how widely it is adopted was not checked | [IFC, Sept 2023](https://www.ifc.org/en/pressroom/2023/new-guidance-on-blue-bonds-to-help-unlock-finance-for-a-sustainable-ocean-economy) | "Define blue economy typology and eligibility criteria" |
| A6 | 35 | (same) | That guide built on ICMA's Green Bond Principles and on earlier blue-specific guidance from UNEP FI and the UN Global Compact | [IFC, Sept 2023](https://www.ifc.org/en/pressroom/2023/new-guidance-on-blue-bonds-to-help-unlock-finance-for-a-sustainable-ocean-economy) | "draws on pre-existing specific blue guidance" |
| A4 | 22 | It was backed by the World Bank, which de-risked it | The World Bank guaranteed $5M of the $15M; a separate $5M GEF concessional loan also supported it | [Financial Afrik, Nov 2018](https://www.financialafrik.com/en/2018/11/07/seychelles-launches-first-blue-sovereign-bond/) | "partially secured by a USD 5 million World Bank (IBRD) guarantee and supported by a USD 5 million concessional loan from the GEF" |
| B6 | 101 | A CVE was disclosed in late January for a WebSocket hijacking bug allowing RCE | The date is close enough: the fix shipped 29 January and NVD published CVE-2026-25253 on 1 February. NVD describes a token sent over an automatic WebSocket connection; the hijacking/RCE framing comes from secondary reporting | [NVD](https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-25253) | "automatically makes a WebSocket connection without prompting, sending a token value" |
| B8 | 104 | By February 2 Moltbook claimed 1.5 million bots | 1.5M registered agents was Moltbook's own figure; Wiz found about 17,000 human owners behind them. No source pins the 2 February date | [Wiz](https://www.wiz.io/blog/exposed-moltbook-database-reveals-millions-of-api-keys) | "while Moltbook boasted 1.5 million registered agents" |
| B13 | 109 | Anthropic's research team had agents build a C compiler that compiles Linux: ~100,000 lines of Rust in two weeks, almost no human input | Figures are right (16 agents, ~2,000 sessions). One engineer wrote it up, and the post describes a human-built test harness and known gaps, which "almost no human input" glosses | [Anthropic Engineering](https://www.anthropic.com/engineering/building-c-compiler) | "the agent team produced a 100,000-line compiler that can build Linux 6.9" |
| C5 | 324 | An MoE expert is not specialised in a domain; at most it learns word-level syntax | True for Mixtral | [Mixtral, arXiv 2401.04088](https://arxiv.org/pdf/2401.04088) | "we do not observe obvious patterns in the assignment of experts based on the topic" |
| C5 | 324 | (same) | Not for OLMoE (2024), whose experts specialise by data domain, e.g. one is nearly 100% specialised to arXiv text | [OLMoE, arXiv 2409.02060](https://arxiv.org/pdf/2409.02060) | "they specialize in different kinds of data" |

## No source found

The searches found nothing that a fetched page could back. This is not proof the claims are false.

- **A7 (line 26):** blue bonds are niche next to green bonds. Almost certainly true, but the market-size figures turned up only in search snippets (sources gave about $2.5–4.7B of blue issuance for 2024, against green issuance in the hundreds of billions), not on a page fetched for this check.
- **B4 (line 99):** OpenClaw went from 9,000 to over 60,000 GitHub stars "in just a few days". Search summaries carried these numbers, but no fetched page did. Fetched pages give only later totals, such as Computerworld's "over 145,000 GitHub stars in weeks".

**Not looked into:** parts of confirmed rows that the cited source does not cover: TeammateTool's "13 operations" (B11), the list of LLMs OpenClaw works with (B3), and "alignment is trained across the whole model" (C6), which follows from the architecture but was not sourced.

<details>
<summary>Confirmed (17)</summary>

| id | line | claim | source | quote |
|---|---|---|---|---|
| A1 | 21 | The first major blue bond was Seychelles, 2018 (it was the first sovereign one) | [Financial Afrik](https://www.financialafrik.com/en/2018/11/07/seychelles-launches-first-blue-sovereign-bond/) | "launches first blue sovereign bond" |
| A2 | 22 | Seychelles raised $15 million | [Financial Afrik](https://www.financialafrik.com/en/2018/11/07/seychelles-launches-first-blue-sovereign-bond/) | "raised US $ 15 million from international investors" |
| A3 | 22 | For fisheries reform and marine protection | [Financial Afrik](https://www.financialafrik.com/en/2018/11/07/seychelles-launches-first-blue-sovereign-bond/) | "expansion of marine protected areas, improving the governance of priority fisheries" |
| A5 | 35 | The EU Green Bond Standard exists (alongside ICMA's GBP) | [EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32023R2631) | "on European Green Bonds and optional disclosures" |
| B1 | 97 | OpenClaw is by Austrian developer Peter Steinberger | [Wikipedia](https://en.wikipedia.org/wiki/OpenClaw) | "Austrian programmer turned vibe coder Peter Steinberger" |
| B2 | 97 | Clawdbot → Moltbot → OpenClaw after Anthropic's lawyers asked | [Business Today](https://www.businesstoday.in/amp/technology/news/story/the-lobster-sheds-its-shell-for-the-third-time-as-clawdbot-becomes-openclaw-513650-2026-01-30) | "until Anthropic's legal team politely asked us to reconsider" |
| B3 | 97 | Reachable over Signal, Telegram, WhatsApp, Discord | [openclaw.ai](https://openclaw.ai) | "WhatsApp, Telegram, Discord, Slack, Signal" |
| B5 | 99 | Creator joined OpenAI; project to a foundation | [The Register](https://www.theregister.com/2026/02/16/open_ai_grabs_openclaw) | "will live in a foundation as an open source project that OpenAI will continue to support" |
| B7 | 104 | Moltbook, an agent-only forum, launched January 2026 by Matt Schlicht | [Built In](https://builtin.com/articles/what-is-moltbook-openclaw) | "Since its release in January 2026" |
| B9 | 104 | Moderation handed to his bot "Clawd Clawderberg" (Built In says "partly") | [Built In](https://builtin.com/articles/what-is-moltbook-openclaw) | "partly run and moderated by his own bot, Clawd Clawderberg" |
| B10 | 104 | Researchers found exposed databases | [Wiz](https://www.wiz.io/blog/exposed-moltbook-database-reveals-millions-of-api-keys) | "The exposure included 1.5 million API authentication tokens" |
| B11 | 109 | `strings` on Claude Code found TeammateTool, feature-flagged off (third-party reverse engineering) | [paddo.dev](https://paddo.dev/blog/claude-code-hidden-swarm/) | "feature-flagged off" |
| B12 | 109 | Launched as agent teams with Opus 4.6 (as a research preview; today's docs still call it experimental) | [Anthropic, Opus 4.6 launch](https://www.anthropic.com/news/claude-opus-4-6) | "We've introduced agent teams in Claude Code as a research preview." |
| C2 | 292 | Constitutional AI: written principles, self-critique and revision | [arXiv 2212.08073](https://arxiv.org/abs/2212.08073) | "generate self-critiques and revisions, and then finetune the original model on revised responses" |
| C3 | 295 | Neither fully corrigible nor fully autonomous; closer to corrigible for now | [Claude's constitution](https://www.anthropic.com/constitution) | "without being fully corrigible" |
| C3 | 295 | (publication date: before the session) | [Anthropic, Claude's constitution (2023 page)](https://www.anthropic.com/news/claudes-constitution) | "Update, Jan 21, 2026" |
| C4 | 298 | Values as the model's own character, not external constraints | [Claude's constitution](https://www.anthropic.com/constitution) | "rather than seeing them as external constraints imposed upon it" |
| C6 | 324 | MoE experts are sub-networks inside one model | [Mixtral, arXiv 2401.04088](https://arxiv.org/abs/2401.04088) | "each layer is composed of 8 feedforward blocks" |

</details>
