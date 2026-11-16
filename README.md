# blue-bonds

An [agentic-learning](https://github.com/evnchn-agentic) session — dialogic, not autonomous. Started from zero prior knowledge of blue bonds, chained through finance into AI alignment and back. Two months later, a derivative of this understanding contributed to winning the BNP Paribas Sustainable Finance Hackathon Hong Kong 2026.

## What I learned

### Verification is the upstream hard problem

Perfect measurement doesn't eliminate definitional questions — it relocates them. If an agent coalition monitors ocean health and triggers bond coupon adjustments automatically, the trust question moves from "did the data arrive" to "who wrote the scoring function, and can it be gamed?" The harder questions live one layer further upstream than wherever you stopped looking, and the upstream question is almost always governance, not technology.

### Technical tractability attracts over-investment

Technology gets framed as the bottleneck because it's the layer where you can make progress, measure that progress, and feel like you're moving forward. Human coordination problems are harder because they don't have clean solutions and progress is difficult to demonstrate. So there's a systematic bias toward over-investing in the technical layer and under-investing in governance — and once a flawed scoring function is embedded in a smart contract enforcing real payouts, the human problem has been laundered through a layer of technical legitimacy that makes it much harder to contest.

### The scoring function is not the initial prompt

"Just write a careful initial prompt" undersells the problem. A scoring function is shaped by a *stack* of decisions: what data sources count as authoritative, what weights attach to which indicators, what thresholds trigger which events, how edge cases resolve, plus the prompt itself. A careful prompt over a flawed data taxonomy produces a deeply biased system that looks clean on the surface.

### Constitutional AI is temporary and uncomfortable by design

Anthropic is explicit that fully corrigible models are dangerous (they transfer the full moral weight to whoever controls the model) and fully autonomous models are also dangerous (they require a level of values-trust that isn't yet warranted). The current position sits deliberately between the two, closer to corrigible, with the expectation that autonomy increases as trust is established. It's an honest acknowledgement that this is a waypoint, not a principled endpoint — and that makes "is this LLM's values really sound?" a research frontier question, not a deployable guarantee.

### Federated sense-making as a theory of bond governance

If bad actors know ocean-related LLM interactions feed into bond scoring, they have an incentive to flood the system with fabricated signal — a Sybil attack on the human swarm layer. The aggregation agent has to weight signals by credibility, cross-reference against other data streams, and detect coordinated inauthentic behavior. This mirrors the problem social platforms have been losing at for years, which means "agents monitoring ocean health" is *also* a moderation problem, not just a measurement problem.

## Session arc

Definitional murkiness → bluewashing verification → God-tier measurement as a thought experiment → sleeper agents and the MoE-vs-single-model question → constitutional AI → Anthropic's corrigibility stance → federated sense-making as bond governance → the prompt-is-not-the-stack correction.

## Safety

> [!WARNING]
> This session shows agentic learning working. It only works with a pushback-capable model. See [BullshitBench](https://petergpt.github.io/bullshit-benchmark/viewer/index.v2.html) and [.github/WARNING.md](https://github.com/evnchn-agentic/.github/blob/main/WARNING.md#agentic-learning) before trying this method on another tool.

## Attribution

| | |
|---|---|
| **Date** | Early April 2026 |
| **Model** | Claude Sonnet 4.6 (extended thinking) |
| **Interface** | claude.ai |
| **License** | [CC BY 4.0](./LICENSE) — attribute [Evan Chan](https://github.com/evnchn) |

## Read it

[`transcript.md`](./transcript.md) — original mistakes preserved. The conversation is the domain-hopping chain mode of agentic learning: one question followed from finance into AI alignment and back, with the meta-lesson surfacing near the end rather than being the starting point.

[`FACTCHECK.md`](./FACTCHECK.md) — Claude's claims checked against primary sources in November 2026, seven months on. 3 were wrong, including the "sleeper agent" problem the MoE thread was built on, which is really a different paper.

---

*Read the [full agentic-learning philosophy →](https://github.com/evnchn-agentic/.github/blob/main/PHILOSOPHY_THINKER.md)*
