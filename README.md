# ChronoSphere: AI Time Service API


![Header](https://user-images.githubusercontent.com/8254624/222209193-e470c1e4-d621-4f93-8686-7b8f2a50ea26.png)


<p align="center">
  <a href="https://github.com/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API/ci.yml?branch=main&style=flat-square" alt="Build Status">
  </a>
  <a href="https://codecov.io/gh/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API">
    <img src="https://img.shields.io/codecov/c/github/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API?style=flat-square" alt="Code Coverage">
  </a>
  <img src="https://img.shields.io/badge/tech-Node.js%20%7C%20TypeScript-blue?style=flat-square" alt="Tech Stack">
  <a href="https://biomejs.dev/">
    <img src="https://img.shields.io/badge/linter-Biome-blueviolet?style=flat-square" alt="Linter">
  </a>
  <a href="https://creativecommons.org/licenses/by-nc/4.0/">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg?style=flat-square" alt="License">
  </a>
  <a href="https://github.com/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API?style=flat-square" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API/stargazers"><strong>Star ⭐ this Repo</strong></a> if you find it useful!
</p>

---

**ChronoSphere is a high-performance, timezone-aware time service API built for the demands of modern AI agents.** It delivers precise, context-rich temporal data, ensuring your automated systems operate with perfect chronological awareness.

This robust NodeJS service provides accurate date and time information across any timezone, essential for context-aware operations, scheduling, and seamless platform integration (e.g., Claude, GPT-4).

## Table of Contents

- [Architecture Overview](#architecture-overview)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Development Standards](#development-standards)
- [🤖 AI Agent Directives](#-ai-agent-directives)
- [Contributing](#contributing)
- [License](#license)

## Architecture Overview

ChronoSphere is built using a Hexagonal (Ports & Adapters) architecture to ensure a clean separation of concerns. The core domain logic is completely isolated from external frameworks and infrastructure, making the system highly testable, maintainable, and adaptable.

sh
.
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   └── ...
├── dist/
├── src/
│   ├── application/    # Use Cases / Application Services
│   ├── domain/         # Core Business Logic & Entities
│   ├── infrastructure/ # External Services (e.g., Database, Caching)
│   └── presentation/   # API Controllers, Routes (e.g., Fastify)
├── tests/
├── .gitignore
├── biome.json
├── package.json
└── tsconfig.json


## Key Features

- **High Precision:** Delivers accurate time data, accounting for leap seconds and daylight saving adjustments.
- **Global Timezone Support:** Query time for any IANA timezone identifier (e.g., `America/New_York`, `Europe/London`).
- **Built for AI:** Provides structured, machine-readable JSON responses perfect for consumption by AI agents and automated workflows.
- **Performant & Scalable:** Built on Node.js and Fastify for low-overhead, high-throughput performance.
- **Strictly Typed:** Fully authored in TypeScript for robust, error-free development.

## Getting Started

### Prerequisites

- Node.js (v20.x or later)
- npm (v10.x or later)

### Installation & Setup

1.  **Clone the repository:**
    sh
    git clone https://github.com/chirag127/ChronoSphere-AI-Time-Service-NodeJS-API.git
    cd ChronoSphere-AI-Time-Service-NodeJS-API
    

2.  **Install dependencies:**
    sh
    npm install
    

3.  **Run the development server:**
    sh
    npm run dev
    
    The API will be available at `http://localhost:3000`.

## API Endpoints

The primary endpoint provides detailed time information for a specified timezone.

**GET** `/api/v1/time?tz=<timezone>`

- **Example Request:** `GET /api/v1/time?tz=America/Los_Angeles`
- **Success Response (200 OK):**
  
  {
    "timezone": "America/Los_Angeles",
    "iso": "2025-12-15T10:30:00.000-08:00",
    "utc_offset": "-08:00",
    "day_of_week": "Monday",
    "unix_timestamp": 1765804200
  }
  

## Development Standards

This project adheres to strict development principles to ensure code quality and maintainability.

### Available Scripts

| Script              | Description                                      |
| ------------------- | ------------------------------------------------ |
| `npm run dev`       | Starts the development server with hot-reloading. |
| `npm run build`     | Compiles TypeScript to JavaScript for production. |
| `npm start`         | Runs the production-ready build.                 |
| `npm run test`      | Executes unit and integration tests with Vitest. |
| `npm run test:cov`  | Runs tests and generates a coverage report.      |
| `npm run lint`      | Lints and formats the codebase with Biome.       |
| `npm run lint:check`| Checks for linting and formatting violations.    |

### Core Principles

- **SOLID:** Code is structured following SOLID principles.
- **DRY (Don't Repeat Yourself):** Reusable logic is abstracted to avoid duplication.
- **YAGNI (You Ain't Gonna Need It):** Features are added only when necessary to avoid bloat.

## 🤖 AI Agent Directives

<details>
<summary><strong>Click to expand: System Instructions for AI Code Generation</strong></summary>

### SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

#### 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards.
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

#### 2. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
This repository, `ChronoSphere-AI-Time-Service-NodeJS-API`, is a TypeScript-based, high-performance API.

*   **PRIMARY SCENARIO: WEB / API (TypeScript)**
    *   **Stack:** This project leverages **TypeScript 5.x (Strict Mode)** and **Node.js 22.x (LTS)**. The web framework is **Fastify** for its superior performance and low overhead.
    *   **Architecture:** Adheres to a **Hexagonal Architecture (Ports & Adapters)**. All core business logic resides within the `src/domain` and `src/application` layers, completely decoupled from external frameworks like Fastify (`src/presentation`) and data sources (`src/infrastructure`). This is the Single Source of Truth.
    *   **Tooling & Testing:** All linting, formatting, and code organization are handled by **Biome**. Unit and integration tests are written and executed with **Vitest**, which provides a fast, modern testing experience.

*   **SECONDARY SCENARIO A: SYSTEMS / PERFORMANCE (Rust) - *Not applicable for this project's primary function.***

#### 3. VERIFICATION & DEPLOYMENT PROTOCOL
*   **Local Validation:** Before committing, you **MUST** run the following commands to ensure 100% compliance with project standards:
    *   `npm run lint` - To format and lint all files.
    *   `npm run test:cov` - To ensure all tests pass and coverage meets the 95% threshold.
*   **CI/CD Pipeline:** All changes are validated through the GitHub Actions workflow defined in `.github/workflows/ci.yml`. The pipeline performs linting, testing, and builds a production-ready artifact.

</details>

## Contributing

Contributions are welcome! Please read the [CONTRIBUTING.md](./.github/CONTRIBUTING.md) file for guidelines on how to submit pull requests.

## License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License](./LICENSE). See the `LICENSE` file for more details.
