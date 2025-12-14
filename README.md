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
pip install git+https://github.com/stonybrooknlp/appworld.git  # installs package in your site-packages directory
appworld install  # unpacks encrypted code in your site-packages directory
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
