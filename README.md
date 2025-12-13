# ChronoSphere-AI-Date-Time-MCP-NodeJS-API

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API/ci.yml?branch=main&style=flat-square)](https://github.com/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API/actions/workflows/ci.yml)[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API?style=flat-square)](https://codecov.io/gh/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API)[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-ff69b4?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/)[![GitHub Stars](https://img.shields.io/github/stars/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API?style=flat-square)](https://github.com/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API/stargazers)

## Introduction
ChronoSphere provides an AI‑enabled Model Context Protocol (MCP) API built with TypeScript/Node.js, delivering precise, locale‑aware date and time data across timezones for real‑time AI agent operations.

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [AI Agent Directives](#ai-agent-directives)
- [Contributing](#contributing)
- [License](#license)

## Getting Started
To get started with ChronoSphere, follow these steps:
### Step 1: Clone the repository
bash
 git clone https://github.com/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API.git

### Step 2: Install dependencies
bash
npm install

### Step 3: Start the API
bash
npm start


## AI Agent Directives
<details>
<summary>View AI Agent Directives</summary>

### Cerebras Inference Configuration
* **Base URL:** `https://api.cerebras.ai/v1`
* **API Key Variable:** `CEREBRAS_API_KEY`
* **Library:** Use the standard `openai` Node.js library.
javascript
const { OpenAI } = require('openai');
const cerebrasClient = new OpenAI({
  base_url: 'https://api.cerebras.ai/v1',
  api_key: process.env.CEREBRAS_API_KEY,
});


### Model Hierarchy (Fallback Cascade)
Always attempt the highest-parameter model first for complex reasoning, cascading down for speed.
* **Tier 1 (Frontier Intelligence):** `zai-glm-4.6` (357B)
* **Tier 2 (Heavy Reasoning):** `qwen-3-235b-a22b-instruct-2507` (235B)
* **Tier 3 (General Purpose):** `gpt-oss-120b` (120B)
* **Tier 4 (Balanced Workhorse):** `llama-3.3-70b` (70B)
* **Tier 5 (Fast Inference):** `qwen-3-32b` (32B)
* **Tier 6 (Ultra-Fast/Instant):** `llama3.1-8b` (8B)

### Operational Limits
* **Max Output Tokens:** `32768` (Free Tier Limit)
* **Context Window:** 65,536 (Free Tier)
* **Concurrency:** `MAX_WORKERS = 5` (Free Tier Safe Limit)
* **Circuit Breaker:** On 429/500 error, trigger **Exponential Backoff** (start 2s) and retry.

</details>

## Contributing
Please see [CONTRIBUTING.md](https://github.com/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API/blob/main/CONTRIBUTING.md) for details on how to contribute to this project.

## License
This project is licensed under the [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) license. See [LICENSE](https://github.com/chirag127/ChronoSphere-AI-Date-Time-MCP-NodeJS-API/blob/main/LICENSE) for more information.

Star ⭐ this Repo if you find it useful!