# My Applied AI Engineer / LLMOps Roadmap — v2 (detailed)

> **Goal:** Applied AI Engineer / LLMOps — build LLM products on top of models + serve/operate
> them at scale; fine-tuning when needed. Target titles: *Applied AI Engineer, LLMOps Engineer,
> AI Infrastructure Engineer* (GCCs, well-funded/AI-first startups, YC early-stage).
> **Stance:** Solid ML/DL/NLP **fundamentals** (debug model behavior, pass product-company
> "AI fundamentals" rounds) — *not* researcher depth. Math at an **intuitive/operational** level.
> **Stack:** Python primary; TypeScript a competitive edge (ramp just-in-time); **ignore Rust/Julia**
> code in lessons. Docker/k8s ramped just-in-time.
> **Capacity:** 15 hrs/week, Jun 15 → Oct 30 (~20 weeks). Tooling ramp-up is *inside* the 15h.
> **Profile:** Rusty Python + math, but ramp fast (done before). TypeScript needs more time.

---

## The 4 categories (your rubric)
1. **DO FULLY** — work the whole phase; aim to genuinely understand it.
2. **SELECTIVE** — do the important lessons, skip the rest (lists below).
3. **READ-ALL / GENERAL GRASP** — go over everything, don't sweat every line.
4. **SKIP FOR NOW** — pick up later only if a project needs it.
> (2 + 3 combine = "important, but just read it.")

---

## The reality of the timeline
- Full recommended scope (all 20 phases) ≈ **500+ hrs**. Your window ≈ **250–300 hrs**.
- **In-window (Jun 15–Oct 30):** the critical path → Foundations → NLP/Transformers →
  LLMs-from-scratch (core) → LLM Engineering → Tools/MCP → Agents (core) → Production →
  Practical Security → **start 1 capstone.**
- **Phase 2 (right after Oct 30):** finish/2nd capstone, P12 Multimodal (applied subset),
  P16 Multi-Agent (applied subset), P14 remaining lessons, P10 frontier walkthroughs,
  P18 alignment theory, P17 deep internals, P8/P9 selective. **These are in your roadmap,
  categorized below — they just fall just outside the 20-week window.**

---

## Master table — all 20 phases

| Phase | Name | Lessons | Category | In-window scope (hrs) | In Jun–Oct window? |
|---|---|---:|:---:|---:|:---:|
| P0 | Setup & Tooling | 12 | **2** Selective | 8 (+ Python/Docker ramp) | ✅ |
| P1 | Math Foundations | 22 | **2** Selective (DO-heavy) | 16 | ✅ |
| P2 | ML Fundamentals | 18 | **2** Selective | 12 | ✅ |
| P3 | Deep Learning Core | 13 | **1** Do Fully | 18 | ✅ |
| P4 | Computer Vision | 28 | **4** Skip (read 2 transferable) | ~2 | ⏸ mostly skip |
| P5 | NLP | 29 | **1→2** Do core / skim rest | 26 | ✅ |
| P6 | Speech & Audio | 17 | **4** Skip (Whisper later) | 0 | ⏸ |
| P7 | Transformers Deep Dive | 16 | **1** Do Fully | 28 | ✅ |
| P8 | Generative AI | 15 | **4** Skip for now (DDPM/SD later) | 0 | ⏸ |
| P9 | Reinforcement Learning | 12 | **4→2** Skip; read RLHF concept | ~2 | ⏸ |
| P10 | LLMs from Scratch | 24 | **2** Selective (core DO + frontier READ) | 16 | ✅ |
| P11 | LLM Engineering | 17 | **1** Do Fully | 22 | ✅ |
| P12 | Multimodal AI | 25 | **3** Read-all (applied subset DO) | 0 | ⏭ Phase 2 |
| P13 | Tools & Protocols | 23 | **2** Selective (large DO subset) | 16 | ✅ |
| P14 | Agent Engineering | 42 | **1** Do Fully (core subset in-window) | 28 | ✅ (partial) |
| P15 | Autonomous Systems | 22 | **3** Read-all (ops subset internalize) | 8 | ✅ |
| P16 | Multi-Agent & Swarms | 25 | **2** Selective (applied DO / theory skim) | 0 | ⏭ Phase 2 |
| P17 | Infrastructure & Production | 28 | **1** Do Fully (build key / read rest) | 20 | ✅ |
| P18 | Ethics, Safety & Alignment | 30 | **2** Selective (security DO / theory READ) | 12 | ✅ |
| P19 | Capstone Projects | 17 (+deep-builds) | **2** Selective (build 1–3; skip deep-builds) | 15 (start) | ✅ start |

---

## Per-phase detail (grounded in reading the actual lessons)

### P0 — Setup & Tooling · **Cat 2 (Selective)** · ~8h
**DO:** 01 dev-environment, 05 jupyter, 06 python-environments (uv/venv), 07 **docker-for-ai** (standout — volume mounts, GPU passthrough, docker-compose with Qdrant; production-grade).
**SKIP/skim:** 02 git, 03 gpu-cloud (skim), 04 apis-keys (skim), 08 editor, 09 data-management (later), 10 terminal, 11 linux, 12 debugging (defer). *You pick these up fast / already know most.*

### P1 — Math Foundations · **Cat 2, DO-heavy** · ~16h
**DO (core intuition):** 01 LA-intuition, 02 vectors-matrices, 03 matrix-transforms, 04 calculus, 05 **chain-rule-autodiff** (standout — builds a tiny autograd, trains XOR; bridges to backprop), 06 probability, 08 optimization, 10 dimensionality-reduction, 14 **norms-and-distances** (standout — cosine/Euclidean → why RAG/vector DBs work), 15 statistics-for-ml.
**SKIM:** 07 bayes, 09 information-theory (entropy/cross-entropy/KL — worth a read), 11 SVD.
**SKIP:** 12 tensor-ops, 13 numerical-stability, 16 sampling, 17 linear-systems, 18 convex-opt, 19 complex-numbers, 20 fourier, 21 graph-theory, 22 stochastic-processes. *Research-deep or off-path for applied work.*

### P2 — ML Fundamentals · **Cat 2** · ~12h
**DO:** 01 what-is-ml, 02 linear-regression (from scratch), 09 **model-evaluation** (standout — train/val/test, cross-val, precision/recall/F1/ROC-AUC, leakage; this is your interview + production gold), 13 ml-pipelines (leakage prevention), 10 bias-variance, 12 hyperparameter-tuning.
**READ (concept, minimal code):** 03 logistic-regression, 04 decision-trees, 08 feature-engineering, 11 ensemble-methods.
**SKIP:** 05 SVM, 06 KNN (revisit at RAG), 07 unsupervised (skim k-means), 14 naive-bayes, 15 time-series, 16 anomaly, 17 imbalanced, 18 feature-selection.

### P3 — Deep Learning Core · **Cat 1 (Do Fully)** · ~18h
**DO ALL:** 01 perceptron → 02 mlp → 03 **backprop** (standout — Value autograd, trains XOR by hand) → 04 activations → 05 loss → 06 optimizers → 07 regularization → 08 weight-init → 09 lr-schedules → 10 **mini-framework** (standout — Linear/MLP/loop/optimizers in ~600 lines) → 11 **intro-to-pytorch** (maps everything you built 1:1 to PyTorch).
**SKIM:** 12 intro-to-jax (PyTorch dominates your stack), 13 debugging-nn (revisit when training breaks).

### P4 — Computer Vision · **Cat 4 (Skip for now)** · ~2h
You agreed to skip. **Optional read only:** 14 vision-transformers + 02 convolutions-from-scratch (transferable: ViT shows up in multimodal). Everything else off-path.

### P5 — NLP · **Cat 1→2 (Do core, skim the rest)** · ~26h
**DO:** 01 text-processing, 02 bow-tfidf, 03 word2vec (from scratch), 04 glove-fasttext, 19 subword-tokenization, 08 cnn-rnn-for-text, 09 seq2seq, 10 **attention-mechanism** (foundation for P7), 14 information-retrieval-search, 22 **embedding-models-deep-dive** (standout — dense/sparse/multi-vector, matryoshka, MTEB; critical for RAG), 23 **chunking-strategies-rag** (production RAG), 20 structured-outputs, 27 **llm-evaluation-frameworks** (RAGAS/DeepEval/G-Eval — production quality gates).
**SKIM:** 05 sentiment, 06 NER, 07 pos-parsing, 11 machine-translation, 12 summarization, 13 QA, 16 text-gen, 17 chatbots, 28 long-context-eval.
**SKIP:** 15 topic-modeling, 18 multilingual, 21 NLI, 24 coreference, 25 entity-linking, 26 relation-extraction-kg, 29 dialogue-state.

### P6 — Speech & Audio · **Cat 4 (Skip)** · 0h
Skip. *If a voice product ever appears:* 04 ASR + 05 Whisper-architecture only.

### P7 — Transformers Deep Dive · **Cat 1 (Do Fully)** · ~28h
**DO:** 01 why-transformers, 02 **self-attention-from-scratch** (non-negotiable), 03 multi-head, 04 positional-encoding (incl. RoPE), 05 **full-transformer** (RMSNorm/SwiGLU/RoPE modernizations), 06 BERT, 07 **GPT** (causal LM, sampling/temperature/top-p), 08 T5/BART (read), 12 **KV-cache & flash-attention** (standout — direct to inference/LLMOps), 13 **scaling-laws** (Chinchilla; model/data tradeoffs), 14 build-a-transformer-capstone.
**SKIM:** 09 ViT, 10 audio-whisper, 11 MoE, 15 attention-variants, 16 speculative-decoding.

### P8 — Generative AI · **Cat 4 (Skip for now)** · 0h
Defer. *Phase 2 if needed:* 06 DDPM-from-scratch + 07 latent/stable-diffusion (understand SD internals for fine-tuning). Skip GANs/VAE/video/3D/flow.

### P9 — Reinforcement Learning · **Cat 4→2 (Skip; read RLHF concept)** · ~2h
**Read only:** 09 reward-modeling-rlhf (concept — feeds your understanding of how chat models are aligned). *Phase 2 if going deep into fine-tuning:* 01 MDPs, 06 policy-gradients, 07 actor-critic, 08 PPO. Skip classical RL (Q-learning/DQN/games/sim-to-real).

### P10 — LLMs from Scratch · **Cat 2 (core DO + frontier READ)** · ~16h
**DO (core — your anti-"hollow-architect" insurance):** 01 tokenizers, 02 build-a-tokenizer, 03 data-pipelines, 04 **pre-training-mini-GPT (124M)** (standout — mental model for everything after), 06 instruction-tuning-SFT, 08 **DPO** (2025+ standard; do this over 07 RLHF), 10 evaluation, 11 quantization, 12 inference-optimization.
**READ (awareness):** 05 distributed/FSDP, 14 open-models-architecture-walkthrough (maps Llama/Qwen/Mistral to a few knobs), 07 RLHF.
**SKIP (frontier paper-tours):** 15–22, 25, 34 (NSA, MTP, DualPipe, Jamba, differential-attention, DeepSeek-V3, async-hogwild, gradient-checkpointing). Read in Phase 2 if curious.

### P11 — LLM Engineering · **Cat 1 (Do Fully)** · ~22h
**DO ALL 17:** 01 prompt-eng, 02 few-shot/CoT, 03 structured-outputs, 04 embeddings, 05 context-engineering, 06 **RAG**, 07 **advanced-RAG** (rerank/hybrid/query-transform), 08 LoRA/QLoRA fine-tuning, 09 **function-calling**, 10 evaluation, 11 caching/cost, 12 guardrails, 13 **production-app (FastAPI/TS, monitoring, e2e)**, 14 **MCP**, 15 prompt-caching, 16 langgraph, 17 framework-tradeoffs (read). *This phase IS the job description. No skips.*

### P12 — Multimodal AI · **Cat 3 (Read-all; applied subset DO)** · Phase 2
**DO (applied subset, Phase 2):** 01 ViT/patch-tokens, 05 LLaVA visual-instruction-tuning, 23 **ColPali vision-native RAG**, 24 multimodal-RAG, 25 multimodal-agents/computer-use.
**READ:** 02 CLIP, 03 BLIP-2 Q-Former, 04 Flamingo, 22 document-understanding.
**SKIM/skip:** the VLM architecture tour (06–21). *Doesn't fit the window; first up in Phase 2.*

### P13 — Tools & Protocols · **Cat 2 (large DO subset)** · ~16h
**DO:** 01 tool-interface, 02 function-calling-deep-dive, 03 parallel/streaming-tool-calls, 04 structured-output, 05 tool-schema-design, 06 MCP-fundamentals, 07 **building-an-MCP-server**, 08 building-an-MCP-client, 09 MCP-transports, 10 MCP-resources-and-prompts.
**READ:** 13 async-tasks, 15 security/tool-poisoning, 16 OAuth-2.1, 20 OpenTelemetry-GenAI.
**SKIP/defer:** 11 sampling, 12 roots/elicitation, 14 MCP-apps, 17 gateways/registries, 18 auth-production, 19 A2A, 21 routing, 22 skills/SDKs, 23 capstone.

### P14 — Agent Engineering · **Cat 1 (Do Fully; core subset in-window)** · ~28h in-window
**Sub-themes (read the subagent's full breakdown):**
- **01–12 Reasoning & core (DO, ~8h):** agent-loop(01), rewoo(02), reflexion(03), tot/lats(04), self-refine(05), tool-use(06), memory(07–09), skill-libraries(10), planning(11), **anthropic-workflow-patterns(12)**.
- **13–18 Frameworks (DO 2 deeply, ~6h):** **langgraph(13)** + **claude-agent-sdk(17)** deep; skim autogen(14)/crewai(15)/openai-sdk(16)/agno-mastra(18).
- **25–30 Safety/evals (DO, ~5h):** multi-agent-debate(25), **failure-modes(26)**, **prompt-injection-defense(27)**, orchestration(28), production-runtimes(29), **eval-driven-development(30)**.
- **31–42 Workbench (DO core, ~7h in-window; rest Phase 2):** 31 why-models-fail, 32 minimal-workbench, 38 verification-gates, 39 reviewer-agent, 40 multi-session-handoff (the highest-ROI subset; finish 33–37, 41–42 in Phase 2).
- **19–24 Benchmarks/observability (READ, ~2h):** 19 swebench/gaia + 23 OTel-conventions + 24 observability-platforms; skim 20; **skip** 21 computer-use, 22 voice-agents.

### P15 — Autonomous Systems · **Cat 3 (Read-all; ops subset internalize)** · ~8h
**Internalize:** 10 claude-code-permission-modes, 12 durable-execution, 13 cost-governors, 14 kill-switches/canaries, 15 HITL-propose-then-commit, 16 checkpoints/rollback, 21 METR-external-evaluation.
**General grasp (fast read):** the self-improvement / alignment-policy lessons (01–09, 11, 17–20, 22).

### P16 — Multi-Agent & Swarms · **Cat 2 (applied DO / theory skim)** · Phase 2
**DO (applied, Phase 2):** 05 supervisor/orchestrator, 10 group-chat, 11 handoffs, 12 A2A, 13 shared-memory/blackboard, 22 production-scaling, 23 failure-modes/MAST, 24 evaluation, 25 case-studies-2026.
**SKIM:** 04 primitive-model, 06 hierarchical, 08 role-specialization, 09 parallel-swarm.
**SKIP:** 02 FIPA-ACL, 03 protocols, 14 BFT, 15 voting-topology, 16 negotiation, 17 generative-sim, 18 theory-of-mind, 19 PSO/ACO, 20 MARL, 21 agent-economies. *Overlaps P14; first up in Phase 2.*

### P17 — Infrastructure & Production (LLMOps) · **Cat 1 (Do Fully; build key / read rest)** · ~20h
**DO/internalize:** 01 managed-platforms, 04 vLLM-internals (PagedAttention/continuous-batching), 08 **inference-metrics (TTFT/TPOT/goodput/P99)**, 13 observability-stack, 14 **prompt/semantic-caching** (60–90% cost leverage), 15 batch-APIs, 19 AI-gateways, 22 **load-testing (build)**, 23 SRE-for-AI, 27 **FinOps/unit-economics**.
**READ for decisions:** 02–03, 05–07, 09–12, 16–18, 20–21, 24–26, 28.
**Needs external hands-on:** vLLM deploy, k8s autoscaling, load test against a live endpoint (ramp Docker/k8s here).

### P18 — Ethics, Safety & Alignment · **Cat 2 (security DO / theory READ)** · ~12h
**DO (practical security):** 12 red-teaming/PAIR, 13 many-shot-jailbreak, 15 **indirect-prompt-injection** (the #1 2026 production threat), 16 **red-team-tooling (Garak/Llama-Guard/PyRIT)**, 23 watermarking, 25 EchoLeak-CVEs (read), 29 moderation-systems, 30 dual-use (read).
**READ (awareness):** alignment theory 01–11 (RLHF pathologies, sleeper agents, alignment-faking), 17–22, 24, 26–28.
**SKIP:** 14 ASCII-art-jailbreaks.

### P19 — Capstone Projects · **Cat 2 (build 1–3; skip deep-builds)** · start in-window
**Build (portfolio) — recommended for your infra/LLMOps profile:**
1. **02 RAG over Codebase** (~30h) — *best first build.* Semantic search, AST/tree-sitter, hybrid retrieval, reranking, citations. High employer signal (Cursor/Sourcegraph-style).
2. **08 Production RAG Chatbot, regulated** (~30h) — compliance, multi-layer guardrails, drift monitoring, caching at scale. Most-deployed 2026 shape.
3. **11 LLM Observability/Eval Dashboard** (~25h) — OTel ingest, evals, cost attribution (plays to infra background).
- *Optional/Phase 2:* 06 K8s DevOps agent (great Cohesity fit), 01 terminal coding agent (highest signal, but TS-heavy), 16 GitHub issue→PR agent.
**SKIP the deep-build tracks (20–87):** redundant re-implementations of what you already built in P5/P7/P10/P11/P13/P14. Capstone 02 covers the RAG deep-builds more efficiently.

---

## Just-in-time ramp-up plan (inside the 15h, synchronous)
- **Week 1:** Python refresh + Docker basics (you ramp fast). Enough to run notebooks + containerized model API.
- **Before P11/P13 (Week 13):** light **FastAPI _or_ TypeScript** API ramp (~3h). Pick one; Python/FastAPI is lower-effort for you now, TS is the competitive edge for later.
- **Before P17 (Week 18):** Docker Compose + minimal **k8s** concepts (~3h) for serving/load-testing.
- **TypeScript proper:** defer to Phase 2 unless you choose a TS capstone — budget real time for it then.

---

# Week-by-week schedule · Jun 15 → Oct 30 · ~15 hrs/week

> ~14 hrs content + ~1 hr buffer per week. Two designated lighter/catch-up weeks (W7, W12)
> absorb slippage since you're ramping rusty foundations. Each week ends with a **shippable
> artifact** (the course's per-lesson outputs + your own repo). Adjust freely.

### PART A — Foundations (Weeks 1–5)
**W1 · Jun 15–21 · Setup + ramp.** P0 (01,05,06,07) + Python/Docker refresh.
→ *Artifact:* working env; a Dockerized "hello-LLM" API call.
**W2 · Jun 22–28 · Math I.** P1: 01 LA-intuition, 02 vectors-matrices, 03 matrix-transforms, 04 calculus, 05 chain-rule-autodiff.
→ *Artifact:* tiny autograd engine; XOR trained by hand.
**W3 · Jun 29–Jul 5 · Math II.** P1: 06 probability, 08 optimization, 10 dim-reduction, 14 norms-distances, 15 statistics; skim 09 info-theory.
→ *Artifact:* cosine-vs-Euclidean retrieval demo; gradient-descent visualizer.
**W4 · Jul 6–12 · ML fundamentals.** P2: 01, 02 linear-regression, 03 logistic (read), 09 model-evaluation, 10 bias-variance, 13 ml-pipelines; read 08,11.
→ *Artifact:* regression from scratch + a clean eval/cross-val notebook (interview-ready).
**W5 · Jul 13–19 · Deep Learning I.** P3: 01 perceptron, 02 mlp, 03 backprop, 04 activations, 05 loss.
→ *Artifact:* backprop from scratch.

### PART B — DL finish + NLP + Transformers start (Weeks 6–9)
**W6 · Jul 20–26 · Deep Learning II.** P3: 06 optimizers, 07 regularization, 08 weight-init, 09 lr-schedules, 10 mini-framework, 11 PyTorch; skim 12 JAX, 13 debugging.
→ *Artifact:* mini-framework + the same net rebuilt in PyTorch.
**W7 · Jul 27–Aug 2 · BUFFER / catch-up + NLP I.** Catch up on anything slipping; then P5: 01 text-processing, 02 bow-tfidf, 03 word2vec.
→ *Artifact:* word2vec from scratch.
**W8 · Aug 3–9 · NLP II.** P5: 04 glove-fasttext, 19 subword-tokenization, 08 cnn-rnn-text, 09 seq2seq, 10 attention-mechanism.
→ *Artifact:* attention mechanism notebook (sets up P7).
**W9 · Aug 10–16 · NLP III (RAG-relevant) + Transformers I.** P5: 14 IR-search, 22 embedding-models-deep-dive, 23 chunking-for-RAG, 20 structured-outputs, 27 llm-eval-frameworks (skim 05,06,12,13). Then P7: 01 why-transformers.
→ *Artifact:* embeddings + chunking experiment with a retrieval metric.

### PART C — Transformers + LLMs from scratch (Weeks 10–12)
**W10 · Aug 17–23 · Transformers II.** P7: 02 self-attention, 03 multi-head, 04 positional-encoding, 05 full-transformer.
→ *Artifact:* self-attention + a transformer block from scratch.
**W11 · Aug 24–30 · Transformers III.** P7: 06 BERT, 07 GPT, 08 T5/BART (read), 12 KV-cache/flash-attention, 13 scaling-laws, 14 build-transformer-capstone; skim 09–11,15,16.
→ *Artifact:* a working small transformer (capstone 14).
**W12 · Aug 31–Sep 6 · BUFFER + LLMs-from-scratch I.** Catch-up; then P10: 01 tokenizers, 02 build-a-tokenizer, 03 data-pipelines, 04 pre-train-mini-GPT.
→ *Artifact:* BPE tokenizer + a tiny pre-trained GPT.

### PART D — LLM engineering core (Weeks 13–14)
**W13 · Sep 7–13 · LLMs-from-scratch II + LLM-Eng start.** P10: 06 SFT, 08 DPO, 11 quantization, 12 inference-opt, 10 eval; read 14 open-models. Then P11: 01 prompt-eng, 02 few-shot/CoT. *(FastAPI/TS ramp ~3h.)*
→ *Artifact:* SFT + DPO on a small model.
**W14 · Sep 14–20 · LLM Engineering (the job).** P11: 03 structured-outputs, 04 embeddings, 05 context-eng, 06 RAG, 07 advanced-RAG, 09 function-calling, 10 eval, 11 caching/cost, 12 guardrails, 13 production-app; (08 LoRA, 14 MCP, 15 prompt-caching, 16 langgraph spill to W15 if needed).
→ *Artifact:* **a deployed RAG app with evals + cost tracking** (your first portfolio piece).

### PART E — Tools/MCP + Agents (Weeks 15–17)
**W15 · Sep 21–27 · Tools & MCP.** Finish P11 (14 MCP, 08 LoRA). P13: 01–10 (tool interface → MCP server/client → transports → resources); read 15,16,20.
→ *Artifact:* a working MCP server + client your agent calls.
**W16 · Sep 28–Oct 4 · Agents I.** P14: 01 agent-loop, 02 rewoo, 03 reflexion, 04 tot/lats, 05 self-refine, 06 tool-use, 07–09 memory, 12 workflow-patterns.
→ *Artifact:* agent loop + memory from scratch.
**W17 · Oct 5–11 · Agents II.** P14: 13 langgraph + 17 claude-agent-sdk (deep); 26 failure-modes, 27 prompt-injection, 30 eval-driven, 28 orchestration; workbench 31,32,38,39,40; read 19,23,24.
→ *Artifact:* an agent with verification gates + a separate reviewer agent.

### PART F — Production + Security + Capstone (Weeks 18–20)
**W18 · Oct 12–18 · Production / LLMOps.** *(Docker/k8s ramp ~3h.)* P17: 01,04,08,13,14,15,19,22 (build load-test),23,27; read the rest.
→ *Artifact:* load-test report + observability wiring (TTFT/TPOT/cost dashboards).
**W19 · Oct 19–25 · Security + Autonomous ops.** P18: 12,13,15,16,23,29 (do), 25,30 (read), skim 01–11. P15: internalize 10,12,13,14,15,16,21; skim the rest.
→ *Artifact:* a red-team/guardrail harness (Garak/PyRIT + injection tests) on your RAG app.
**W20 · Oct 26–30 · Capstone kickoff + review.** Start **Capstone 02 (RAG over Codebase)** — scope, scaffold, first working slice. Review the 20 weeks; write a portfolio README.
→ *Artifact:* capstone repo scaffolded + first end-to-end slice; a portfolio summary.

> **Capstone completion + 2nd capstone run past Oct 30** — that's the start of Phase 2.

---

## Phase 2 (right after Oct 30) — in priority order
1. **Finish Capstone 02**, then build **Capstone 08** (regulated RAG) or **11** (observability).
2. **P14 remaining** workbench lessons (33–37, 41, 42 — ship the reusable pack).
3. **P16 applied subset** (supervisor, group-chat, handoffs, A2A, shared-memory, production-scaling, failure-modes).
4. **P12 applied subset** (ViT, LLaVA, ColPali, multimodal-RAG, computer-use).
5. **P10 frontier walkthroughs** + **P8 DDPM/SD** + **P9 PPO/RLHF** — only if a project pulls you there.
6. **P18 alignment theory** deep read; **P17 deep internals** (TensorRT, disaggregated prefill, edge).
7. **TypeScript** proper (for user-facing AI features / TS-based agent runtimes).

## Guardrails (so depth doesn't kill momentum)
- **Ship from W14 onward.** A deployed app + eval rigor + cost numbers beats theory on a resume.
- **Always measure:** RAG recall, eval scores, per-conversation cost. "No metrics" = toy-project signal.
- **Track frontier-model changelogs** (Anthropic/OpenAI) weekly — a named 2026 hiring signal.
- **Don't let math stall you.** If a P1 lesson isn't clicking in one sitting, note it and move on; a later phase makes it concrete.
- **Interview prep angle:** product companies probe AI fundamentals + "debug this hallucinating agent / is this RAG retrieving relevant context?" — your foundations (P1–P3, P5, P7) + evals (P5-27, P11-10, P14-30) are exactly what answer those.
- **Job targeting:** Applied AI / LLMOps / AI-Infra titles at GCCs (Microsoft/Google/Walmart Global Tech), AI-first/well-funded startups, YC early-stage. Go to buildathons; meet founders.

---

# How to study (evidence-based) — read this before Week 1

The hardest part isn't the material; it's *the method*. Here's what the research actually
supports, turned into a system for this specific course and your weekly slots. The headline:
**learning is an output activity, not an input activity.** Reading/watching feels productive
but is among the *least* effective things you can do. The two techniques with "high utility"
in the research (Dunlosky's review, confirmed by a 242-study meta-analysis) are **practice
testing (active recall)** and **spaced practice**. Highlighting, rereading, and summarizing
rated **low utility** — they create a "fluency illusion" where familiarity feels like mastery.
Concretely: learners who *recalled* material kept ~80% after a week vs ~34% for rereaders.

## 1. Should you "just follow the author"? No — add a retrieval layer.
Following instructions linearly is exactly how people get stuck in "tutorial hell": your brain
does *recognition* ("yes, that makes sense") and mistakes it for *recall* (being able to produce
it yourself). The course's MOTTO → PROBLEM → CONCEPT → BUILD IT → USE IT → SHIP IT loop is
excellent **input**; you must bolt **output** onto it. Per-lesson protocol:

> **The 6-step lesson loop (use this every lesson):**
> 1. **Read CONCEPT once** (passive). Don't take notes yet — just understand.
> 2. **Close it. Explain it out loud / on paper in your own words** (Feynman). Where you stutter = your real gap. *This is the note-trigger.*
> 3. **Predict the BUILD before reading the solution** — "how would I implement attention?" Sketch the approach.
> 4. **Build it** following the lesson. Struggle first, peek when stuck. (The struggle *is* the learning.)
> 5. **Re-implement the core from a blank file, from memory.** Compare to the solution. Repeat until it flows. *This is the single highest-value activity for code.*
> 6. **Ship the artifact** (the lesson's output) + write 3–5 lines: what it does, why it works, one gotcha.
>
> Aim for the **20/80 rule**: ~20% of time reading/concept, ~80% building & recalling.

## 2. Notes: what to write down (and what NOT to)
Don't transcribe. The code is already in the repo — copying it is busywork that *feels* like
learning. Write **in your own words** or don't write it. Keep these **four artifacts** (all
markdown, in a `notes/` folder or your own repo):

**✅ DO note:**
- **The one-line mental model** of each concept, in your words ("attention = a soft, learned lookup table over tokens").
- **The *why* behind a design choice** ("why scale by √d_k? to keep softmax gradients sane").
- **Gotchas & bugs you hit + the fix** — your personal debugging log. This is gold and uniquely yours.
- **Connections** ("this is just the chain rule from P1-05 applied to layers").
- **"Look up later" pointers** — API names, library functions. Awareness > memorization.

**❌ DON'T note:**
- Full code blocks (they're in the repo — link to the file instead).
- Definitions you can Google in 5 seconds.
- Anything you understood instantly (noting it wastes a recall opportunity).

**The four note artifacts:**
| Artifact | What goes in it | When |
|---|---|---|
| **Lesson note** (one per lesson, ~5–10 lines) | mental model, the *why*, one gotcha, link to your code | end of each lesson (step 6) |
| **Concept ledger** (one running file) | the running list of "things that clicked" + cross-links | weekly cleanup |
| **Anki deck** (flashcards) | Q→A for interview-cold facts & "why" questions (see §3) | as you go; review daily |
| **Debug log** (one running file) | error → cause → fix, for every non-trivial bug | whenever you get stuck |

## 3. Active recall + spaced repetition = your retention engine (Anki)
This is non-negotiable and it's *cheap* (10 min/day). Make flashcards as you learn, review them
daily; the algorithm resurfaces a card right as you're about to forget it (spaced repetition
boosts long-term retention up to ~200% vs cramming). **Card-worthy items** for this course:
- "Why does X work?" (e.g., *why does RAG reduce hallucination?*, *why AdamW over SGD?*)
- Definitions you'll need cold in a product-company interview (precision vs recall, TTFT vs TPOT, what KV-cache saves).
- Formula intuitions (cross-entropy, cosine similarity), **not** derivations.
- One card per "gotcha" from your debug log.
Keep cards atomic (one idea each) and phrased as questions. This *is* your interview prep — it
accumulates silently over 20 weeks.

## 4. Your three slots — match the task to your energy
Don't do "constant medium." Research is clear: **batch tasks by energy type** — demanding work
in energy peaks, light work in dips — and work in **ultradian cycles** (~90 min focus, then a
real 15–20 min break: move, no screens; 10 min of light activity restores focus to ~90% vs ~60%
for sitting). Map that onto your blocks:

| Slot | Energy | Do THIS (task type) | Course mapping |
|---|---|---|---|
| **Weekday — ACTIVE block** | Peak / high focus | The hardest *new* concept + **BUILD IT** from scratch; deliberate practice on a weak spot; re-implement-from-memory (step 5). One 90-min sprint, hardest thing first. | P3 backprop, P7 self-attention, P10 tokenizer/pre-train, P11 RAG, P13 MCP server, capstone builds |
| **Weekday — PASSIVE block** | Low / medium | **CONCEPT reading** (step 1), **READ-category** lessons, **USE IT** (run the library version), Anki review, note cleanup, watching a supporting talk, skimming docs. Low stakes, low willpower. | P15 autonomous, P18 alignment theory, P10 frontier walkthroughs, P17 "read-for-decisions" lessons, concept narratives |
| **Weekend — 8–10 hrs** | Mixed (long) | **One long integrative BUILD/SHIP task** for flow + visible progress (this is the motivation driver) — but *structured as 4–5 ultradian sprints*, hardest-first in the morning, a lighter **review/notes sprint in the post-lunch dip**, and one sprint for **spaced review** of the week. | finish a phase's build, the weekly artifact, capstone work |

**On your specific question** (alternate high/low vs constant medium vs long-task-for-flow):
the answer is a **hybrid** — pick a **long task for flow** on weekends (long tasks are what
produce flow and the sense of progress that keeps you motivated), but **don't grind it flat**:
slice it into 90-min sprints, front-load the hard parts to your morning peak, and drop a
low-focus sprint (review, notes, USE-IT, Anki) into the early-afternoon trough. That gives you
flow *and* respects the energy curve, which is how you sustain 10 hours without burning out.
Never sacrifice sleep for hours — no technique compensates for it, and "good enough" focused
sprints beat checked-out grinding.

## 5. Weekly rhythm (the spacing that makes it stick)
- **Daily:** 10 min Anki (active recall + spacing) — even on light days.
- **Each weekend:** 1 sprint reviewing *last 1–2 weeks'* builds — re-implement one core piece from memory cold. This is interleaving + spacing; it's why the buffer weeks (W7, W12) exist.
- **End of each Part (A–F):** a 30-min "teach it back" — explain the whole part to an imaginary interviewer (or rubber duck). Gaps you find → new Anki cards.
- **Interleave**, don't block: revisiting earlier topics while learning new ones beats finishing one thing and never touching it again.

## 6. Anti-patterns to delete
- ❌ Rereading / highlighting and feeling productive (low utility — it's the fluency illusion).
- ❌ Copy-pasting the lesson's code and running it = recognition, not recall. Always re-type/re-derive.
- ❌ Watching/reading 5 lessons ahead without building any. Input without output.
- ❌ Perfectionist notes (pretty Notion pages). Notes are a recall tool, not an artifact.
- ❌ Marathon sessions with no breaks. Past ~90 min focus quality falls off a cliff.

> **Sources:** [Dunlosky high-utility techniques](https://theasrj.com/articles/studytechniques) · [Active recall & spaced repetition evidence](https://recallify.ai/evidence-for-active-recall-and-spaced-repetition/) · [Escaping tutorial hell / recognition-vs-recall](https://algocademy.com/blog/why-youre-stuck-in-tutorial-hell-even-after-completing-10-courses/) · [Deliberate practice for programmers](https://medium.com/@kaungzinhein/deliberate-practice-for-programmers-e0fffb06fd0a) · [Note-taking while learning to code](https://blog.stackademic.com/how-to-take-notes-efficiently-while-learning-to-code-62cd852849a4) · [Ultradian rhythms / 90-min cycles](https://www.asianefficiency.com/productivity/ultradian-rhythms/) · [Energy-type task batching](https://wintechub.com/time-blocking-deep-work-and-energy-management-for-knowledge-workers/) · [Focus in long sessions / breaks](https://www.revisiondojo.com/blog/how-to-stay-focused-during-long-study-sessions)
