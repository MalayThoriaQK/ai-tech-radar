<div align="center">

# 📡 The Radar — an executive AI briefing

### 22 AI technologies from the last 18 months — beyond what the general public uses

![format](https://img.shields.io/badge/format-21_technologies-8A631C?style=for-the-badge)
![audience](https://img.shields.io/badge/audience-technology_leaders-8A631C?style=for-the-badge)
![evidence](https://img.shields.io/badge/evidence-verified_Aug_2026-8A631C?style=for-the-badge)
![homework](https://img.shields.io/badge/homework-none-8A631C?style=for-the-badge)
![license](https://img.shields.io/badge/license-CC_BY_4.0-8A631C?style=for-the-badge)

</div>

> For technology leaders who want to know what has actually changed. Twenty-one technologies from roughly the last eighteen months, all of them well past what the general public sees: AI models a company can own instead of rent, the plumbing behind agents, what agents need to deal with the outside world, a few things that look nothing like a chatbot, and the software now testing other software. Each entry says what happened, links the proof, and says what it makes possible. No warnings, no advice, no homework.

## 📖 How to read this

- **New, not news.** Everything here shipped in roughly the last eighteen months and sits beyond the chatbots and copilots the general public already uses.
- **Capabilities, not warnings.** Each entry is something that now exists and what it makes possible. The conclusions are yours to draw.
- **Check the evidence.** Every claim links to announcements, papers, and benchmarks. Quote the source, not the summary.
- **It moves.** A radar is a snapshot, dated 19 August 2026. Half of this will be mainstream within a year — which is exactly why it's here now.

---

## Part one — Owning the model, not renting it

*Until recently, serious AI meant paying for someone else's model by the request. These four make running and shaping your own realistic.*

### 01 · Free models caught up with the paid ones

The models anyone can download have nearly caught the ones you rent. Moonshot's Kimi K2.6, Z.ai's GLM-5.2, and DeepSeek V4 Pro all landed within a few points of the best paid models on standard coding tests in 2026, and most allow commercial use. DeepSeek costs roughly a tenth as much per unit of text — and running it on your own machines removes the meter altogether.

**Evidence:** [MarkTechPost: Kimi K3 vs DeepSeek V4 Pro vs GLM-5.2 compared](https://www.marktechpost.com/2026/07/18/kimi-k3-vs-deepseek-v4-pro-vs-glm-5-2-open-trillion-scale-moe-models-compared-on-benchmarks-license-and-serving-cost/) · [Artificial Analysis: Kimi K2.6 intelligence, performance and price](https://artificialanalysis.ai/models/kimi-k2-6) · [Simon Willison: GLM-5.2 is probably the most powerful text-only open-weights LLM](https://simonwillison.net/2026/jun/17/glm-52/)

> 💡 **What it opens up —** Sensitive work can stay entirely inside a company's own network, with no per-use fee and no supplier deciding when the model changes underneath you.

### 02 · Teach a model your work by checking its answers

If a computer can check whether an answer is right — the tests pass, the numbers reconcile, the workflow finishes — that check alone can train a model. The method behind DeepSeek's reasoning models now comes ready-made: Hugging Face ships a trainer for it, AWS published a step-by-step recipe, and Nous Research packages the whole setup. You define the task and the check; the tools handle the training.

**Evidence:** [AWS: verifiable-rewards RL with GRPO on SageMaker](https://aws.amazon.com/blogs/machine-learning/overcoming-reward-signal-challenges-verifiable-rewards-based-reinforcement-learning-with-grpo-on-sagemaker-ai/) · [Nous Research Atropos RL environments framework](https://github.com/nousresearch/atropos) · [IBM Research, ICML 2026: GRPO's loss dynamics and success amplification](https://research.ibm.com/publications/reinforcement-learning-with-verifiable-rewards-grpos-loss-dynamics-and-success-amplification)

> 💡 **What it opens up —** A model can be trained against a company's own definition of correct, rather than coaxed towards it with cleverly worded instructions.

### 03 · Copy an expensive model's skill into a cheap one

Distillation means training a small model to imitate a big one. The 2025 version has the small model attempt the work itself while the big one grades every word it writes, which works far better than the older approach of copying finished answers. NVIDIA used more than ten teacher models this way to build one of its own, and the technique now sits inside most frontier training recipes.

**Evidence:** [Thinking Machines Lab: On-Policy Distillation](https://thinkingmachines.ai/blog/on-policy-distillation/) · [arXiv survey of on-policy distillation for LLMs](https://arxiv.org/abs/2604.00626) · [Hugging Face: Distillation in 2026 across frontier models](https://huggingface.co/blog/sergiopaniego/distillation-2026)

> 💡 **What it opens up —** A costly model becomes a teacher rather than a supplier — its behaviour on your particular work captured in a small model you own and run for a fraction of the price.

### 04 · Models now train across the open internet

Training a large model used to need one enormous data centre. Nous Research trained Hermes 4.3 across twenty-four independent computers scattered around the internet, at speeds matching a single cluster. Prime Intellect did the same on the harder pre-training side, releasing models up to 106 billion parameters trained this way, along with the full recipe for anyone to copy.

**Evidence:** [Nous Research: Introducing Hermes 4.3, trained on Psyche](https://nousresearch.com/introducing-hermes-4-3) · [Implicator: Prime Intellect's INTELLECT-3](https://www.implicator.ai/prime-intellects-intellect-3-open-source-ambition-meets-centralized-reality/) · [Survey of decentralized LLM training (arXiv)](https://arxiv.org/pdf/2503.11023)

> 💡 **What it opens up —** Training capacity can be assembled from whatever machines are free across regions, clouds, and partners, instead of reserved as one enormous block.

---

## Part two — The plumbing behind AI agents

*None of this is visible from a chat box. It is the wiring that turns a model into something that does actual work.*

### 05 · Agents can now work a full shift alone

A research group called METR measures how long a job an AI can finish unsupervised. In 2023 it was about four minutes. By January 2026 the best models were completing work that takes a person more than five hours, and the figure has been doubling roughly every four months. That is why overnight runs became a category: hand over the work in the evening, review what came back in the morning.

**Evidence:** [METR: Time Horizon 1.1](https://metr.org/blog/2026-1-29-time-horizon-1-1/) · [METR: Measuring AI Ability to Complete Long Tasks](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/) · [AI Digest time-horizon tracker](https://theaidigest.org/time-horizons)

> 💡 **What it opens up —** Idle night-time hours turn into working hours, with the results waiting as finished, reviewable work when people arrive.

### 06 · Agents that remember get better with time

A memory layer has grown underneath agents, holding three things: what happened, what is true, and how things are done here. One system stores facts on a timeline, tracking when something became true as well as when it found out; another sorts and de-conflicts facts across a person, a session, and a company; a third lets the agent edit its own notes. Reported accuracy gains reach 18%.

**Evidence:** [Zep temporal knowledge graph paper (arXiv)](https://arxiv.org/abs/2501.13956) · [Mem0 memory architecture paper (arXiv)](https://arxiv.org/abs/2504.19413) · [Letta (MemGPT) documentation](https://docs.letta.com/)

> 💡 **What it opens up —** Software that knows an account's history on day 400 that it could not have known in week one — a tool that improves simply by being used.

### 07 · Company know-how as a folder you can version

Agent Skills, opened as a shared standard in December 2025, packages the way your best people do a task — the checklist, the scripts, the house style — into a folder an agent opens only when that job comes up. Because it is just files, it can be reviewed, approved, and versioned like any other code. The tools from OpenAI, Microsoft, Google, and Cursor all read the same format.

**Evidence:** [Anthropic Agent Skills announcement](https://claude.com/blog/skills) · [Agent Skills open specification](https://agentskills.io/home) · [The New Stack on the Agent Skills standard](https://thenewstack.io/agent-skills-anthropics-next-bid-to-define-ai-standards/) · [The Decoder: Agent Skills published as open standard](https://the-decoder.com/anthropic-publishes-agent-skills-as-an-open-standard-for-ai-platforms/)

> 💡 **What it opens up —** Knowledge that used to live in senior people's heads becomes text every agent follows the same way, in every part of the business.

### 08 · One plug for connecting AI to your systems

The Model Context Protocol is the standard way an agent finds and uses a tool — your database, your ticketing system, your internal service. In December 2025 Anthropic handed it to the Linux Foundation so no single company owns it, with AWS, Google, Microsoft, Bloomberg, and Cloudflare backing the new foundation. Over 10,000 public connectors have been built already.

**Evidence:** [Anthropic: donating MCP to the Agentic AI Foundation](https://www.anthropic.com/news/donating-the-model-context-protocol-and-establishing-of-the-agentic-ai-foundation) · [Linux Foundation press release on the AAIF](https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation) · [MCP blog: joining the Agentic AI Foundation](https://blog.modelcontextprotocol.io/posts/2025-12-09-mcp-joins-agentic-ai-foundation/) · [TechCrunch coverage of the AAIF launch](https://techcrunch.com/2025/12/09/openai-anthropic-and-block-join-new-linux-foundation-effort-to-standardize-the-ai-agent-era/)

> 💡 **What it opens up —** Integration work done once carries across every major AI supplier, so changing model does not mean rebuilding the connections.

---

## Part three — Agents out in the world

*Three standards that let agents work beyond one company's walls — finding each other, paying for things, and proving who they are.*

### 09 · Agents from different companies can find each other

A2A is a standard for agents talking to agents rather than to tools. Each agent publishes a small JSON file — an Agent Card — at a fixed address, listing what it can do and how to authenticate; another agent reads it and hands over work. Google launched it in April 2025 and gave it to the Linux Foundation that June. The first stable version landed in March 2026, and AWS, Microsoft, and Google Cloud all support it in their agent platforms.

**Evidence:** [What A2A is](https://a2a-protocol.org/latest/topics/what-is-a2a/) · [Handover to the Linux Foundation](https://developers.googleblog.com/en/google-cloud-donates-a2a-to-linux-foundation/) · [AWS support in its own docs](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/runtime-a2a.html)

> 💡 **What it opens up —** Work can be split across agents built by different vendors — yours, a partner's, a supplier's — without writing a custom integration for every pair.

### 10 · Agents can hold a budget and settle a bill

Two standards let an agent buy things. Google's AP2 gives it a signed mandate: cryptographic proof of exactly what a person authorised it to spend, so a transaction cannot later be disputed. Google handed AP2 to the FIDO Alliance in April 2026. x402, started at Coinbase, does the settlement — a server answers an unpaid request with HTTP 402, the agent pays, the request retries. Its Linux Foundation body launched in July 2026 with Stripe, Visa, Mastercard, Google, and AWS among the members.

**Evidence:** [x402 Foundation launch](https://x402.org/linux-foundation-announces-operational-launch-of-x402-foundation-to-standardize-internet-native-payments-for-ai-agents-and-applications/) · [Google's AP2 announcement](https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol) · [Stripe's x402 integration](https://docs.stripe.com/payments/machine/x402)

> 💡 **What it opens up —** Machine-to-machine buying with no one clicking a button — an agent paying for data, an API call, or a delivery, inside limits a person set in advance.

### 11 · Every agent gets its own ID card

Microsoft Entra Agent ID, generally available since April 2026, gives each agent a real identity in the company directory instead of a shared service account. The machinery that governs staff then applies: access rules, eight kinds of risk detection, and a joiner-mover-leaver lifecycle. The accountability detail is the interesting one — every agent has a named human sponsor, and if that person leaves, sponsorship transfers automatically to their manager. Agents built on AWS Bedrock or n8n can be enrolled too.

**Evidence:** [What Entra Agent ID is](https://learn.microsoft.com/en-us/entra/agent-id/what-is-microsoft-entra-agent-id) · [Enrolling non-Microsoft agents](https://learn.microsoft.com/en-us/entra/agent-id/configure-third-party-agents) · [Release record](https://learn.microsoft.com/en-us/entra/fundamentals/whats-new)

> 💡 **What it opens up —** Agents can be granted, audited, and switched off like employees, with a named person answerable for each one — the piece that was missing before letting them work unattended.

---

## Part four — Beyond the chatbot

*Things AI can now do that look nothing like the chat window most people picture.*

### 12 · Robots that learn a job from a few demonstrations

Putting a language model behind a robot's hands changed what robots can do. Figure's humanoids, trained on about 500 hours of demonstrations, sorted nearly 50,000 packages across forty hours of unattended work in May 2026, and the company now builds one robot an hour. Google's version runs on the robot itself and picks up a new task from as few as fifty demonstrations.

**Evidence:** [Interesting Engineering — Figure autonomous sorting run](https://interestingengineering.com/ai-robotics/figure-ai-humanoids-24-hour-autonomous-run) · [Figure — Ramping Figure 03 production at BotQ](https://www.figure.ai/news/ramping-figure-03-production) · [Gemini Robotics overview](https://en.wikipedia.org/wiki/Gemini_Robotics)

> 💡 **What it opens up —** A robot that learns a new warehouse or line job by being shown it a few dozen times, rather than a machine built to do one thing forever.

### 13 · AI that produces genuinely new results

Google's AlphaEvolve found a faster way to multiply matrices, beating a record that had stood for 56 years, and recovered 0.7% of Google's worldwide computing capacity. Its co-scientist system proposed existing drugs that might treat liver scarring; researchers tested them and one cut the damage marker by 91%, published in a journal. In both cases the AI proposed at volume and something else checked the answers.

**Evidence:** [DeepMind — AlphaEvolve](https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms/) · [DeepMind — AI co-scientist](https://deepmind.google/blog/co-scientist-a-multi-agent-ai-partner-to-accelerate-research/) · [Advanced Science — AI-assisted drug repurposing for liver fibrosis](https://advanced.onlinelibrary.wiley.com/doi/10.1002/advs.202508751)

> 💡 **What it opens up —** Hard problems with a clear way to score an answer — scheduling, formulations, chip layouts — can be handed to a system that finds improvements nobody on the team proposed.

### 14 · AI that builds worlds for other AI to practise in

Google's Genie 3 turns a sentence into a place you can walk around, drawn live and holding together for minutes at a time. DeepMind now drops its agents into these invented worlds to practise, a loop its chief executive calls endless training. It reached the public in 2026 as Project Genie.

**Evidence:** [DeepMind — Genie 3 announcement](https://deepmind.google/blog/genie-3-a-new-frontier-for-world-models/) · [Google — Project Genie availability](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/project-genie/)

> 💡 **What it opens up —** Practice grounds for robots and software agents can be conjured from a description — a warehouse aisle, a shop floor, a hazardous site — instead of built by hand or borrowed from live operations.

### 15 · A different way of writing text, ten times faster

Almost every AI writes one word at a time. Diffusion models write the whole answer roughly, then sharpen it over a few passes, the way image generators work. Inception's Mercury does this at over 1,000 tokens a second, five to ten times the usual speed, and Google has shown the same approach. Because the speed comes from the method rather than from a smaller model, quality holds up.

**Evidence:** [Inception Labs — Introducing Mercury](https://www.inceptionlabs.ai/blog/introducing-mercury) · [arXiv — Mercury technical report](https://arxiv.org/abs/2506.17298) · [Artificial Analysis — Mercury 2 benchmarks and pricing](https://artificialanalysis.ai/models/mercury-2)

> 💡 **What it opens up —** Anything that answers while a person waits — live voice, inline code suggestions, bulk document work — gets an order of magnitude more room.

---

## Part five — AI that tests software

*Six technologies taking over work that test scripts do today — written in plain language, no background needed. Where a number comes from the company selling the product rather than an independent test, it says so.*

### 16 · Tests written in plain English

Momentic lets a team describe a test the way they would explain it to a colleague — log in, add an item to the basket, check the total. Its software then works out how to do that on screen, and when the app's design changes, it finds the new path instead of failing. The company raised $15 million in November 2025; Notion, Webflow, and Xero are customers.

**Evidence:** [Momentic](https://momentic.ai/blog/series-a) · [TechCrunch](https://techcrunch.com/2025/11/24/momentic-raises-15m-to-automate-software-testing)

> 💡 **What it opens up —** Tests stop breaking every time a button moves, because what you wrote down is the intent, not the button.

### 17 · Nobody writes the tests at all

Meticulous goes further: it quietly records how real people use an app, then turns those recordings into tests by itself. It adds new ones as features ship, retires the ones that no longer apply, and replays them on every code change to show what looks different. No one writes or maintains a single test. Dropbox and Notion use it; the company raised $15 million in July 2026. Its no-flaky-tests claim is its own.

**Evidence:** [Meticulous](https://www.meticulous.ai/)

> 💡 **What it opens up —** The cost of a test suite becomes the cost of running it — the writing and the upkeep disappear.

### 18 · AI now uses a computer about as well as a person

There is a standard exam for this called OSWorld: 369 everyday desktop jobs, like editing a spreadsheet or working across several windows. In April 2024 the best AI finished 12% of them, against about 72% for a human. By February 2026 Anthropic reported roughly 72% for its own models — its own figures, on an updated version of the exam. Google says its teams already use a similar model to test their products.

**Evidence:** [OSWorld exam](https://arxiv.org/abs/2404.07972) · [Anthropic results](https://www.anthropic.com/news/claude-sonnet-4-6) · [Google's model](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/gemini-computer-use-model/)

> 💡 **What it opens up —** Screens that test tools could never reach — desktop software, Citrix, old ERP systems — can now be worked by an agent that looks and clicks the way a tester does.

### 19 · The same skill, running on your own servers

ByteDance gives away UI-TARS, a model that does the same job: it looks at a screenshot and decides where to click, across desktop, browser, and Android. Because anyone can download it, it can run inside a company's own data centre, so screenshots of a client's banking or hospital system never leave the building. Its scores are self-reported, but they sit in the same range as the paid services.

**Evidence:** [UI-TARS](https://github.com/bytedance/ui-tars)

> 💡 **What it opens up —** Agent-driven testing for clients whose data is not allowed to go outside — paid for in servers rather than per use.

### 20 · Tests that prove they catch something

Test writing usually chases coverage: how much of the code was touched. Meta flipped it. Their system first invents a realistic bug — one that leaks private data, say — then writes a test proven to catch that exact bug. Across 10,795 pieces of code in Facebook, Instagram, and WhatsApp, engineers kept 73% of the tests it produced. The work is published in a peer-reviewed paper, which is rare in this field.

**Evidence:** [Meta engineering](https://engineering.fb.com/2025/02/05/security/revolutionizing-software-testing-llm-powered-bug-catchers-meta-ach/) · [Research paper](https://arxiv.org/abs/2501.12862)

> 💡 **What it opens up —** A test suite can be judged by the kinds of bugs it demonstrably catches rather than the lines it touches — which makes something like privacy testing or payment testing a service you can prove.

### 21 · Coverage becomes an overnight job

Adding tests to an old system used to be months of dull work. Now an agent is pointed at the code, writes tests, runs them, and keeps only the ones that pass and genuinely add coverage. Qodo's version had 15 of its tests accepted into a large open-source project. Diffblue does the same for big Java systems without using a language model at all, so the output is predictable enough to run unattended.

**Evidence:** [Qodo](https://github.com/qodo-ai/qodo-cover) · [Diffblue](https://www.diffblue.com/resources/announcing-the-next-generation-of-our-best-in-class-unit-test-generation-platform/)

> 💡 **What it opens up —** Coverage work across hundreds of client systems can run overnight on spare machines and arrive as ready-to-review changes by morning.

---

> **The test of this page** — it earns its keep when one of these comes up in your next planning discussion before it turns up in a supplier's pitch deck.

## 🗺️ The series

This repo is one of four. Together they form **Zero → Frontier**, a complete AI-engineering curriculum:

| Track | For | Repo |
|---|---|---|
| 🌱 **From Zero** | Absolute beginner | [`ai-engineer-from-zero`](https://github.com/MalayThoriaQK/ai-engineer-from-zero) |
| ⚡ **The Fast Track** | Proficient developer | [`ai-engineer-fast-track`](https://github.com/MalayThoriaQK/ai-engineer-fast-track) |
| 🔭 **The Frontier** | Advanced / frontier | [`ai-engineer-frontier`](https://github.com/MalayThoriaQK/ai-engineer-frontier) |
| 📡 **The Radar** | Executive briefing | *(this repo)* |

## 📜 License & credits

Curriculum text is licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — reuse it, adapt it, credit the source. Every linked course, book, video, and repository belongs to its respective creator; this repo curates, it does not host.

Compiled **August 2026**. Links age; skills don't — if a resource here has been replaced by the time you arrive, learn its successor. **Found a dead link? Open an issue or PR.**
