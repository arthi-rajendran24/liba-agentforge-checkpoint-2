# LIBA AgentForge Checkpoint 2

Clone this repository for a complete Checkpoint 2 reference, or open it beside a student's Checkpoint 1 project in Google Antigravity. It contains all Checkpoint 1 code plus the compatibility adapter, shared service and Streamlit interface.

## Checkpoint 2: live-capable domain agent

This branch inherits Checkpoint 1 and adds a single compatibility seam, shared service and local Streamlit interface. Rehearsal mode makes no model or network call. Live mode makes one Gemini request only after the deterministic tool succeeds.

```sh
git clone https://github.com/arthi-rajendran24/liba-agentforge-checkpoint-2.git
cd liba-agentforge-checkpoint-2
uv sync
uv run pytest -q
uv run streamlit run app.py
```

If Checkpoint 1 already passes, preserve the student's domain tool and tests. Ask Antigravity to inspect `patches/checkpoint-1-to-2.patch` and adapt only `src/agentforge/student_adapter.py` when necessary.

Previous checkpoint: https://github.com/arthi-rajendran24/liba-agentforge-checkpoint-1  
Next checkpoint: https://github.com/arthi-rajendran24/liba-agentforge-checkpoint-3
