# ainfera-crewai — CrewAI + Ainfera Routing

CrewAI integration + Ainfera Routing. Multi-agent crew with one audit chain — 2 env vars.

## Quickstart

```bash
git clone https://github.com/ainfera-ai/ainfera-crewai
cd ainfera-crewai
pip install -r requirements.txt
export AINFERA_API_KEY=ainfera_...  # https://app.ainfera.ai/signup
# Optional overrides: AINFERA_API_URL (default: https://api.ainfera.ai/v1), AINFERA_MODEL (default: ainfera-inference)
python main.py
```

Or with `curl` only:

```bash
./curl-example.sh
```

## What this shows

- Multi-agent flows audited end-to-end (researcher → writer)
- One Agent Card across providers (L1)
- Routed inference with per-call budget caps (L3)
- Hash-chained receipts per call (L4)

> EU AI Act Annex IV ready — every call hash-chained, signed, exportable.

## The whole change

CrewAI's `LLM` class accepts an OpenAI-compatible base URL natively:

```python
llm = LLM(
    model="openai/ainfera-inference",
    api_key=os.environ["AINFERA_API_KEY"],
    base_url="https://api.ainfera.ai/v1",
)
```

Every agent in the crew uses it.

## Other frameworks

- [ainfera-openai-compatible](https://github.com/ainfera-ai/ainfera-openai-compatible) — universal wedge (no framework)
- [ainfera-langchain](https://github.com/ainfera-ai/ainfera-langchain) — LangChain
- [ainfera-google-adk](https://github.com/ainfera-ai/ainfera-google-adk) — Google ADK
- [ainfera-mcp](https://github.com/ainfera-ai/ainfera-mcp) — Claude Desktop + Cursor
- [ainfera-letta](https://github.com/ainfera-ai/ainfera-letta) — Letta (MemGPT)

Apache 2.0. © Ainfera Inc. 2026.
