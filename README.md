# m_power_n8n
an n8n-like platform specifically for M-Power Information

## 🐍 Python Environment Setup (For Codespaces & Local)

### A. If you have Python 3.10+ (recommended):

```bash
# 1. Create a virtual environment (recommended folder: .venv)
python3 -m venv .venv

# 2. Activate the virtual environment
source .venv/bin/activate

# 3. Install dependencies (if you have a requirements.txt)
pip install -r requirements.txt
```
---

### Saving your project dependencies to `requirements.txt`

After you install any packages with pip, **run this command to update your requirements file:**

```bash
pip freeze > requirements.txt
```
## 🔑 Setting API Keys

Before running any code, set your required API keys as environment variables in your terminal **(never commit your actual keys to this repo):**

```bash
# Set your Composio API key (replace with your actual key)
export COMPOSIO_API_KEY=your_composio_key_here

# Set your OpenAI API key (replace with your actual key)
export OPENAI_API_KEY=your_openai_key_here
```

## 1. Tech Stack Package Evaluation Table
| Package     | Description                                                         | Key Features / What It Can Do                                      | Pros                                          | Cons                                            | Component Fit                    |
| ----------- | ------------------------------------------------------------------- | ------------------------------------------------------------------ | --------------------------------------------- | ----------------------------------------------- | -------------------------------- |
| Composio    | Workflow automation/orchestration platform (Python/TS).             | Build, connect, and run multi-step workflows (like n8n/Node-RED).  | Open-source, modular, workflow builder, API.  | Newer project, docs still maturing.             | Core orchestration for app block |
| browser-use | Headless browser automation and web scraping toolkit for Python.    | Scrape structured/unstructured web data using browser simulation.  | Flexible, supports SPA/web apps, open source. | Requires headless browser, some learning curve. | Data collection/scraping         |
| PraisonAI   | Python-based agent framework for chaining LLMs and AI-driven logic. | Create agent chains, prompt templates, flexible output formatting. | Scriptable, multi-format, works with any LLM. | UI not included, smaller community.             | AI Agent logic/chaining          |
| Ollama      | Local LLM hosting for open-source models.                           | Run LLMs locally, fast inference, no API cost.                     | Free, fast, private.                          | Needs hardware, some models less capable.       | LLM backend for PraisonAI        |
| OpenRouter  | API aggregator for open-source & commercial LLMs.                   | Access multiple models, flexible API, easy key setup.              | Flexible, multi-model, fallback easy.         | Free tier limits, external dependency.          | LLM backend for PraisonAI        |
| Groq        | Fast API for Llama/Mixtral models.                                  | Super-fast inference, free/paid, easy setup.                       | Fastest inference.                            | Free tier limited, API key needed.              | LLM backend for PraisonAI        |

## 2. Project Components & Milestones
| Component                   | Milestone / Subtasks                                                                     | Deliverables / Outputs                                                  |
| --------------------------- | ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Backend – Application Block | Set up Composio, integrate browser-use, add API/manual input, routing, preprocessing     | Working Composio pipeline, scraping node, API/manual input support      |
| Backend – AI Agent Block    | Integrate PraisonAI, prompt config UI/back, LLM setup, agent chaining, output formatting | AI agent that takes input and prompt, returns output in JSON/text/table |
| Integration                 | Connect Application to AI Agent, schema validation, error middleware, test data flows    | Working end-to-end workflow, data passed from app to agent and back     |
| Frontend – UI               | Input forms, workflow trigger button, output display, builder UI, status/errors          | User-facing web UI (React/Vue), workflow trigger/monitor                |
| Evaluation & Testing        | Unit/integration tests, end-to-end tests, user feedback, deployment scripts              | Test coverage, bug/UX feedback log, deployment-ready demo               |

## 3. Week-by-Week, Goal-Driven Milestone Guide
| Week (2025)      | Focus Area               | Key Tasks / Goals                                                                   | Outputs / Milestones                                |
| ---------------- | ------------------------ | ----------------------------------------------------------------------------------- | --------------------------------------------------- |
| 1 (Jun 9–12)     | Project Setup & Planning | Repo/env, Docker, run core package samples, define MVP w/ supervisor                | Skeleton repo, "Hello World", initial workflow list |
| 2 (Jun 16–19)    | App Backend MVP          | Composio pipeline, connect browser-use, API/manual nodes, cleaning node             | Data collection workflow, test harness              |
| 3 (Jun 23–26)    | AI Agent Backend MVP     | Integrate PraisonAI, prompt/output format, LLM config, chaining experiments         | Working agent block, model configs                  |
| 4 (Jun 30–Jul 3) | Integration              | Connect App→Agent, schema validation, error handling/logging, end-to-end test       | Full pipeline, CLI/API test                         |
| 5 (Jul 7–10)     | UI Foundations           | Simple UI for input/prompt/output, backend trigger, display results                 | Web UI triggers workflow, output display            |
| 6 (Jul 14–17)    | UI/Workflow Enhancements | Basic builder UI, status/error states, multi-agent demo (e.g., investment use case) | Workflow composition UI, real-world demo            |
| 7 (Jul 21–24)    | Testing & Feedback       | Backend/frontend tests, user testing, bugfixes & UX polish                          | Passing tests, feedback log, bugfixes               |
| 8 (Jul 28–Aug 7) | Polish, Docs & Handover  | Docs, final UI/UX polish, demo recording, supervisor handover                       | Docs, demo video, handover doc                      |
