# Slide Outline: Introduction to Agentic AI (2 hours)

*Deep Learning Indaba 2026, lecture style with live coding.*

Timings match the submitted outline. Live-coding blocks switch to the notebooks, so they
need only a "title and goal" holder slide each. Everything runs on a small open model
locally, so there is no API key step.

## Segment 0: Welcome and framing (5 min)
1. Title: Introduction to Agentic AI. Name, affiliation, the Indaba theme line.
2. Why agents, why now: chatbots become agents that remember and act.
3. The sovereign-intelligence lens: who builds, owns, and hosts Africa's agents?
4. Roadmap and a quick poll of the room's backgrounds.
5. Framing line: "we build a simplified version of the same concepts that run in real systems," all on open, self-hostable models.

## Segment 1: What is an AI agent? (20 min)
6. From one model call to an agent: a single call is not yet an agent.
7. The perceive, reason, act loop.
8. Agent vs. chatbot vs. plain prompting: a comparison.
9. Anatomy of an agent: model, instructions, tools, memory.
10. Meet our example: a griot storyteller agent, and why storytelling makes memory tangible.

## Segment 2: Memory in conversational AI (20 min)
11. Models are stateless: they only know what is in the request.
12. The context window: big but finite, and you pay per token.
13. Short-term vs. long-term memory.
14. What to remember vs. forget: TTLs, summarisation, cost.
15. African angle: memory on low-bandwidth, intermittent connections.

## Segment 3: Building an agent in Python, live (25 min)
16. Holder slide: open `00_minimal_agent.ipynb`. Goal: a working griot agent in under 100 lines, no key.
    - Beats: load a small open model, one call, add a tool via a simple reason-act loop, in-session memory, watch it forget on restart.
17. Recap: what we built, and the limitation that motivates persistence.

## Segment 4: Persistent memory with embeddings, live (25 min)
18. Embeddings, intuitively: text becomes vectors; meaning as direction.
19. Cosine similarity in one picture.
20. Holder slide: open `02_vector_memory.ipynb`. Goal: a saga that survives a restart.
    - Beats: embed events, a tiny vector store, retrieve by meaning, augment, continue, reload from disk.
21. From prototype to production: your code vs. a real vector database with a short and long-term split.

## Segment 5: Talking to our griot, live (15 min)
22. An open, unscripted conversation with the agent; let the room steer the tale.
23. Show short-term memory holding within the chat, then restart and show the saga persists from disk.
24. A few honest notes on running open models: model size, speed, and quality trade-offs.

## Segment 6: Sovereign intelligence (5 min)
25. Data scarcity and bias: training on non-African datasets and what breaks.
26. Sovereignty: where models run, where data lives, who pays.
27. Practical steps: local datasets, local voices, local and self-hosted models and hosting.

## Segment 7: Q&A and resources (5 min)
28. Resources: repo, notebooks, Colab links.
29. Thank you and contact.

### Speaker notes
- Re-ground each idea in the live griot demo within about two minutes of introducing it.
- Keep code on screen large and narrate every line for the mixed-background room.
- Lean on the no-key, local-model setup as the concrete sovereignty story.
