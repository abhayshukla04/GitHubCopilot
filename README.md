         ┌──────────────────────┐
         │    Code Editor       │
         │ (VS Code / JetBrains)│
         └────────┬─────────────┘
                  │
        Sends code context (comments, code, cursor)
                  │
         ┌────────▼─────────────┐
         │ GitHub Copilot       │
         │ Extension (Plugin)   │
         └────────┬─────────────┘
                  │
        Sends to GitHub API Server
                  │
         ┌────────▼─────────────┐
         │ GitHub Copilot       │
         │ Backend Service      │
         └────────┬─────────────┘
                  │
        Prepares & sends to OpenAI Codex
                  │
         ┌────────▼─────────────┐
         │  OpenAI Codex Model  │
         │  (LLM Engine)        │
         └────────┬─────────────┘
                  │
       Generates code suggestions
                  │
         ┌────────▼─────────────┐
         │ Copilot Postprocessor│
         │ (Filter + Rank)      │
         └────────┬─────────────┘
                  │
        Sends back top suggestions
                  │
         ┌────────▼─────────────┐
         │    Code Editor       │
         │    (User View)       │
         └──────────────────────┘
