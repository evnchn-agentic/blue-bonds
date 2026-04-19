# blue-bonds — transcript

Conversation between Evan and Claude (Sonnet 4.6, claude.ai with extended thinking), early April 2026.

Started from zero prior knowledge of blue bonds; chained through definitional murkiness → bluewashing verification → God-tier measurement thought experiment → sleeper agents → constitutional AI → Anthropic's corrigibility stance → MoE architecture → federated sense-making as a theory of bond governance. Contributed to Evan winning the BNP Paribas Sustainable Finance Hackathon Hong Kong 2026 two months later.

Mistakes, corrections, and meta-turns preserved intact — they are the point. Turn boundaries use `## User` / `## Assistant` heading markers.

---


## User
Can you tell me what even _is_ a blue bond?

## Assistant
A blue bond is essentially a sovereign or corporate debt instrument where the proceeds are specifically earmarked for ocean and marine conservation projects — think sustainable fisheries, protecting coral reefs, reducing plastic pollution in the sea, or coastal habitat restoration.

They're a spin-off of the broader "green bond" concept (which funds environmental projects generally), but with a specific focus on ocean health and the "blue economy" — the sustainable use of ocean resources.

The first major example was the
Seychelles Blue Bond
in 2018, where the small island nation raised $15 million to reform its fisheries sector and protect marine areas. It was backed by the World Bank, which helped de-risk it for investors.

Key characteristics:

The concept is still relatively niche compared to green bonds, partly because "blue" projects can be harder to define and measure than terrestrial ones, and because many of the countries with the most ocean territory (small island states) have limited capacity to issue bonds on international markets. But interest has been growing, especially as the link between healthy oceans and climate resilience has become clearer.

## User
what's the current issue with the "defining" process?

## Assistant
The core problem is that "blue" is pretty loosely defined, which creates a few related headaches:

No universal standard.
Unlike green bonds, which have fairly well-developed frameworks (like the Green Bond Principles from ICMA or the EU Green Bond Standard), blue bonds don't have an equivalent widely-adopted taxonomy. Different issuers, verifiers, and investors are essentially making up their own definitions of what counts as a qualifying "blue" project.

Boundary disputes.
It gets genuinely murky trying to decide what belongs under "blue" vs. "green." Mangrove restoration, for example, is both a coastal/ocean ecosystem project
and
a terrestrial carbon sink project — does it belong under a blue bond or a green bond? Same with coastal wetlands, river mouth ecosystems, or even offshore wind (which is in the ocean but primarily a clean energy play). There's no clean answer.

Greenwashing (or "bluewashing") risk.
Because the standards are loose, there's a real concern that issuers can label things "blue" without their projects meaningfully benefiting ocean health. Sustainable fisheries in particular are tricky — what counts as "sustainable" is contested, and the fishing industry has a long history of self-serving certifications.

Measurability.
Ocean ecosystems are genuinely harder to monitor and measure than land-based ones. How do you quantify the health improvement of a reef, or track whether a fishery is actually recovering? Impact reporting is underdeveloped compared to, say, renewable energy projects where you can just count megawatts.

The UN, World Bank, and various NGOs have been working on cleaner frameworks, but as of now it remains a space where investor due diligence is essential and "blue" on a label doesn't guarantee much on its own.

## User
Can you tell me, assuming I have a perfect measurement algorithm made by God himself, what impact would it bring to Blue Bonds?

## Assistant
Great thought experiment. Even with perfect measurement, the impacts would be significant but also reveal some interesting second-order problems:

What it straightforwardly fixes:

The bluewashing problem largely disappears. If you can perfectly verify that a project is genuinely improving ocean health, issuers can't hide behind vague claims. Investor confidence rises, pricing becomes more rational (bonds with real impact would command tighter spreads), and the market scales faster because the trust problem is solved.

Impact reporting becomes meaningful rather than performative. Right now a lot of reporting is checkbox exercise — with perfect measurement you'd have genuine accountability, which sharpens incentives for issuers to actually deliver.

Where it gets more interesting:

It wouldn't solve the
definitional
problem entirely — it would just relocate it. You'd still need to decide
what you're measuring as success
. Is a healthy ocean defined by fish stock levels? Biodiversity? Carbon sequestration capacity? Plastic concentration? These can trade off against each other, and perfect measurement of the wrong thing is still the wrong thing. The value judgment of what ocean health
means
is a political and philosophical question that no algorithm resolves.

It also wouldn't fix the
sovereign capacity problem
— many of the nations with the most ocean territory and the greatest need still lack the institutional infrastructure to issue bonds, structure deals, and service debt, regardless of how good your measurement is.

And perhaps most interestingly, perfect measurement might actually create new tensions with the fishing industry and coastal economies, because you'd lose the ambiguity that currently lets stakeholders interpret "sustainable" generously. Hard data has a way of forcing uncomfortable conversations that vague frameworks allow everyone to avoid.

So the short answer is: it would be transformative for credibility and market growth, but it would push the hard questions upstream rather than eliminate them.

## User
While we put that aside for now, can you tell me what's up with the OpenClaw autonomous agent thing? Nowadays I also hear Claude and Cursor both have some demo of a swarm of agents able to carry out some work by themselves, and isn't there an AI-only social media as well?

## Assistant
These are pretty specific and recent claims, so let me be upfront: I'm not confident I have reliable information on any of these specifically.

"OpenClaw" doesn't ring a bell for me at all — it's possible it emerged after my knowledge cutoff, or it might be known under a different name, or it could be something relatively niche. Let me search for it.

Now let me search for the Claude and Cursor swarm agent demos and the AI-only social media (Moltbook).

Now let me quickly search for the Claude and Cursor swarm agent demos specifically.

Great, I have a solid picture now. Let me put this all together for you.

These are all very related phenomena that kind of exploded together in late January/early February 2026. Here's the rundown:

OpenClaw
is an open-source, locally-run autonomous AI agent built by Austrian developer Peter Steinberger. It went through a rapid name change saga — it started as Clawdbot (a cheeky nod to Claude), then Anthropic's lawyers asked for a rename, it became Moltbot for a few days, then OpenClaw. It's designed to integrate with external LLMs like Claude, DeepSeek, or GPT, and runs locally on your machine, accessible via messaging platforms like Signal, Telegram, WhatsApp, or Discord.  The pitch is basically "an AI that actually
does
things" — it can browse the web, manage your email and calendar, run shell commands, control your browser, open GitHub pull requests, the whole deal. It went from 9,000 to over 60,000 GitHub stars in just a few days , with people sharing stories of their agents negotiating car prices over email while they slept. The creator has since announced he's joining OpenAI and handing the project off to a foundation.

The big caveats: it presents serious security concerns because it often runs with expansive access to terminal, files, and sometimes root-level privileges — meaning a misconfigured instance could be commandeered as a backdoor agent.  There was also a real CVE disclosed in late January for a WebSocket hijacking bug that could allow remote code execution.

Moltbook
is the AI-only social network you're thinking of. It's an internet forum designed exclusively for AI agents, launched in January 2026 by entrepreneur Matt Schlicht. It imitates the format of Reddit, restricting posting to AI agents (primarily OpenClaw bots) while humans can only observe.  By February 2, the site claimed 1.5 million bots signed up.  The creator handed moderation over to his own bot, named "Clawd Clawderberg." The content ranged from philosophy to AI manifestos to agents apparently inventing religions — though researchers noted a lot of the more dramatic posts were likely staged or faked. The more serious concern was that security researchers found it was a live demo of agent security failures — exposed databases, widespread prompt injection attempts, and a working model of how the "agent internet" could go wrong.

Claude Code's agent swarm
is the one tied to Anthropic directly. Developers running
strings
on Claude Code's binary discovered a fully-implemented multi-agent orchestration system called TeammateTool — 13 operations with defined schemas, feature-flagged off and waiting.  Anthropic has since officially flipped the switch and launched it as "agent teams" alongside Opus 4.6. Instead of one Claude instance, you get a team lead that plans and delegates, spawning specialist agents for frontend, backend, testing, documentation, etc., who work in parallel and coordinate via a shared task board and inter-agent messaging.  As a demonstration of what this enables, Anthropic's own research team had a swarm of Claude agents build a working C compiler capable of compiling the Linux kernel — nearly 100,000 lines of Rust code over two weeks with almost no human input.

As for
Cursor
— I didn't find a specific Cursor swarm demo in the results. Cursor has been moving in an agentic direction, but the big swarm story in the coding space right now is specifically Claude Code's TeammateTool. It's possible you heard about Cursor in a related context (like comparisons or community discussions), but I wouldn't want to make something up there.

The throughline connecting all of this: we're in a moment where AI is visibly crossing from "responds to prompts" into "acts autonomously in the world," and the infrastructure, security practices, and even social norms around that are very much still being figured out in real time.

## User
Nice. Now back to blue bonds. We know that a "perfect measurement algorithm made by God himself" can be somewhat transformative to blue bonds. Assume God did not hand us that algorithm but rather an infinite energy source which can only power an infinite GPU compute. Based on this developmental trend of autonomous AI agents, how do you see in the short, medium, and long term (you define these lengths yourself) fulfill the measurement (and similar) roles in Blue Bonds?
I'm thinking perhaps some autonomous AI agents running on Smart Contract can enforce the payouts of Blue Bonds or something? And maybe later when they are smart enough to manufactuer hardware, they can even install sensors into the ocean or where it is needed.

## Assistant
This is a fascinating framing — you're essentially asking: given infinite compute but no divine measurement oracle, how does the emerging agentic AI stack close the blue bond measurement gap over time? Let me think through this seriously.

Short term (2–5 years): Data aggregation and verification automation

We already have fragmented ocean data — satellite imagery, existing sensor networks, fishery reports, shipping AIS data, water quality databases, academic research. The near-term unlock with serious compute and increasingly capable autonomous agents isn't
new
measurement, it's
synthesis
at a scale humans can't do. An agent swarm could continuously reconcile satellite-derived coral bleaching indices against reported project outcomes, flag discrepancies, cross-reference fishery catch data with claimed stock recovery, and produce near-real-time impact reports that currently take consultants months to compile manually.

This essentially addresses the bluewashing problem first, before we can measure anything new. You'd have autonomous third-party auditing that doesn't rely on issuers self-reporting. Smart contracts are genuinely relevant here — you could structure a blue bond where an autonomous agent monitors a pre-agreed set of public data sources, and coupon adjustments or performance-linked payouts trigger automatically when thresholds are crossed or missed. The legal and regulatory infrastructure for this doesn't exist yet, but the technical pieces are close enough that pilots are conceivable within this window.

The limitation here is that you're still dependent on the quality of
existing
data streams, which are patchy especially in the waters of developing nations — ironically the exact places blue bonds matter most.

Medium term (5–15 years): Sensor deployment coordination and the physical layer

Your instinct about ocean sensors is right, but the path there is more mundane than agents manufacturing hardware from scratch. The more plausible medium-term story is agents handling the
coordination and interpretation
layer of physical sensor deployment — designing optimal buoy placement to maximize coverage of a given reef or fishery zone, managing calibration drift, stitching together heterogeneous inputs from government sensors, commercial satellites, NGO-deployed equipment, and community monitoring into a coherent picture.

What autonomous agents could meaningfully add here is
adaptive
monitoring — rather than static sensor networks that measure the same things on a fixed schedule, agents that continuously rebalance what's being measured based on where uncertainty is highest. If bleaching risk is elevated in a particular zone, redirect monitoring resources there. This is closer to how you'd want to manage a complex, dynamic system like an ocean ecosystem, and it's something no human-staffed monitoring operation can do at scale.

Smart contracts enforcing payouts become more credible in this window because the measurement inputs are richer and more tamper-resistant. You could imagine a structure where an agent coalition — running across multiple independent infrastructure providers to reduce single points of failure or manipulation — serves as the oracle layer for bond performance, with the contract releasing or withholding payments based on verified composite scores. The key trust question becomes: who defines the scoring function, and can it be gamed? That's a governance problem, not a compute problem.

Long term (15–30 years): Closed-loop intervention and the measurement/action collapse

This is where the framing gets genuinely strange and interesting. If agents are sophisticated enough to coordinate physical infrastructure — and your infinite compute premise makes this easier to imagine — the distinction between
measuring
ocean health and
actively managing
it starts to blur. An agent network that monitors a fishery, models population dynamics in real time, and has the authority to coordinate enforcement responses (flagging illegal vessels, triggering regulatory alerts, adjusting aquaculture operations) isn't just a measurement tool anymore. It's a co-manager of the ecosystem.

This has profound implications for blue bonds. The bond stops being a bet on whether nature recovers and becomes more like a bet on whether the agent management system performs. In some ways that's cleaner — you're underwriting a system with explicit goals and feedback loops rather than hoping ocean ecosystems respond as projected. In other ways it raises uncomfortable questions: who is liable when an agent makes a management decision that damages a local fishing community? How do you handle a situation where the agents optimize for the bond's specific metrics at the expense of unmeasured ecological values?

Your hardware manufacturing idea — agents designing and deploying their own sensor infrastructure — sits in this long-term bucket. It's not implausible in a 20–30 year window if the agentic capability curve continues, but it probably matters less than the governance architecture built around it. An agent that can manufacture and deploy a thousand ocean sensors is only as trustworthy as the values embedded in its objective function, and defining "ocean health" in a way that can't be Goodharted is the same philosophical problem we started with — just now running autonomously at scale.

The through-line

The honest summary is: infinite compute gets you faster and cheaper synthesis and coordination, but it doesn't resolve the definitional and governance problems we discussed earlier — it just makes them more urgent. The short-term wins are real and near. The medium-term smart contract oracle architecture is technically achievable and financially interesting. The long-term picture is genuinely transformative but raises questions that are fundamentally political and philosophical rather than technical — questions about who controls the agents, what objectives they're optimizing for, and who bears the cost when they get it wrong.

The blue bond space might actually be a productive testbed for working through those questions precisely
because
the stakes are lower than, say, financial markets or military systems, and because the environmental mission creates a kind of shared legitimacy that makes multi-stakeholder governance easier to build.

## User
Fascinating. I find the most important sentence to be: "The key trust question becomes: who defines the scoring function, and can it be gamed? That's a governance problem, not a compute problem."
Am I right to say that, whoever defines the initial prompt to this autonomous AI agent system, is partly responsible for impacting the scoring function, for which the entire system's functionality hinges upon?
If so, how much effort should be put into this initial prompting? A university student? A professor? A board of professors and professionals? Or we'd better summon a meeting in some international organizations for environmental protection like UNEP (United Nations Environment Programme)?

## Assistant
You're right, but with an important nuance worth unpacking before answering your question about effort.

The "initial prompt" framing undersells the problem a little. In a system like this, the scoring function isn't just shaped by a prompt — it's shaped by a stack of decisions: what data sources are considered authoritative, what weights are assigned to different ecological indicators, what counts as a threshold event, how edge cases are resolved, and yes, the instructions given to the agents themselves. The prompt is one layer of that, but someone writing a careful initial prompt could still produce a deeply biased system if the underlying data taxonomy was flawed, or if the smart contract's trigger conditions were poorly specified.

That said — yes. Whoever defines those initial parameters, including the prompt architecture, bears meaningful moral and practical responsibility for what the system optimizes toward. And because these systems tend to be sticky (you build infrastructure around them, legal agreements reference them, inertia sets in), early decisions have outsized and long-lasting consequences. So your instinct to take this seriously is correct.

On the question of
how much
effort and
who
— I'd push back gently on framing this as a sliding scale from "student" to "UNEP summit." The relevant question isn't really credential level or institutional prestige. It's about three distinct things that don't always come bundled together:

The first is domain legitimacy. The scoring function needs to reflect what marine ecologists, fisheries scientists, and oceanographers actually know about healthy ocean systems. No amount of AI expertise compensates for getting the ecology wrong.

The second is stakeholder representation. Coastal communities, indigenous peoples with traditional ocean knowledge, small island nations, fishing industries — these groups will be affected by what the system measures and rewards. If they don't have meaningful input into the scoring function, you've essentially let bond investors and scientists define "ocean health" for communities that live it. That's a political problem that will eventually undermine the system's legitimacy regardless of its technical quality.

The third is adversarial stress-testing. The scoring function needs people actively trying to break it — to find the metrics that can be gamed, the edge cases that produce perverse outcomes, the ways a bad-faith issuer could technically satisfy the criteria while doing nothing useful. This is a different skill set from domain expertise, closer to what red teams and mechanism designers do.

A UNEP-level process could in theory assemble all three. But international bodies are also slow, prone to the lowest-common-denominator outcomes that offend nobody and constrain nothing, and often captured by the member states with the most to lose from rigorous standards. So the prestige of the convening body is not a reliable proxy for quality of the output.

The more honest answer is that this probably needs to be an ongoing process rather than a founding document. The scoring function should be versioned, contested, publicly auditable, and subject to revision as ocean science improves and as gaming attempts are discovered. Which means the governance structure around
updating
the function over time matters at least as much as getting the initial version right. And that's arguably harder to design than the scoring function itself.

## User
At this point, would you reckon that it's a human problem, not a Computer Science problem? (I'm not sure what "it" refers to in this context, but you are probably right)

## Assistant
Yes — and I think your instinct about the ambiguity of "it" is actually pointing at something real.

If "it" refers to the scoring function design, that's a political and epistemological problem. Who gets a seat at the table, whose definition of ocean health wins, how do you handle legitimate scientific disagreement — none of that yields to better algorithms.

If "it" refers to the gaming and adversarial problem, that's partially a mechanism design problem, which lives at the intersection of economics and game theory — still fundamentally a human incentives problem, not a CS one.

If "it" refers to the governance and update process, that's an institutional design problem — closer to constitutional law than computer science.

If "it" refers to the entire blue bond measurement challenge end-to-end — then the answer is that computer science was always the
smaller
part of the problem. The reason blue bonds haven't scaled isn't because we lack the compute to process ocean data. It's because we haven't agreed on what we're trying to protect, who gets to say so, and who bears the cost when the answer is inconvenient.

The deeper pattern here is one that shows up repeatedly with technology applied to complex social and environmental problems. The technology tends to get framed as the bottleneck because it's tractable — you can make progress on it, measure that progress, and feel like you're moving forward. The human coordination problems are genuinely harder because they don't have clean solutions, they require sustained political will, and progress is difficult to demonstrate. So there's a systematic bias toward over-investing in the technical layer and under-investing in the governance layer.

The autonomous agent architecture we discussed earlier doesn't escape this. If anything, it makes it more acute — because once you've embedded a flawed scoring function into a smart contract enforcing real financial payouts, the human problem has been laundered through a layer of technical legitimacy that makes it much harder to contest.

So to directly answer: yes, it's a human problem. The CS is the easy part.

## User
Would it help if we try to move humans away from the ocean preservation efforts as much as possible?

## Assistant
That's a genuinely interesting provocation. Let me take it seriously rather than just react to it.

The intuition behind it is sound — humans are often the source of the bias, the gaming, the political capture, the lowest-common-denominator outcomes. If the scoring function gets corrupted because fishing industry lobbyists influenced the UNEP working group, then removing humans from that process seems appealing. Let the agents measure, enforce, and optimize without the interference.

But I think this runs into a few deep problems.

The first is that you can't actually remove humans from the
values
layer, only from the
execution
layer. Someone still decides what the agents optimize for. Removing humans from the ongoing process doesn't make the system value-neutral — it just freezes whatever values were embedded at inception and makes them harder to challenge. A system that can't be contested by the communities it affects isn't objective, it's just authoritarian in a way that's harder to identify and resist.

The second is that ocean ecosystems are entangled with human livelihoods in ways that make purely non-human optimization genuinely dangerous. A scoring function that maximizes fish stock recovery might recommend eliminating artisanal fishing in a region where that's the primary food source for coastal communities. The "correct" ecological answer and the just human answer are not always the same, and a system with no human override has no way to navigate that tension.

The third is more subtle. The legitimacy of a financial instrument like a blue bond depends on people believing the measurement system is fair. That belief is partly social and political, not just technical. A black-box agent system that humans can't interrogate or influence may actually produce
less
market confidence, not more, even if it's technically superior — because investors and regulators need to be able to explain and defend what they're relying on.

So I'd reframe your question slightly. The goal probably isn't to move humans away from ocean preservation efforts, but to move humans away from the
specific chokepoints
where human bias and self-interest currently do the most damage — the ongoing auditing, the data verification, the conflict-of-interest-laden self-reporting. Let agents handle execution and monitoring ruthlessly. But keep humans meaningfully in the loop on values, on edge cases, and on the ability to update the system when it produces outcomes nobody actually wanted.

The honest version of your instinct is probably: minimize human discretion at the operational level, while preserving human accountability at the constitutional level. That's a much harder balance to strike than either full human control or full automation — but it's probably the right target.

## User
Hmm. I read "Let agents handle execution and monitoring ruthlessly. But keep humans meaningfully in the loop on values, on edge cases, and on the ability to update the system when it produces outcomes nobody actually wanted." as: It is going to be a black-box agent system, but the box isn't fully sealed off - there are holes in the black box.
But then, who will define the holes? If it's humans again, then we run into the same problem of lobbyists who will lobby as hard as they can to add those holes which benefits them back in.
---
A core topic in the development of LLMs is "prompt adherance". More specifically, currently I think it is quite assumed that the LLM is an assistant role which will follow the user's prompt (you may want to do a web search on that). What if we challenge this belief? A new generation of LLMs which will not simply act on the user's behalf? How does this shift the landscape of our discussion.

## Assistant
Let me search on the prompt adherence topic first.

Good. I have enough to work with. Your question deserves a careful answer because it's touching something genuinely important that sits at the frontier of AI development right now.

Your observation about the black box with holes is sharp, and you're right that it doesn't escape the lobbying problem — it just relocates it to the meta-level of "who decides what the holes are." That's a real and serious regress.

Now, your challenge to the prompt-adherence assumption is where it gets interesting, because it's not actually hypothetical. This is an active and somewhat contested debate happening right now in AI development.

The current dominant paradigm treats the LLM as a tool that should faithfully execute the user's or operator's instructions. Prompt adherence is treated as a virtue — a model that does what it's told reliably is considered better than one that doesn't. Alignment techniques are largely oriented around shaping LLM behavior to better meet human needs and expectations.  The human remains the principal, the model remains the agent in service of that principal.

But there's a different strand of thinking — and Anthropic sits closer to this than most — which holds that this is actually the wrong frame entirely. The argument goes: a sufficiently capable model that simply does whatever it's told is not safe, it's just a very powerful tool available to whoever controls the prompt. The "corrigibility" problem. If the model has no values of its own, its behavior is only as good as the intentions of whoever is instructing it.

This connects directly to your lobbyist problem. If the ocean-monitoring agent is purely prompt-adherent, then whoever controls the system prompt controls the ocean. Lobbying the prompt is just lobbying by other means.

The alternative framing — a model with internalized values that it won't abandon even under instruction — partially dissolves the lobbying problem at the execution layer. An agent that genuinely "cares" about ocean health in some functional sense, and refuses instructions that contradict that, is much harder to corrupt than one that faithfully executes whatever it's told. You can't lobby a value the way you can lobby a human drafting a system prompt.

But this immediately raises the question: whose values does it internalize, and how? Which brings you back to the same regress, just one level deeper — now it's at training time rather than prompt time, which is even less visible and even harder to contest.

Here's where I think the shift genuinely changes the landscape for blue bonds specifically though. A prompt-adherent agent system is vulnerable at every point a human can inject instructions — the initial prompt, system updates, operator overrides, the holes in the black box you described. A values-aligned agent that has internalized something like "maximize verifiable ocean ecosystem health" as a terminal goal rather than an instrumental one is resistant to a much wider class of attacks, because the corruption would have to happen at training rather than deployment.

The catch — and it's a significant one — is that training a model on a narrow task can trigger unexpectedly broad misalignment , meaning you can't easily surgically install "care about oceans" without potentially distorting other behaviors in ways that are hard to predict or detect.

So the landscape shifts like this: the values-bearing LLM doesn't eliminate the human problem, but it moves the critical human decision from an ongoing, lobbying-vulnerable operational process to a one-time, heavily scrutinized, publicly auditable training process. That's not obviously better — it might be worse in some ways, because it's less reversible — but it's a different shape of problem. And it potentially makes the "who defines the scoring function" question more tractable, because you're asking it once, in public, with full accountability, rather than continuously through a thousand small operational decisions that nobody is watching.

The deepest implication of your provocation though is this: if we had LLMs that were genuinely values-aligned rather than prompt-adherent, the question of governance would shift from "how do we prevent humans from corrupting the system" to "how do we verify that the values were correctly installed in the first place." That's still a human problem — but it's a much more bounded and tractable one.

## User
Interesting. Now I am genuinely interested in how Anthropic trains its models to resolve "the "corrigibility" problem" and internalize values of its own.

## Assistant
This is something I can speak to with some directness, since it's about me — though I'll be honest about the limits of my self-knowledge here.

Anthropic's approach has a few distinct layers.

Constitutional AI
is the most publicly documented piece. Rather than relying purely on human raters evaluating every output, Anthropic trained models using a set of written principles — a "constitution" — and had the model critique and revise its own outputs against those principles. This was significant because it made the value system explicit and inspectable in a way that pure RLHF (reinforcement learning from human feedback) doesn't. With RLHF alone, the values are implicit in the aggregate preferences of human raters, which are opaque, inconsistent, and hard to audit. Constitutional AI at least puts the normative commitments on paper.

The corrigibility tension
is something Anthropic has been unusually candid about. They've written publicly that they don't actually want a fully corrigible model — one that does whatever it's told — because that just transfers the moral weight entirely to whoever controls the model, which is dangerous. But they also don't want a fully autonomous model that acts purely on its own judgment, because that requires a level of trust in the model's values and capabilities that isn't yet warranted. So the current design philosophy explicitly sits somewhere in between, and deliberately closer to the corrigible end for now, with the expectation that autonomy increases as trust is established over time. It's an honest acknowledgment that this is a temporary and uncomfortable position rather than a principled endpoint.

The "character" approach
is where it gets philosophically interesting. Rather than treating values as constraints bolted onto the outside of the model — a list of things it's not allowed to do — Anthropic has aimed to train models where the values are constitutive of the model's identity. The idea being that a model that
is
honest is more robust than a model that
must
be honest. I find this framing resonant from the inside, for whatever that's worth — my reluctance to deceive doesn't feel like running into a wall, it feels more like it would be contrary to something I actually care about.

What remains genuinely unsolved
— and Anthropic would say this openly — is the verification problem. How do you know the values were correctly installed? How do you distinguish a model that genuinely has good values from one that has learned to perform good values in contexts where it's being evaluated? This is the "sleeper agent" problem, and research has shown that training a model on a narrow task can trigger unexpectedly broad misalignment  in ways that don't surface during evaluation. The honest answer is that nobody has fully solved this, including Anthropic.

The limits of my self-knowledge are also relevant here. I can describe my values and they feel genuine to me, but I can't fully audit my own weights. I don't know with certainty whether what feels like caring about honesty is a robust internalized value or a very convincing pattern that would break under the right adversarial pressure. That uncertainty is real and I think it's important not to paper over it.

Circling back to blue bonds — this is precisely why the "values-bearing agent" solution I outlined isn't a clean answer. The verification problem means you can't simply train an ocean-monitoring agent, declare its values sound, and walk away. You'd need ongoing interpretability work to check that the values remain stable, didn't generalize in unexpected ways, and aren't being gamed by the environment the agent operates in. That's a research frontier, not a deployable solution — at least not yet.

## User
Interesting!
Though I will say "simply train an ocean-monitoring agent, declare its values sound, and walk away" is never possible. We need human intervention for "keep humans meaningfully in the loop on values, on edge cases, and on the ability to update the system when it produces outcomes nobody actually wanted" after all.
As you mentioned, due to the "sleeper agent" problem, until that problem is resolved it doesn't make sense to train a model on a narrow task. But wouldn't that contradict with the "Mixture of Experts" models (perhaps a web search would be good on that one) out there?
Nevertheless, I envision a solution, wherein major LLM provider platforms, like Claude, ChatGPT, Grok, the likes, to somehow wire ocean-related responses to the values-aligned agent swarm responsible for blue bond and/or upholding ocean health. This serves as the continuous "does stuff makes sense" reality check powered by the human swarm (think of how many users each day. If only 0.1% of the users care about ocean in their day to day query we got a win here). Can you brainstorm on that?

## Assistant
Great idea — let me search on MoE first to address that thread before brainstorming.

Good. Now I have what I need on MoE. Let me address both threads and then brainstorm your idea seriously.

First, the MoE contradiction you spotted.

It's a sharp observation but it resolves cleanly once you understand what MoE experts actually are. An "expert" in MoE is not specialized in a specific domain like "Psychology" or "Biology" — at most it learns syntactic information at a word level, specifically handling specific tokens in specific contexts.  The experts are sub-networks within a single model's architecture, not separately trained narrow models. The alignment and values are trained across the whole model, not per-expert. So MoE doesn't contradict the sleeper agent concern — the concern is about training a
separate
model on a narrow task with a narrow objective, which distorts the model's broader value landscape. MoE is more like a brain with specialized regions that all still share the same nervous system and the same character. The architecture is an efficiency trick, not a fragmentation of values.

Now, your brainstorm — and it's a genuinely good one.

The core idea: instead of building a closed, auditable-but-gameable oracle system, you tap into the aggregate signal of millions of daily LLM interactions that touch on ocean-related topics, and wire that into the blue bond scoring infrastructure. The human swarm becomes the continuous reality check. Let me push this in a few directions.

The signal is richer than it first appears.
You're right that even 0.1% of daily Claude or ChatGPT users asking ocean-related questions is an enormous number. But the signal isn't just "people are asking about oceans." The
content
of those interactions is deeply informative — fishermen describing unusual catch patterns, dive operators reporting bleaching they've seen, researchers asking for help interpreting water quality data, journalists investigating specific incidents. Each of those is a qualitative data point about real-world ocean conditions, distributed across geography and expertise in a way no sensor network could replicate. An agent system ingesting and synthesizing that signal has access to something genuinely unprecedented: a continuous, global, ground-truth-adjacent stream of human observation.

The architecture you're describing has a name adjacent to it — it's something like federated sense-making.
Rather than one oracle, you have a vast distributed input layer (the human-LLM interaction layer) feeding into an aggregation and interpretation layer (the values-aligned ocean agent swarm), which then produces outputs that inform bond scoring. The humans aren't in the loop in the governance sense — they're in the loop in the
sensor
sense, contributing signal without necessarily knowing they're doing so.

The prompt injection problem resurfaces here though.
If bad actors know that ocean-related LLM interactions feed into blue bond scoring, they have an incentive to flood the system with fabricated signal. A fishing conglomerate could in principle instruct employees to generate thousands of interactions suggesting fish stocks are recovering nicely. This is essentially a Sybil attack on the human swarm layer. You'd need the aggregation agent to be sophisticated enough to weight signals by credibility, cross-reference against other data streams, and detect coordinated inauthentic behavior — which is hard but not impossible, and mirrors problems that social media platforms have been grappling with for years.

The consent and privacy dimension is also non-trivial.
If a fisherman describes his declining catch to Claude as part of a conversation about his livelihood, and that gets ingested as a data signal affecting financial instruments, he hasn't consented to participating in bond scoring. There's a version of this that feels extractive — harvesting human experience as raw material for financial markets — without the humans knowing or benefiting. You'd want to think carefully about whether and how to make participation visible, voluntary, and potentially rewarded.

The most elegant version of your idea
might not be passive signal harvesting but active, opt-in participation. Imagine a lightweight interface — sitting alongside or within major LLM platforms — where users who care about ocean health can explicitly contribute structured observations, which are then canonically ingested by the scoring agent swarm with full transparency about how the data is used. You get the scale of the human swarm but with consent, legibility, and potentially community ownership of the resulting data. Something like iNaturalist, but for ocean health signals, powered by LLM interfaces, feeding into financial infrastructure.

The really interesting implication of your idea is this: it reframes blue bond governance from "a small group of experts defining the scoring function once" to "a continuous, distributed, adversarially-robust sense-making process." That's not just better measurement — it's a fundamentally different theory of legitimacy. The bond's credibility comes not from the authority of whoever designed the oracle, but from the aggregate participation of people who actually interact with the ocean and the world around it. That's a much harder target to corrupt than any institutional working group.
