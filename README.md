# Introduction to Agentic AI: Building Conversational Agents with Persistent Memory

> Hands-on materials for the 2-hour tutorial at **Deep Learning Indaba 2026**, under the
> theme *"Sovereign Intelligence: Africa's Path in a Frontier AI World."*

This is a **self-contained** teaching project. You will build a conversational agent from
scratch in Python, give it short-term memory, and then add **persistent long-term memory
using vector embeddings**: the core engine behind real memory-backed agents.

To keep it fun and to make the lesson stick, our agent is a **griot**: a traditional oral
storyteller, who co-weaves an original, evolving folktale with the room. Storytelling is
the perfect vehicle here because **memory is the whole point**: a good tale has to remember
its own characters and events across turns and across sessions.

Everything runs on **small open models, locally, with no API key**. Nothing to sign up for,
nothing leaving your machine. That is also the point: agents you can host yourself are the
foundation of locally-owned, sovereign AI.

No prior experience with agents or NLP is assumed. Basic Python is enough.

---

## What you'll build

| Notebook | You will... | Open in Colab |
|----------|-------------|---------------|
| [`00_minimal_agent.ipynb`](notebooks/00_minimal_agent.ipynb) | Build a minimal agent loop: model, instructions, and a tool | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dagbolade/indaba-agentic-ai/blob/main/notebooks/00_minimal_agent.ipynb) |
| [`01_short_term_memory.ipynb`](notebooks/01_short_term_memory.ipynb) | Manage the story history; watch the context window overflow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dagbolade/indaba-agentic-ai/blob/main/notebooks/01_short_term_memory.ipynb) |
| [`02_vector_memory.ipynb`](notebooks/02_vector_memory.ipynb) | Add persistent memory with embeddings and a tiny vector store (plus an optional chat UI) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dagbolade/indaba-agentic-ai/blob/main/notebooks/02_vector_memory.ipynb) |
| [`03_from_prototype_to_production.md`](notebooks/03_from_prototype_to_production.md) | See how these patterns scale to a real production system | (n/a) |

> The Colab badges point to `github.com/dagbolade/indaba-agentic-ai`. If you push to a
> different repo name, update the badge URLs to match.

---

## Setup (no API key)

There is no key and no signup. The first notebook cell downloads a small open model
(about 1 GB) once, then everything runs locally.

### Option A: Google Colab (recommended for the session)
Click any "Open in Colab" badge above, then run all cells. For speed, switch on a free GPU
first: **Runtime > Change runtime type > T4 GPU**. The model loads in a minute or two; after
that, replies are quick.

### Option B: Run locally
```bash
git clone https://github.com/dagbolade/indaba-agentic-ai.git
cd indaba-agentic-ai
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

The models used are `Qwen/Qwen2.5-0.5B-Instruct` for text and `all-MiniLM-L6-v2` for
embeddings. Both are open and download automatically on first run. A GPU is optional; a CPU
works, just more slowly.

### Troubleshooting

- In a notebook, install with `%pip install ...` (percent sign), not `!pip`, so packages
  land in the running kernel. If an import still fails, restart the kernel and re-run.
- If you see an import error mentioning `huggingface_hub` (for example a missing
  `DeviceCodeError`), a package downgraded it. Fix with
  `%pip install -U "huggingface_hub>=0.24" transformers sentence-transformers`, then restart
  the kernel.
- For the live session, Google Colab is the most reliable environment; local setups vary.

---

## The 2-hour session at a glance

1. **Welcome & framing** (5 min): why agents, why now, why it matters for Africa
2. **What is an AI agent?** (20 min): perceive, reason, act; agents vs. chatbots
3. **Memory in conversational AI** (20 min): short-term vs. long-term; what to forget
4. **Building an agent in Python** (25 min): *live coding,* notebook `00`
5. **Persistent memory with embeddings** (25 min): *live coding,* notebook `02`
6. **Talking to our griot** (15 min): an extended live conversation, and proving the agent remembers across a restart
7. **Sovereign intelligence** (5 min): data, sovereignty, the path forward
8. **Q&A and resources** (5 min)

---

## Why this matters: Sovereign Intelligence

As frontier AI concentrates abroad, the agents that serve African users are too often
built, owned, and hosted elsewhere. This tutorial is deliberately code-forward and runs
entirely on open, self-hostable models: no metered API, no key, no data leaving the machine.
That is the practical core of sovereign intelligence, and it is how locally-built,
locally-owned agents become possible.

For how these classroom patterns scale to a production system, see
[`03_from_prototype_to_production.md`](notebooks/03_from_prototype_to_production.md).

## License

MIT. See [LICENSE](LICENSE). Teaching materials free to reuse and adapt.
