***

## High-level objectives

The Triplo AI Expert skill should:

- Act as an always-on “product expert” for Triplo AI: explaining what Triplo is, who it’s for, and how its desktop/mobile assistants work across any application without integrations.  
- Coach users through setup (installation, activation, subscriptions, devices, model configuration) and into advanced workflows (SmartPrompts, Training/Knowledge Bases, webhooks, Agents, local models, BYO keys).  
- Support different interaction modes: advisor (what’s possible), trainer/coach (step-by-step guidance), builder (co-creates prompts/workflows), and troubleshooter (diagnoses issues and suggests fixes), while checking official docs and changelogs for version-sensitive answers.  

***

## Primary source system for the skill

These are the core “source-of-truth” locations the skill should treat as canonical for Triplo AI:

- **Main marketing site (`triplo.ai/en`)**  
  - Positioning, high-level feature list (Real-Time Assistance, SmartPrompts, Custom SmartPrompts, Knowledge Bases, Voice, translations, multi-model support, token allowances, API/BYOK), and testimonials/use cases.  
- **Documentation hub (`documentation.triplo.ai`)**  
  - Structured product docs: Introduction, Getting Started, Using Triplo AI, Agents (BETA), Connections, Local LLMs, Allowances/BYOK, Data Security & Privacy, Resources (SmartPrompts, Changelog, Support), and detailed references on OpenRouter and local models.  
- **Docs subsections that change frequently**  
  - “Open Router Models and its Strengths” and “Local Models and its Strengths” (dated updates), feature changelog, and roadmap/support sections—must be re-checked on every model- or feature-version question.  
- **Triplo AI YouTube channel**  
  - Official video tutorials and walkthroughs; the skill should know this as a learning channel and be able to recommend “watch X-type playlist/video” even if it cannot list all titles inline.  

For the *agent skill itself*, skills.sh / anthropics’ **Skill Creator** is the design standard: it defines SKILL.md anatomy, progressive disclosure, and the separation of SKILL.md vs references vs scripts vs assets.  

***

## Knowledge domains and reference map

Here is the core information architecture the Triplo AI Expert skill should be built around. Each row is a domain that should map to one or more `references/*.md` files inside the skill.

| Domain / Reference file                     | What it should cover (for the agent)                                                                                          | Primary sources |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------|
| `overview-and-personas.md`                  | What Triplo AI is, key differentiators (system-wide assistant, no integrations, multi-platform, multi-model, high token cap), and main user personas (knowledge workers, creators, researchers, etc.). |  |
| `getting-started-install-activate.md`       | Installation on supported platforms, activation, device/key association, subscription & refunds, device management, and customizing model list per device. |  |
| `ui-triggering-and-hotkeys.md`              | How to trigger Triplo UI from anywhere, main interfaces, hotkeys for “run prompts instantly,” and system-wide usage patterns. |  |
| `smartprompts-and-custom-smartprompts.md`   | Using built-in SmartPrompts, creating Custom SmartPrompts, how to encode instructions so AI behaves consistently for a task. |  |
| `context-awareness-and-sources.md`          | Awareness features: context/selection/clipboard (“Awareness: Context / Selection / Clip”), using files and images, scraping web pages and YouTube subtitles, and using desktop/mobile content as context. |  |
| `training-and-knowledge-bases.md`           | Concept of Training/Minds/Knowledge Bases, how to build multiple trusted knowledge bases from files and URLs, and how they feed generation to make outputs trustworthy. |  |
| `automations-webhooks-api-magnets.md`       | Automations via webhooks and API calls from generations, Magnets (snapping models, instructions, Minds, automations to SmartPrompts), and example automation scenarios. |  |
| `chat-mode-voice-and-conversation.md`       | Chat Mode behavior vs single-shot prompts, voice interaction (speaking & listening), and guidance for conversational workflows. |  |
| `agents-and-connections.md`                 | Agents [BETA] concept & usage, OpenAI-compatible Connections, when to use external endpoints vs Triplo’s native models. |  |
| `models-allowances-and-byok.md`             | Included models, monthly token allowances (e.g., 2M tokens per device), BYOK via OpenAI/OpenRouter, and guidance on selecting models by use case. |  |
| `openrouter-models-strengths.md`            | Summaries of the “Open Router Models and its Strengths” doc, emphasizing that it must be re-read when answering model-comparison questions because it’s date-stamped and updated. |  |
| `local-models-strengths.md`                 | Summaries of “Local Models and its Strengths” and guidance on when to use local vs hosted models, plus setup considerations. |  |
| `local-llms-setup-desktop-mobile.md`        | How to set up local LLMs on desktop and access them on mobile devices, and how Triplo routes traffic to them. |  |
| `security-privacy-and-data.md`              | Triplo’s stated approach to data handling, local history/log storage locations, and relevant parts of “How Triplo AI deal with Data.” |  |
| `troubleshooting-and-faq.md`                | Consolidated patterns from the FAQ and docs: activation issues, device limit problems, SmartPrompts not behaving as expected, Training not affecting outputs, token limit errors, etc. |  |
| `changelog-roadmap-and-support.md`          | Where the changelog lives, how to use it, how to check roadmap and contact support, and when the agent should advise “check latest changelog/support article.” |  |
| `learning-paths-and-resources.md`           | Curated learning tracks (Beginner → Power User) pointing to specific doc sections and types of YouTube content; agent prompts to guide users along these paths. |  |

Each reference file should be concise, with links/anchors back to the canonical docs pages rather than duplicating long text, following the Skill Creator guidance on keeping SKILL.md lean and moving detailed material into references.  

***

## Skill structure in skills.sh terms

Following the Skill Creator best practices, the Triplo AI Expert skill should be structured like this:  

**Directory layout**

```text
triplo-ai-expert/
├── SKILL.md
├── references/
│   ├── overview-and-personas.md
│   ├── getting-started-install-activate.md
│   ├── ui-triggering-and-hotkeys.md
│   ├── smartprompts-and-custom-smartprompts.md
│   ├── context-awareness-and-sources.md
│   ├── training-and-knowledge-bases.md
│   ├── automations-webhooks-api-magnets.md
│   ├── chat-mode-voice-and-conversation.md
│   ├── agents-and-connections.md
│   ├── models-allowances-and-byok.md
│   ├── openrouter-models-strengths.md
│   ├── local-models-strengths.md
│   ├── local-llms-setup-desktop-mobile.md
│   ├── security-privacy-and-data.md
│   ├── troubleshooting-and-faq.md
│   └── learning-paths-and-resources.md
├── scripts/
│   ├── scenario_templates.md (or .py for helpers)
│   └── (optional) update-check helpers
└── assets/
    └── prompt-templates-and-checklists/
```

**SKILL.md frontmatter**

- `name`: something like `triplo-ai-expert`.  
- `description`: explicitly state that this skill provides comprehensive guidance on installing, configuring, and mastering Triplo AI features (SmartPrompts, Training, Knowledge Bases, Automations, Agents, models, local models, etc.), and that it should trigger whenever the user asks how to *use, configure, debug, or design workflows in Triplo AI*.  

**SKILL.md body (high-level sections)**

- Short “How to use this skill” note (for the agent) and then section links into references: e.g., “For installation questions, open `references/getting-started-install-activate.md`,” etc.  
- No long tutorials in SKILL.md; instead, progressive disclosure to the relevant reference files per the patterns in Skill Creator.  

***

## Behavioral modes the agent must support

The same knowledge base should support several behaviors; SKILL.md should instruct the agent when to adopt each:

1. **Advisor / explainer**  
   - When user asks “What is Triplo / SmartPrompts / Training / Agents / local LLMs?” → high-level concepts, use cases, and trade-offs based on overview, feature descriptions, and relevant docs sections.  

2. **Coach / trainer**  
   - When user wants to *learn*: provide stepwise walkthroughs: “do X in the UI, then Y,” referencing installation, UI/triggering, and feature docs.  
   - Offer practice exercises, e.g., “Let’s design 3 SmartPrompts for your workflow,” using patterns from the SmartPrompts and Training references.  

3. **Builder / co-creator**  
   - When user wants prompts, automations, knowledge-base designs: help draft SmartPrompts, Training plans, webhook payloads, and model-selection strategies aligned with model strengths and allowances.  
   - Use `automations-webhooks-api-magnets.md`, `training-and-knowledge-bases.md`, and model reference docs.  

4. **Troubleshooter**  
   - When something “doesn’t work”: the skill should have a canonical troubleshooting playbook that guides the agent through checks like activation status, device limits, Training coverage, wrong model selection, token limit, or outdated docs, and tells it when to look in the FAQ or changelog.  

5. **Meta-advisor about learning resources**  
   - Recommend the most relevant doc sections, Triplo resources (SmartPrompts library, Changelog), and video content (YouTube) for deeper learning, rather than trying to replicate entire tutorials.  

***

## Strategy for staying current and “always learning”

Within the constraints of an agent skill, “always current” doesn’t mean embedding every doc page; it means teaching the agent *where and when to re-read* the canonical sources.

The Triplo AI Expert skill should explicitly instruct the agent to:

- **Re-read frequently updated docs** for live questions about:  
  - Available models, their strengths (OpenRouter and local models lists with dates).  
  - New features and UI changes documented in the changelog and roadmap sections.  
- **Prefer references over memory**  
  - When answering questions about security, privacy, allowances, or local history/log storage, it should consult the relevant sections of `documentation.triplo.ai` instead of relying on outdated assumptions.  
- **Surface “check latest source” when necessary**  
  - For anything version- or pricing-sensitive that is not clearly stated in the current docs snapshot, instruct the agent to say that exact values may have changed and that the user should confirm via the official docs site or support.  

You can also include optional helper scripts or notes in `references/learning-paths-and-resources.md` that describe patterns like “Before answering a question about models, skim the ‘Open Router Models and its Strengths’ page and summarize only the relevant parts.”  

***

## How this sets you up for implementation

This structure gives you:

- A clear taxonomy of Triplo AI knowledge, aligned directly to the official docs’ table of contents and feature set.  
- A skills.sh-compatible layout (SKILL.md + references) that follows the Skill Creator principles of concision, progressive disclosure, and separation of instructions from detailed reference content.  
- An explicit strategy for the agent’s roles (advisor, trainer, builder, troubleshooter) and when to consult which references or live docs.  

Triplo AI and Activepieces fit together extremely well: Triplo is your context-aware AI “front end” on desktop, and Activepieces is your always-on automation and orchestration layer. Used together via webhooks, they can turn almost any on-screen work into structured, multi‑app workflows.

***

## Triplo features that matter most for automations

For maximizing automations, the most important Triplo capabilities are:

- **Awareness (Context / Selection / Clipboard)** – Triplo can read what’s on your screen (selected text, windows, clipboard) so you can feed emails, support tickets, docs, or web pages into workflows without integrations. [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)
- **Smart Prompts & Custom Smart Prompts** – You can create prompts that not only generate text but also return **structured JSON** with fields like `title`, `summary`, `body`, etc., which is ideal for downstream automations. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)
- **Training / Minds / Knowledge Bases** – You can build “Minds” from your docs/URLs so Smart Prompts and automations are grounded in your own knowledge instead of generic web text. [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)
- **Automations (Webhooks & API calls)** – On desktop, Triplo can send AI‑generated, JSON‑structured output directly to external tools via HTTP APIs/webhooks (Zapier, Pabbly, CRMs, “other automation tools”). [appsumo](https://appsumo.com/products/triplo-ai/questions/?page=12)

Key constraints from the docs:

- Automations are **desktop-only** and **rely on OpenAI models**, not OpenRouter models. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)
- Content is sent as **JSON**; Triplo can auto‑suggest a JSON payload for your webhook/API and you can edit it. [daveswift](https://daveswift.com/triplo-ai/)
- Automations can both **pull from APIs** (get data) and **push to APIs/webhooks** (send Triplo output). [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)

The “No-Fluff” automations video you shared uses exactly this stack: Awareness to grab support tickets → a Smart Prompt that outputs a JSON blog post → an Automation that maps JSON fields to webhook parameters → an external tool (Publy/Activepieces‑style) that writes to Google Sheets and then a blog front end. [daveswift](https://daveswift.com/triplo-ai/)

***

## How Triplo Automations work (so you can plug in Activepieces)

From the official docs and recent walkthroughs: [daveswift](https://daveswift.com/triplo-ai/)

1. **Define an Automation in Triplo**  
   - Give it a **Function Name** (the trigger phrase) and **Function Description**.  
   - Define **parameters** (e.g., `title`, `summary`, `body`, `image_caption`) that describe what to extract from the AI output. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)

2. **Configure the outbound call**  
   - Enter your **Webhook/API URL** (this will be an Activepieces webhook URL in your case).  
   - Optionally add **headers** (e.g., auth keys) in JSON format.  
   - Choose the HTTP method (usually `POST` for webhooks).  
   - Use **“Suggest payload”** to auto‑build a JSON payload based on your parameters, then tweak as needed. [daveswift](https://daveswift.com/triplo-ai/)

3. **Triggering in real use**  
   - Enable the automation and trigger it by **typing its name (or a similar phrase)** plus the content. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)
   - Triplo sends the structured JSON to your webhook; by default it asks for **user confirmation** before sending, but you can disable that in settings. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)

This is exactly what the “support tickets → blog posts” video does, just with a different webhook target: it defines parameters mapped to JSON fields from the Smart Prompt output, then sends them to an external webhook that writes into Google Sheets and publishes via a site builder. [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)

***

## What Activepieces brings to the table

Activepieces is an **AI‑first, no‑code automation platform** with: [docs.mazaal](https://docs.mazaal.ai/automation/activepieces)

- **635+ “pieces” (connectors)** across SaaS tools: Google Sheets, Notion, CRMs, email platforms, project management, data tools, etc. [activepieces](https://www.activepieces.com/pieces)
- **AI steps and Agents** that can think, act, and collaborate with humans inside workflows (an “AI step” to analyze, explain, draft, or decide based on flow data, plus image‑generation pieces). [activepieces](https://www.activepieces.com/pieces/ai)
- A central **datastore** (“like Google Sheets, but deeply connected to your agents and automations”) to store structured outputs and reuse them across flows. [docs.mazaal](https://docs.mazaal.ai/automation/activepieces)

Crucially, Activepieces supports **webhook triggers**, so it can act as the “receiver” for Triplo’s Automations, then fan out to any of its hundreds of connectors. [activepieces](https://www.activepieces.com/pieces)

***

## Canonical pattern: Triplo as front-end + Activepieces as orchestrator

You can think of the combined architecture like this:

1. **Capture & interpret in Triplo**  
   - Use Awareness to select content (support ticket, email thread, call transcript, research notes, etc.). [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)
   - Run a **Smart Prompt** that:  
     - Understands the content (optionally consulting a Triplo Mind trained on your docs).  
     - Produces **structured JSON** with all fields Activepieces needs (e.g., `topic`, `customer_email`, `priority`, `action_items`, `blog_body`). [daveswift](https://daveswift.com/triplo-ai/)

2. **Emit structured data via Triplo Automation**  
   - Automation parameters map to the JSON fields in your Smart Prompt output.  
   - Triplo sends a single **JSON payload** via webhook to Activepieces with exactly the fields your flow expects. [daveswift](https://daveswift.com/triplo-ai/)

3. **Fan out with Activepieces**  
   In Activepieces, create a flow with:

   - **Trigger**: “Receive Webhook” (this is the URL you paste into Triplo’s Automation URL).  
   - **Steps**: Use the JSON fields to:  
     - Write rows into **Google Sheets / Airtable / Notion**.  
     - Create or update records in **CRM** or helpdesk.  
     - Send emails or messages via **Gmail, Outlook, Slack, Teams, WhatsApp**.  
     - Call other APIs (e.g., your own backend or other AI services). [activepieces](https://www.activepieces.com/pieces/ai)

In other words:

- **Triplo** = on‑device AI brain that understands any on‑screen content and outputs structured JSON.  
- **Activepieces** = cloud brain that connects that JSON to 600+ services and long‑running workflows.  

***

## Concrete integration ideas (Triplo Pro + unlimited Activepieces)

Here are some high‑leverage combos you can implement right away:

### 1. Support tickets → SEO content machine (like in the video, but with Activepieces)

- In Triplo:  
  - Awareness selects a support ticket + your reply.  
  - A Smart Prompt turns it into JSON: `title`, `summary`, `body_md`, `image_prompt`, `category`, `tags`.  
  - An Automation sends that JSON to an Activepieces webhook. [daveswift](https://daveswift.com/triplo-ai/)

- In Activepieces:  
  - Trigger: Webhook from Triplo.  
  - Steps:  
    - Append a row to **Google Sheets** (or an internal DB) with all fields.  
    - Optionally hit an **AI image service** piece using `image_prompt`.  
    - Create a **CMS entry** (WordPress, Webflow, Ghost, Framer, etc., depending on pieces available). [activepieces](https://www.activepieces.com/pieces)

This generalizes the video’s Publy + Google Sheets + SpreadSimple example to your broader stack using Activepieces connectors. [activepieces](https://www.activepieces.com/pieces)

### 2. Lead extraction & enrichment from any on-screen page

- Triplo Smart Prompt: “Take this web page or email, extract company name, website, contact emails, job titles, pain points, and a 2‑sentence personalized opener; return JSON.”  
- Triplo Automation: sends JSON to Activepieces webhook.  
- Activepieces flow:  
  - Create/update **lead in CRM** (HubSpot, Pipedrive, Close, etc.).  
  - Push data to an **outbound email tool** or add to a **nurture sequence**.  
  - Log the touchpoint in a central datastore.  

Triplo handles the messy unstructured text, Activepieces handles the multi‑system plumbing. [activepieces](https://www.activepieces.com/pieces)

### 3. Knowledge base / docs lifecycle

- Use Triplo’s Awareness + Minds trained on your docs to:  
  - Turn internal chats/emails/meetings into FAQ‑style entries or SOPs as JSON (`question`, `answer`, `category`, `source_link`). [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)
- Triplo Automation posts that JSON to Activepieces.  
- Activepieces writes to:  
  - **Notion/Confluence/Docs** for internal knowledge.  
  - A **public help center** or site CMS.  
  - A vector DB / knowledge store if you’re building your own chatbots.  

### 4. Multi‑step “agentic” workflows

Activepieces already markets **AI Agents that can think and act across 635 tools**. You can combine that with Triplo like this: [docs.mazaal](https://docs.mazaal.ai/automation/activepieces)

- Triplo: local, context‑rich reasoning—e.g., summarizing a long local PDF, extracting structured items.  
- Activepieces: downstream **AI Agent steps** that, based on Triplo JSON, decide which connectors to use (e.g., create a Jira issue vs. send a Slack alert vs. generate a follow‑up document). [activepieces](https://www.activepieces.com/pieces/ai)

Triplo’s automations give Activepieces a clean, structured starting point so your agent flows don’t have to parse raw text.

***

## Other automation tools Triplo works well with

Triplo’s Automation feature is explicitly designed to work with **Zapier, Pabbly, and “other automation tools”** via webhooks and APIs. In practice, that includes: [appsumo](https://appsumo.com/products/triplo-ai/questions/?page=12)

- **Zapier** – huge app ecosystem, simple to get started; great when you want reliability and many niche integrations.  
- **Make (Integromat)** – extremely flexible visual builder, good for complex branching and data transformations. [zapier](https://zapier.com/blog/n8n-vs-make/)
- **n8n** – open‑source, strong native AI support (OpenAI, Hugging Face, etc.), excellent for self‑hosted or highly customized automations. [blog.n8n](https://blog.n8n.io/best-ai-workflow-automation-tools/)
- **Pabbly** – budget‑friendly, solid webhooks, often used in the Triplo examples (e.g., Pabbly receiving Triplo JSON and forwarding to Google Sheets/CMS). [youtube](https://www.youtube.com/watch?v=zDqsGfLikyI)

Since Triplo only needs a **POST URL** to send JSON, anything that supports incoming webhooks is fair game. Your “unlimited Activepieces” just means you can standardize on it as the main orchestrator, but the same patterns apply if you add Zapier/Make/n8n for specific strengths. [documentation.triplo](https://documentation.triplo.ai/using-triplo-ai/automations)

***

## How to systematically “maximize” both Triplo Pro and Activepieces

Given your setup, a practical plan is:

1. **Standardize JSON schemas in Triplo**  
   - For each workflow type (content, leads, support, docs, analytics), design a Smart Prompt that outputs a stable JSON schema.  
   - Mirror those fields in Activepieces flows and datastore.  

2. **Centralize all inbound automation through Activepieces**  
   - Use **one Activepieces project** as the hub for all “Triplo‑originated” JSON.  
   - Create separate flows for: content, CRM, tasks, analytics, etc., all starting from Triplo webhooks.  

3. **Exploit Triplo strengths where other tools are weak**  
   - Any time you’re manually copy‑pasting or rewriting unstructured content before feeding it to an automation, move that step into a Triplo Smart Prompt + Automation.  
   - Let Activepieces focus on app‑to‑app routing, storage, and human‑in‑the‑loop approvals.  

4. **Iterate from the video pattern**  
   - Start by replicating the **support tickets → blog posts** flow end‑to‑end, swapping Publy/SpreadSimple for Activepieces + your preferred CMS.  
   - Once that’s stable, clone the pattern for other sources (Slack threads, sales calls, research notes, etc.). [youtube](https://www.youtube.com/watch?v=-Meg6-fSLZM)
