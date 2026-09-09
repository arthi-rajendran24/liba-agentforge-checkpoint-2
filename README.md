# LIBA AgentForge Checkpoint 2

Checkpoint 2 is the second runnable subset of the canonical [AgentForge repository](https://github.com/arthi-rajendran24/agentforge). It contains Checkpoint 1 plus a real LangChain tool-calling agent and a small FastAPI browser interface that use the same package, domain identifiers and tool names as the complete application.

```sh
git clone https://github.com/arthi-rajendran24/liba-agentforge-checkpoint-2.git
cd liba-agentforge-checkpoint-2
uv sync --frozen
uv run pytest -q
uv run python workshop/checkpoint_app.py
```

Open `http://127.0.0.1:8787`. Rehearsal mode makes no external request but still traverses LangChain's agent and tool loop. Live mode makes a deliberate Gemini request using the private environment variables described in `.env.example`. The service rejects an answer that lacks successful tool evidence.

Checkpoint 3 is the complete canonical repository: [liba-agentforge-checkpoint-3](https://github.com/arthi-rajendran24/liba-agentforge-checkpoint-3). The full cumulative contract is in `workshop/CHECKPOINT_PATH.md`.
