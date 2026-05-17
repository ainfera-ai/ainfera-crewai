# examples-crewai — Ainfera + CrewAI

Multi-agent content team backed by Ainfera. Two agents, two tasks, one
audit chain.

## Quickstart

```bash
git clone https://github.com/ainfera-ai/examples-crewai
cd examples-crewai
pip install -r requirements.txt
export AINFERA_API_KEY=ai_infera_...  # https://app.ainfera.ai/signup
python main.py
```

## What this shows

- Multi-agent flows audited end-to-end (researcher → writer)
- One Agent Card across providers (L1)
- Drain-proof wallet — survives prompt injection (L3)
- Hash-chained receipts per call (L4)

> EU AI Act Annex IV ready — every call hash-chained, signed, exportable.

## The whole change

CrewAI's `LLM` class accepts an OpenAI-compatible base URL natively:

```python
llm = LLM(
    model="openai/claude-opus-4-7",
    api_key=os.environ["AINFERA_API_KEY"],
    base_url="https://api.ainfera.ai/v1",
)
```

Every agent in the crew uses it.

## Other frameworks

- [examples-openai-compat](https://github.com/ainfera-ai/examples-openai-compat) — universal wedge (no framework)
- [examples-langchain](https://github.com/ainfera-ai/examples-langchain) — LangChain
- [examples-google-adk](https://github.com/ainfera-ai/examples-google-adk) — Google ADK
- [examples-mcp](https://github.com/ainfera-ai/examples-mcp) — Claude Desktop + Cursor

Apache 2.0. © Ainfera Inc. 2026.
