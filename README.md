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
git lfs install  # needed anytime you use git as some files are tracked in Git LFS
git clone https://github.com/StonyBrookNLP/appworld; cd appworld  # clone the repo
pip install -e .  # installs package in a local editable mode in ./src/
appworld install --repo  # unpacks encrypted code in the current directory
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
