# Algorithm Agent: Automated Building System

This project is a powerful, multi-agent AI system capable of autonomously building any website, application, or workflow based on your natural language requests. It is framework and language agnostic, and will use whichever stack you direct it to use.

## Core Capabilities

- **Universal Project Generation:** Construct any requested frontend UI, backend API, standalone scripts, or complete workflows.
- **Multi-Agent Architecture:**
  - **Decision Agent:** Analyzes the input prompt, maps out task intents, and outlines software architecture efficiently.
  - **Execution Agent:** Writes the project codebase, managing logic and properly creating file structures and dependencies.
  - **Preview Agent:** Handles launching and serving the built web applications locally so you can see live previews dynamically.
  - **Debug & Bug Fix Agent:** Initiates runtime testing. If it catches a crash or bug, it automatically reads the error tracebacks and applies self-repairs in autonomous cycles.

## Project Structure

```text
├── ai_engine/
│   ├── agent/               # Multi-step reasoning loops and agent modules
│   ├── analyzer/            # Intent and task detection from user requests
│   ├── context/             # Gathers required execution prompt contexts
│   ├── core/                # Core AI loop and execution manager pipeline
│   ├── dependency/          # Extracts and manages code requirements
│   ├── document_processing/ # Chunking, generation, and formatting tools for PDFs
│   ├── formatter/           # Response normalization from the LLM integrations
│   ├── memory/              # Agent memory state management
│   ├── planner/             # Plans architecture and maps out task execution graphs
│   ├── project_builder/     # File parsers and dynamic smart project scaffolding
│   ├── providers/           # Connects to AI models (e.g. OpenAI, Gemini)
│   ├── repair/              # Agents focused purely on bug finding and runtime repairs
│   ├── router/              # Directs paths between coding, web research, or conversation
│   ├── tools/               # Registry containing tools (e.g., Python execution, web search)
│   └── validator/           # Intelligent file and entry point verification
├── tests/                   # Engine and component logic testing
├── api.py                   # FastAPI application running the AI integration server
└── readme.md                # Project documentation
```

## How to Run

To launch the AI build server locally:

```bash
python api.py
```

The server runs on `http://0.0.0.0:8000` (accessible at `http://localhost:8000`). It exposes necessary endpoints to generate projects, handle general chat prompts, or test the preview agent.
