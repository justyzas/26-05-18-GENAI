# Generative AI for beginners

This course is a practical, hands-on introduction to generative AI for beginners. You learn by doing with small, guided exercises and quick wins. No prior coding is required — everything is explained in plain language and built step by step.

Across the program, you start with ChatGPT basics and the core ideas behind LLMs (what they are, how costs work, and safe usage). Then you explore popular tools for research and documents, try multimodal features (images, audio, video), and build simple, useful things — like a one-page site, a tiny app, and a basic AI agent. Coding is optional; when we do code, we use AI helpers to keep it simple or no-code automation platform.

By the end, you will have:

- A personal prompt library and reusable ChatGPT workflows
- A simple research notebook with citations you can check
- Basic image/audio/video outputs created with AI
- A minimal one-page website
- A tiny app (to-do or counter) built with AI assistance
- A basic Q&A assistant over your own docs (RAG)
- A simple automation/agent in n8n (e.g., research-to-email)

Course goals:

1. Demystify generative AI and build confidence through quick wins
2. Teach core skills: clear prompting, picking models at a glance, verifying outputs, and small automations you can actually use

### **Day 1: Introduction to Generative AI and Mastering ChatGPT Use Cases**

- Course overview, objectives, and learning path
- ChatGPT usage and practical applications
- What is a Large Language Model (LLM)
- Understanding AI platforms and ecosystems
- Gen-AI as a transformative technology
- Core concepts of LLMs and their capabilities
- Information seeking
- Web search
- Email generation
- Post generation
- Prompt engineering
- Travel planning
- Basic document analysis
- Document generation
- and others
- **Lab:** Hands-on ChatGPT exploration and prompt experimentation; Prompt engineering workshop with real-world scenarios

### **Day 2: Understanding LLM Models and Economics**

- ChatGPT model variations: GPT-5, GPT-4.1, GPT-5-mini
- Token-based pricing: input vs output costs
- Understanding tools in LLMs and their functions
- Web search tool integration and capabilities
- Memory tools and conversation persistence
- **Lab:** Cost calculation exercises and model comparison

### **Day 3: LLM Capabilities and Limitations**

- ChatGPT Code Interpreter tools and data analysis
- Understanding the core weaknesses of LLMs
- LLMs as probability machines: how they actually work
- Hallucinations: identification and mitigation strategies
- Knowledge limitations and training data cutoffs
- Context size constraints and memory limitations
- **Lab:** Identifying hallucinations and testing model limits

---

## **Week 2: Exploring AI Platform Alternatives**

### **Day 1: Gemini, Reasoning Models, and Comprehensive LLM Platform Tour**

- Gemini platform overview and capabilities
- Introduction to reasoning models and their applications
- Gemini features and tooling
- Gemini model family and their strengths
- Hands-on exploration with Gemini
- Anthropic and the Claude LLM family
- Claude's unique capabilities and conversation style
- Censorship and guard-rails of generative AI
- X.ai's Grok platform and real-time capabilities
- Venice.ai for uncensored models
- **Lab:** Create and test prompts using Gemini; Comparative analysis using different platforms

### **Day 2: Document Analysis with NotebookLM**

- Import PDFs, Google Docs/Slides, and links as sources
- Ask source-grounded questions with inline citations you can verify
- Extract tables, entities, timelines, and compare documents side-by-side
- Auto-generate summaries, note cards, and audio overviews
- Export notes to Google Docs or copy structured outputs
- **Lab:** Upload 3 sample docs and build a mini research notebook: create a comparison table, list key insights with citations, and draft a one-paragraph summary

### **Day 3: Perplexity for Faster Research**

- Introduction to Perplexity AI and its Deep Research mode
- Ask questions and get answers with sources and citations
- When to use quick answers vs Deep Research (3-minute comprehensive reports)
- How to read, verify, and trust citations
- Export and share your findings (PDF, documents, Perplexity Pages)
- Comparing Perplexity vs NotebookLM vs ChatGPT for research
- **Lab:** Run the same brief in Perplexity, NotebookLM, and ChatGPT; compare results

---

## **Week 3: ChatGPT Advanced Features**

### **Day 1: ChatGPT Canvas for Document Creation**

- Introduction to ChatGPT Canvas interface
- Using Canvas for long-form writing and editing
- Collaborative document creation with AI
- Iterative refinement and version control
- **Lab:** Create a business proposal using Canvas

### **Day 2: ChatGPT Projects for Organization**

- Understanding ChatGPT Projects feature
- Organizing conversations by topic or client
- Custom instructions per project
- File uploads and context management
- **Lab:** Set up projects for different business needs

### **Day 3: ChatGPT Voice Mode, Accessibility, and Search Integration**

- Advanced voice mode capabilities
- Hands-free AI interaction for productivity
- Voice-to-text workflows
- Accessibility features for diverse users
- Understanding ChatGPT Search capabilities
- Real-time information retrieval
- Comparing search results with traditional search engines
- Best practices for search-enabled prompts
- **Lab:** Use voice mode for meeting preparation; Conduct research using ChatGPT Search

---

## **Week 4: Multimodal AI**

### **Day 1: ChatGPT Vision**

- OCR, UI, and chart understanding
- Prompt for structure (lists/JSON)
- Limits: counting, tiny/rotated text
- Cost basics: images as tokens
- **Lab:** Analyze 3 images and refine prompts

### **Day 2: Image Generation and Editing with ChatGPT & Qwen**

- gpt-image-1: generate, edit, variations
- Qwen2-VL: OCR/editing, open/local
- When to pick which for tasks
- Prompt patterns: subject, style, negatives
- **Lab:** Make/edit 3 marketing assets in both

### **Day 3: ElevenLabs Text-to-Speech and Sora 2 Video**

- TTS, STT, dubbing, cloning
- Models: v3, Flash, Turbo, Multilingual
- Controls: stability, style, latency
- Responsible voice use and deployment
- Prompting: subject, motion, camera
- Features: consistency, remix, auto audio
- Limits: physics realism, policies
- Compare with Veo/Kling/Ray
- **Lab:** Bilingual demo audio + captions; Generate a 30s concept and iterate

## **Week 5: Generative AI as Technology**

### **Day 1: Ollama (Local Open-Source Models)**

- Install and run (`ollama run gemma3`)
- Catalog: Qwen, Gemma, Llama, DeepSeek
- Modelfile tweaks, HTTP API (Python/JS)
- Offline privacy and performance tips
- **Lab:** Benchmark two local models via API

### **Day 2: OpenAI, Google AI Studio, and OpenRouter**

- OpenAI Responses API + tools
- Gemini 2.5 tiers and Live API
- Compare pricing/context/safety
- Cross-platform workflow patterns
- Unified API, routing, fallbacks, ZDR
- Headers for attribution/provider prefs
- Streaming, structured outputs, caching
- When to use vs native APIs
- **Lab:** Same assistant on both; compare; Compare two models for one task

### **Day 3: Lovable.dev Website**

- Chat-driven builder and templates
- Prompted layout/content iterations
- When to use vs custom code/CMS
- Publish previews and collect feedback
- **Lab:** Ship a one-page site

## **Week 6: Advanced Generative AI**

### **Day 1: LLM Leaderboards (Picking Models)**

- Metrics: MMLU, MT-Bench, Arena Elo
- Caveats: leakage, overfit, reproducibility
- Map scores to domain/context needs
- Shortlist by cost/speed/privacy
- **Lab:** Weighted scorecard for 3 models

### **Day 2: Staying Current with AI News**

- Sources: The Batch, news.smol.ai, official model blogs
- Cadence: weekly scan, verify claims, track changelogs
- Tools: RSS/alerts, Perplexity/NotebookLM summaries
- Categorize updates: safety, capability, tooling, policy
- **Lab:** Build a personal feed and draft a weekly brief

### **Day 3: GitHub Copilot (Vibe Coding) and Build with OpenAI Codex Cloud**

- Inline completions, chat, agent mode in VS Code
- Set up extension; pick models and custom instructions
- Add MCP tools for project-specific tasks
- Write tests first, let Copilot implement, then review
- Read/modify/run code in cloud environments
- GitHub integration; ask vs code modes and PR diffs
- Background tasks and multi-step assignments
- Security: MFA/SSO, audit trails for code changes
- **Lab:** Implement a small feature + tests with Copilot; Delegate a feature to Codex and review the PR

## **Week 7: n8n AI Automation and AI Agents**

### **Day 1: Introduction to No-Code Automation and AI Agents**

- What is no-code automation and why it matters for business
- Introduction to n8n platform and capabilities
- n8n vs Make.com: features, pricing, and use cases
- Understanding execution-based vs task-based pricing
- Exploring n8n templates library (600+ community templates)
- What constitutes a "tool" in Generative AI
- Difference between AI tools and AI agents
- Why 2025 is the year of AI agents
- AI agent architecture and autonomy
- Business applications of AI agents
- **Lab:** Explore n8n interface and browse templates; Design conceptual AI agent workflows

### **Day 2: Building Your First Agents**

- Setting up n8n (cloud or self-hosted)
- Understanding workflows, nodes, and triggers
- Build a Google Calendar agent for scheduling
- Build a Gmail agent for email automation
- Connecting agents to AI models
- **Lab:** Build and test calendar and Gmail agents

### **Day 3: Multi-Agent Systems**

- Building a research agent (web search + email combined)
- Coordinating multiple agents in workflows
- Human-in-the-loop approval steps
- Error handling and monitoring
- **Lab:** Create a comprehensive research-to-email agent

## **Week 8: n8n AI Automation in Action**

### **Day 1: Intro to RAG**

- Retrieve-then-generate basics (chunks, embeddings, vector store)
- Retrieval strategies: top-k, filters, reranking
- When to use RAG vs fine-tuning
- Grounding answers and citing sources
- **Lab:** Build a simple RAG flow and query your docs

### **Day 2: Domain Expert AI Agent**

- Define scope, tools/connectors, and guardrails
- Use retrieval/memory for domain grounding
- Error handling and human-in-the-loop
- Evaluate answers for accuracy and coverage
- **Lab:** Implement an expert agent over your docs + web search

### **Day 3: n8n Project – Build and Test & Ship**

- Choose use case and success metrics
- Design workflow: triggers, nodes, approvals
- Add logging, retries, and error paths
- Connect to LLM(s) and external APIs
- Test cases, rate limits, and costs
- Monitoring, alerts, and audit trail
- Secure secrets and permissions
- Demo and docs for handover
- **Lab:** Build the initial workflow and dry-run with test data; Run end-to-end, fix issues, and present results
