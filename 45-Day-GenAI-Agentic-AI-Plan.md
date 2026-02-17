# 90-Day Learning Plan: Generative AI (45 Days) + Agentic AI (45 Days)

Two complete 45-day plans: first Generative AI, then Agentic AI. Each is structured day-by-day with clear objectives, activities, and notes.

---

# Part 1: Generative AI — 45-Day Plan

## Phase 1A: Foundations (Days 1–15)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **1** | Introduction to Generative AI | Define Gen AI; distinguish from discriminative AI; list domains (text, image, audio) | Read 2 overview articles; list 5 real-world Gen AI applications | LLMs, image gen, code gen, speech | [Tutorial](#) | [Assignment](#) |
| **2** | History & Evolution | From rule-based to neural to transformers; key milestones | Timeline of Gen AI (2014–present); note GPT, DALL·E, etc. | GANs, VAEs, diffusion, transformers | [Tutorial](#) | [Assignment](#) |
| **3** | Probability & Language Modeling | Next-token prediction, conditional probability, perplexity | Compute simple bigram/trigram stats on a small corpus | Foundation for how LLMs are trained | [Tutorial](#) | [Assignment](#) |
| **4** | Neural Networks for Sequence Data | RNNs, LSTMs; limitations (long-range dependency) | Study RNN/LSTM diagrams; note vanishing gradients | Why transformers replaced RNNs | [Tutorial](#) | [Assignment](#) |
| **5** | Attention Mechanism | Self-attention, query/key/value, scaled dot-product | Implement or trace attention for 3 tokens on paper | Core of transformer architecture | [Tutorial](#) | [Assignment](#) |
| **6** | Transformer Architecture | Encoder vs decoder; multi-head attention; feed-forward layers | Read “Attention Is All You Need” summary; draw encoder block | Positional encoding, layer norm | [Tutorial](#) | [Assignment](#) |
| **7** | Tokenization | BPE, WordPiece, sentencepiece; vocab size, subwords | Tokenize 10 sentences with tiktoken or similar; inspect tokens | Trade-off: vocab size vs sequence length | [Tutorial](#) | [Assignment](#) |
| **8** | Pre-training Objectives | Causal LM, masked LM; next-sentence prediction | Compare GPT-style (causal) vs BERT-style (bidirectional) | Autoregressive vs encoder-only | [Tutorial](#) | [Assignment](#) |
| **9** | Model Families Overview | GPT, LLaMA, Mistral, Claude, Gemini; open vs closed | Create comparison table: size, context, license, best use | Commercial vs open-weight models | [Tutorial](#) | [Assignment](#) |
| **10** | Scaling Laws & Capabilities | How performance scales with size, data, compute | Read scaling law summaries; note emergent abilities | Chinchilla, Gopher, GPT-4 style scaling | [Tutorial](#) | [Assignment](#) |
| **11** | Prompting Fundamentals | Instructions, few-shot, zero-shot; clarity and format | Write 5 prompts: classification, extraction, summarization, Q&A, generation | Be explicit; show desired format | [Tutorial](#) | [Assignment](#) |
| **12** | Advanced Prompting | Chain-of-thought, role-playing, step-by-step, structured output | Implement CoT for math; request JSON/XML output from model | Zero-shot CoT: “Let’s think step by step” | [Tutorial](#) | [Assignment](#) |
| **13** | Prompt Engineering Patterns | Templates, variables, delimiters; handling long context | Build a reusable prompt template with 3 variables | System vs user vs assistant messages | [Tutorial](#) | [Assignment](#) |
| **14** | In-Context Learning | Why few-shot works; limitations (context length, consistency) | Test 0-shot vs 3-shot vs 5-shot on same task | When to use few-shot vs fine-tuning | [Tutorial](#) | [Assignment](#) |
| **15** | Evaluation of Text Generation | Fluency, coherence, relevance, factual accuracy | Define metrics for one use case; score 5 sample outputs | BLEU, ROUGE, human eval, LLM-as-judge | [Tutorial](#) | [Assignment](#) |

---

## Phase 1B: RAG, Embeddings & Retrieval (Days 16–25)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **16** | When to Use RAG | Limits of model knowledge; need for up-to-date/private data | List 3 problems best solved by RAG vs pure LLM | Hallucination reduction, grounding | [Tutorial](#) | [Assignment](#) |
| **17** | RAG Pipeline Overview | Indexing (chunk → embed → store) and query (embed → retrieve → generate) | Draw end-to-end RAG diagram; list all components | Retrieval + augmentation + generation | [Tutorial](#) | [Assignment](#) |
| **18** | Embedding Models | What embeddings are; sentence vs token embeddings; model choice | Generate embeddings for 20 sentences; compare similarity | OpenAI, Cohere, open-source (e.g., sentence-transformers) | [Tutorial](#) | [Assignment](#) |
| **19** | Chunking Strategies | Fixed size, sentence, semantic chunking; overlap | Chunk a 10-page doc 3 ways; compare retrieval quality | Chunk size vs context window | [Tutorial](#) | [Assignment](#) |
| **20** | Vector Databases | Indexing, approximate nearest neighbor, filters | Set up Pinecone/Chroma/FAISS; index 100 docs; run queries | HNSW, IVF; metadata filters | [Tutorial](#) | [Assignment](#) |
| **21** | Building a Minimal RAG | Load docs → chunk → embed → store; query → retrieve → prompt → generate | Build RAG for one PDF or small doc set | End-to-end script or notebook | [Tutorial](#) | [Assignment](#) |
| **22** | Retrieval Quality | Precision, recall; hybrid (keyword + vector); reranking | Add keyword fallback or reranker; measure improvement | BM25 + vector; cross-encoder rerankers | [Tutorial](#) | [Assignment](#) |
| **23** | Query Understanding | Query expansion, hypothetical document embedding (HyDE) | Implement query expansion or HyDE; compare retrieval | When to rewrite vs use query as-is | [Tutorial](#) | [Assignment](#) |
| **24** | RAG Evaluation | Faithfulness, relevance, answer correctness | Define 3 metrics; run on 10 Q&A pairs | Ground truth vs LLM-generated reference | [Tutorial](#) | [Assignment](#) |
| **25** | RAG Best Practices | Chunk size, top-k, context ordering, citation | Tune your RAG: vary k and chunk size; add “cite sources” | Document ordering in prompt | [Tutorial](#) | [Assignment](#) |

---

## Phase 1C: Training, Fine-Tuning & APIs (Days 26–38)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **26** | API Basics (OpenAI, Anthropic, etc.) | Authentication, request/response, rate limits | Call completion API from code; handle errors and retries | API keys, model names, parameters | [Tutorial](#) | [Assignment](#) |
| **27** | Streaming Completions | Token-by-token streaming; UX and parsing | Build a small app that streams and displays output | SSE or SDK streaming | [Tutorial](#) | [Assignment](#) |
| **28** | Function Calling / Tool Use (API) | Define tools; parse model response; execute and feed back | Implement 2 tools (e.g., get_weather, search); one round-trip | Schema design; when to use tools | [Tutorial](#) | [Assignment](#) |
| **29** | Token Counting & Cost | Input vs output tokens; pricing by model; estimation | Count tokens for 10 prompts; estimate monthly cost | tiktoken; cache for repeated prefixes | [Tutorial](#) | [Assignment](#) |
| **30** | Fine-Tuning Overview | When to fine-tune vs prompt; full vs parameter-efficient | Read comparison; list pros/cons for your use case | Data quality and quantity needs | [Tutorial](#) | [Assignment](#) |
| **31** | Data for Fine-Tuning | Format (instruction/response); quality; diversity | Create 50 example pairs in standard format | JSONL; consistency and variety | [Tutorial](#) | [Assignment](#) |
| **32** | Full Fine-Tuning Concepts | Training loop; loss; overfitting; validation | Study training curve; define train/val split | Compute and data requirements | [Tutorial](#) | [Assignment](#) |
| **33** | Parameter-Efficient Methods | LoRA, QLoRA; adapters; what gets trained | Read LoRA paper summary; compare trainable params | Rank, alpha; base model frozen | [Tutorial](#) | [Assignment](#) |
| **34** | Fine-Tuning in Practice | Use OpenAI fine-tuning or Hugging Face PEFT | Fine-tune a small model on 100+ examples (or use sandbox) | Epochs, batch size, learning rate | [Tutorial](#) | [Assignment](#) |
| **35** | Evaluation After Fine-Tuning | Holdout set; before/after comparison; drift | Evaluate on 20 held-out examples; compare to base model | Avoid test leakage | [Tutorial](#) | [Assignment](#) |
| **36** | Hallucinations & Mitigation | Causes; grounding; citations; confidence | Compare grounded (RAG) vs ungrounded answers; add citation | Factual consistency metrics | [Tutorial](#) | [Assignment](#) |
| **37** | Safety & Alignment | Toxicity, bias, jailbreaks; red-teaming; content filters | Run simple red-team prompts; use content moderation API | Input/output filtering | [Tutorial](#) | [Assignment](#) |
| **38** | Responsible Deployment | Transparency, human oversight, documentation | Draft a one-pager: intended use, limitations, contact | Terms of use, monitoring | [Tutorial](#) | [Assignment](#) |

---

## Phase 1D: Advanced Topics & Capstone (Days 39–45)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **39** | Multimodal Models | Text + image in/out; use cases (vision, diagram understanding) | Call a vision API (e.g., describe image, answer questions) | GPT-4V, Gemini, LLaVA-style models | [Tutorial](#) | [Assignment](#) |
| **40** | Long Context & Retrieval | Long context windows; when to use retrieval anyway | Compare “stuff all in context” vs RAG for 50-page doc | Cost, latency, attention limits | [Tutorial](#) | [Assignment](#) |
| **41** | Model Selection & Trade-offs | Capability vs cost vs latency vs privacy | Build a decision table: 5 use cases × 3 model options | Open vs closed; on-prem options | [Tutorial](#) | [Assignment](#) |
| **42** | Caching & Optimization | Prompt caching; batch inference; speculative decoding | Enable caching for repeated system prompt; measure savings | Cache hit rates; vendor support | [Tutorial](#) | [Assignment](#) |
| **43** | Gen AI Project Lifecycle | Scoping, data, prompt/retrieval/fine-tune, eval, deploy | Document one full project from idea to deployment | Version prompts and models | [Tutorial](#) | [Assignment](#) |
| **44** | Gen AI Capstone Design | Choose application; define scope, data, metrics, risks | Write 2-page capstone design (RAG app or fine-tuned assistant) | Success criteria and guardrails | [Tutorial](#) | [Assignment](#) |
| **45** | Gen AI Capstone Build & Review | Implement and test; document results and learnings | Build capstone; run eval; write retrospective | What worked; what you’d do differently | [Tutorial](#) | [Assignment](#) |

---

# Part 2: Agentic AI — 45-Day Plan

## Phase 2A: Agent Foundations (Days 1–15)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **1** | What Is an AI Agent? | Define agent: autonomy, perception, action, goals | Compare “single API call” vs “agent loop” for same task | Tools, memory, planning, feedback | [Tutorial](#) | [Assignment](#) |
| **2** | Agents vs Traditional Automation | Scripts vs rule-based vs LLM-based agents | List 3 tasks: which need an agent vs simple API? | When flexibility and reasoning matter | [Tutorial](#) | [Assignment](#) |
| **3** | Agent Architecture Overview | Sense → think → act → observe loop; components | Draw full agent loop; label: LLM, tools, memory, state | ReAct, plan-and-execute patterns | [Tutorial](#) | [Assignment](#) |
| **4** | Tools & Capabilities | Tools as functions; schema (name, description, parameters) | Define 3 tools on paper: name, description, JSON schema | Clear descriptions improve tool choice | [Tutorial](#) | [Assignment](#) |
| **5** | Function Calling from LLMs | How models choose and call tools; parsing output | Call an API with 2 tools; inspect model’s tool_calls | OpenAI/Anthropic tool-calling format | [Tutorial](#) | [Assignment](#) |
| **6** | Building a Single-Tool Agent | One LLM + one tool; loop: decide → call tool or answer | Build “weather agent” or “calculator agent” end-to-end | When to use tool vs respond directly | [Tutorial](#) | [Assignment](#) |
| **7** | Multi-Tool Agent | Agent selects among several tools; handle wrong tool choice | Build agent with 3 tools (e.g., search, compute, lookup) | Tool selection and error handling | [Tutorial](#) | [Assignment](#) |
| **8** | Observation & Feedback | Pass tool result back to LLM; format for clarity | Log full turn: thought → tool call → observation → next thought | Structured observations help reasoning | [Tutorial](#) | [Assignment](#) |
| **9** | ReAct Pattern | Thought–Action–Observation; reasoning trace | Implement ReAct loop with 2 tools; inspect trace | Improves reliability and debuggability | [Tutorial](#) | [Assignment](#) |
| **10** | Plan-and-Execute | High-level plan first; then execute steps; replan on failure | Design “trip planner” agent: plan steps then execute | When to replan vs retry | [Tutorial](#) | [Assignment](#) |
| **11** | Short-Term Memory | Conversation history; context window; summarization | Implement context management: last N turns or summarization | Token limits; what to keep | [Tutorial](#) | [Assignment](#) |
| **12** | Long-Term Memory | Persistent store (vector DB, key-value); recall by relevance | Add “remember” and “recall” to agent using vector store | Episodic vs semantic memory | [Tutorial](#) | [Assignment](#) |
| **13** | Agent Evaluation Basics | Task success, steps to completion, cost, errors | Define success for one agent; run 10 test cases; log metrics | Benchmarks: SWE-bench, WebArena style | [Tutorial](#) | [Assignment](#) |
| **14** | Error Handling in Agents | Tool failure, timeouts, invalid input; retry and fallback | Add retries and user-friendly error messages to your agent | Graceful degradation | [Tutorial](#) | [Assignment](#) |
| **15** | Phase 2A Review | Consolidate agent loop, tools, memory, evaluation | Extend your agent with memory; run eval suite; document | Single-agent baseline for Phase 2B | [Tutorial](#) | [Assignment](#) |

---

## Phase 2B: Frameworks & Production Patterns (Days 16–28)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **16** | LangChain Agents | Agent, tools, AgentExecutor; run loop | Build same multi-tool agent using LangChain | LCEL, tool binding, parsing | [Tutorial](#) | [Assignment](#) |
| **17** | LlamaIndex Agents | Agent + tools + query engines | Build agent that uses LlamaIndex retrieval as a tool | ReAct and plan-and-execute in LlamaIndex | [Tutorial](#) | [Assignment](#) |
| **18** | Other Frameworks (CrewAI, AutoGen) | High-level concepts; when to use which | Read docs for 2 frameworks; compare to LangChain | Multi-agent vs single-agent focus | [Tutorial](#) | [Assignment](#) |
| **19** | Orchestration & Control Flow | Max steps, timeouts, “final answer” condition | Implement max-steps and explicit “I’m done” output | Avoid infinite loops; budget tokens | [Tutorial](#) | [Assignment](#) |
| **20** | Human-in-the-Loop | When to ask user; confirmation, clarification, approval | Add “confirm before send” or “choose option A/B” to agent | Sensitive actions; escalation | [Tutorial](#) | [Assignment](#) |
| **21** | Streaming Agent Output | Stream thoughts and tool calls to UI | Add streaming so user sees reasoning and progress | Chunked response; tool call events | [Tutorial](#) | [Assignment](#) |
| **22** | Observability & Logging | Log prompts, tool calls, latency, token usage | Add structured logs; build simple trace view | Trace tree: steps, tools, costs | [Tutorial](#) | [Assignment](#) |
| **23** | Security for Agents | Tool misuse, privilege escalation, prompt injection | List all tools; minimal permissions; validate inputs | Sandboxing; guardrails on tool use | [Tutorial](#) | [Assignment](#) |
| **24** | Cost & Latency | Tokens per run; caching; smaller models for routing | Measure cost per task; try caching repeated tool results | Model choice for planner vs executor | [Tutorial](#) | [Assignment](#) |
| **25** | Agentic RAG | Agent that decides when to search vs read docs vs answer | Combine RAG retrieval as tool(s) in your agent | Hybrid: agent + RAG pipeline | [Tutorial](#) | [Assignment](#) |
| **26** | Tool Design Best Practices | Naming, description, parameters, idempotency, errors | Redesign 3 tools: clear schema and error contract | Documentation and examples | [Tutorial](#) | [Assignment](#) |
| **27** | Testing Agents | Unit tests for tools; integration tests for full loop | Write 5 tests: 2 for tools, 3 for agent scenarios | Mock LLM for deterministic tests | [Tutorial](#) | [Assignment](#) |
| **28** | Deployment Options | Serverless, containers, queues; scaling | Document how you’d deploy your agent (e.g., FastAPI + queue) | Rate limits, timeouts, health checks | [Tutorial](#) | [Assignment](#) |

---

## Phase 2C: Multi-Agent Systems (Days 29–40)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **29** | Why Multi-Agent? | Specialization, parallel work, debate, division of labor | List 2 problems better solved by multiple agents | Research + writer; coder + reviewer | [Tutorial](#) | [Assignment](#) |
| **30** | Roles & Specialization | Define roles: researcher, writer, critic, executor | Write role prompts for 3 specialist agents | Clear input/output contracts | [Tutorial](#) | [Assignment](#) |
| **31** | Agent Communication | Message format; handoffs; shared state | Define message schema between 2 agents | Sequential vs parallel handoffs | [Tutorial](#) | [Assignment](#) |
| **32** | Two-Agent System | Agent A does task; passes result to Agent B | Build researcher → writer pipeline | When to hand off vs iterate | [Tutorial](#) | [Assignment](#) |
| **33** | Supervisor / Coordinator | One agent routes tasks to specialists | Build supervisor that delegates to 2–3 agents | Routing logic; when to aggregate | [Tutorial](#) | [Assignment](#) |
| **34** | Parallel Agents | Run independent agents in parallel; merge results | Implement “ask 3 agents, merge answers” | Use when tasks are independent | [Tutorial](#) | [Assignment](#) |
| **35** | Debate & Critique | One agent generates; another critiques; refine loop | Build writer + critic for 2 rounds | Improve quality through critique | [Tutorial](#) | [Assignment](#) |
| **36** | Shared Memory in Multi-Agent | Blackboard, shared state, conflict handling | Design shared state for 2 agents (e.g., shared doc) | Consistency and versioning | [Tutorial](#) | [Assignment](#) |
| **37** | Multi-Agent Evaluation | Task success, coordination cost, latency | Define metrics for your multi-agent system; run 10 cases | Compare to single-agent baseline | [Tutorial](#) | [Assignment](#) |
| **38** | Failure Handling in Multi-Agent | Agent failure, timeout, inconsistent output | Add timeouts and fallbacks for agent calls | Retry, substitute agent, or escalate | [Tutorial](#) | [Assignment](#) |
| **39** | Frameworks for Multi-Agent | CrewAI, AutoGen, LangGraph multi-agent | Build same 2-agent system in one framework | Compare code and control flow | [Tutorial](#) | [Assignment](#) |
| **40** | Phase 2C Review | Multi-agent design, roles, coordination, evaluation | Document your multi-agent architecture; run full eval | Prepare for capstone | [Tutorial](#) | [Assignment](#) |

---

## Phase 2D: Advanced Topics & Capstone (Days 41–45)

| Day | Topic | Learning Objectives | Key Activities | Resources / Notes | Tutorial | Assignment |
|-----|--------|----------------------|----------------|-------------------|----------|------------|
| **41** | Agent Planning (Advanced) | Hierarchical plans; replanning; partial execution | Implement “plan 5 steps, execute 2, replan if needed” | Tree-of-thought; backtracking | [Tutorial](#) | [Assignment](#) |
| **42** | Tool Learning & Creation | Agents that create or suggest new tools | Read about tool synthesis; list one use case | When tools are unknown in advance | [Tutorial](#) | [Assignment](#) |
| **43** | Ethics & Governance | Accountability, transparency, human oversight | Draft one-page “agent governance” policy | Auditable decisions; explainability | [Tutorial](#) | [Assignment](#) |
| **44** | Agentic AI Capstone Design | Full system: multi-agent or agentic RAG with production concerns | Write 2-page design: architecture, tools, safety, eval | Diagrams; success criteria; risks | [Tutorial](#) | [Assignment](#) |
| **45** | Agentic AI Capstone Build & Review | Implement and test; document learnings | Build capstone; run evaluation; write retrospective | Present plan vs actual; next steps | [Tutorial](#) | [Assignment](#) |

---

## Quick Reference: Gen AI vs Agentic AI

| | Generative AI (45 days) | Agentic AI (45 days) |
|---|-------------------------|------------------------|
| **Focus** | Models, prompting, RAG, fine-tuning, APIs | Agents, tools, memory, planning, multi-agent |
| **Outcome** | Build RAG apps, use/fine-tune LLMs responsibly | Build single- and multi-agent systems for real tasks |
| **Prerequisite** | None (start here) | Gen AI basics (especially prompting and APIs) helpful |

---

## Tips

1. **Order** — Do the Gen AI 45 days first, then Agentic AI, so you have a solid base.
2. **Hands-on** — Implement something every day, even if small.
3. **One codebase per track** — One Gen AI project (e.g., RAG app) and one agent project; extend them over the 45 days.
4. **Log metrics** — From early on, track tokens, latency, and success rate.
5. **Adjust pace** — Combine light days or split heavy ones (e.g., multi-agent week) as needed.

Good luck with your 90-day Gen AI and Agentic AI journey.
