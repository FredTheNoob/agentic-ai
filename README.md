# Agentify Example: AppWorld

Example code for agentifying AppWorld using A2A and MCP standards.

## Project Structure

```
src/
├── green_agent/    # Assessment manager agent
├── white_agent/    # Target agent being tested
└── launcher.py     # Evaluation coordinator
```

## Installation

```bash
uv sync
```

```bash
git lfs install
git clone https://github.com/StonyBrookNLP/appworld; cd appworld
uv pip install -e .
appworld install --repo
appworld download data
```

Verify AppWorld installation
```bash
appworld verify tests
appworld verify tasks
```

## Usage

First, configure `.env` with `OPENAI_API_KEY=...`, then

```bash
# Launch complete evaluation
uv run python main.py launch
```
