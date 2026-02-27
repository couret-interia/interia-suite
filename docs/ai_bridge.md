# 🤖 InterIA AI Bridge

The AI Bridge provides a transparent pipeline to involve external LLMs
(ChatGPT, Claude, Gemini, etc.) in refactoring, without turning the
process into a black box.

## Workflow

> Note: same commands with `interia-quality` or `make` (vendored)

1. Build a refactor plan:

    ```bash
    make refactor-plan
    ```

2. Build the AI request:

    ```bash
    make ai-request
    ```

   → produces `ai_request.json`

3. Paste `ai_request.json` into your LLM of choice, ask for structured edits,
   and save the result as `ai_response.json`.

4. Preview:

    ```bash
    make ai-preview
    ```

    → opens `ai_preview.html`

5. Apply edits:

    ```bash
    make ai-apply
    ```

All intermediate files (`refactor_plan.json`, `ai_request.json`, `ai_response.json`)
are JSON, human-readable, diffable and reversible.
