# Slide Outline: Introduction to Agentic AI (2 hours)

*Deep Learning Indaba 2026, lecture style with live coding.*

Timings match the submitted outline. Live-coding blocks switch to the notebooks. Everything
runs on a small open model locally, so there is no API key step.

## Segment 0: Welcome and framing (5 min)
Title, why agents now, the sovereign-intelligence lens, roadmap and a quick poll.

## Segment 1: What is an AI agent? (20 min)
One model call is not an agent. Perceive, reason, act. Agent vs. chatbot. Anatomy: model,
instructions, tools, memory. Meet the griot.

## Segment 2: Building an agent in Python, live (20 min)
`00_minimal_agent.ipynb`: load a small open model, one call, a first tool, in-session memory,
watch it forget on restart.

## Segment 3: Memory in conversational AI (20 min)
Stateless models; the context window; short vs. long term; what to forget. Run
`01_short_term_memory.ipynb`: watch tokens climb, then summarise.

## Segment 4: Giving agents tools, live (15 min)
`04_agent_tools.ipynb`: the model is frozen in time and cannot know the current weather; give
it a tool that calls a free, no-key weather API; let the agent call it (reason, act, respond)
and lead the reply with the real reading. The point: tools let the agent reach live external
services, while the model itself stays local and private.

## Segment 5: Persistent memory with embeddings, live (20 min)
`02_vector_memory.ipynb`: embeddings and cosine; a tiny vector store; retrieve, augment,
respond; reload from disk to prove persistence.

## Segment 6: Talking to our griot, live (10 min)
An open conversation; the room steers the tale; restart and show the saga persists from disk.

## Segment 7: Sovereign intelligence (5 min)
Data scarcity and bias; where models run, where data lives, who pays; local and self-hosted
models as the path to ownership.

## Segment 8: Q&A and resources (5 min)
Repo, notebooks, Colab links. Invite collaboration.

### Speaker notes
- Re-ground each idea in the live demo within about two minutes of introducing it.
- Keep code on screen large and narrate every line for the mixed-background room.
- Lean on the no-key, local-model setup as the concrete sovereignty story.
