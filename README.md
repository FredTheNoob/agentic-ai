# Agentify Example: AppWorld

Example code for agentifying AppWorld using A2A and MCP standards.

## AppWorld Documentation
The documentation for AppWorld can be found here: https://github.com/StonyBrookNLP/appworld.

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

First, configure `.env` with `OPENROUTER_API_KEY=...` and setup your domain, then

```bash
HTTPS_ENABLED=true CLOUDRUN_HOST=YOUR_DOMAIN ROLE=AGENT_ROLE PORT=xxxx agentbeats run_ctrl # Replace "YOUR_DOMAIN and "AGENT_ROLE" and "xxxx"
```

> [!CAUTION]
> Do not run both the white agent and green agent from the same working directory

For local evaluation

```bash
# Launch complete evaluation
uv run python main.py launch
```

For remote evaluation, host the GREEN_URL and WHITE_URL publicly, then

```bash
uv run python main.py launch-remote GREEN_URL WHITE_URL
```

## Tests

To run green agent test cases

```bash
uv run python main.py launch-test-cases
```
