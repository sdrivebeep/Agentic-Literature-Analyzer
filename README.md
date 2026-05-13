# Agentic Literature Analyzer

## Overview
The **Agentic Literature Analyzer** is a multi-agent automated pipeline designed to solve the core pain points in academic research: extreme fragmentation of cross-lingual primary sources, massive time consumption in long-text reading, and implicit logical conflicts (e.g., mismatched timelines or contradictory entity relations) across different historical archives.

## Core Architecture & Agent Workflow

This system employs a multi-tiered agent architecture, chaining different LLMs based on their specific strengths to form a closed-loop automated pipeline.

### 1. OSINT Retrieval Layer (Powered by Perplexity)
*   **Action**: Automates Open-Source Intelligence (OSINT) gathering.
*   **Role**: Scrapes and aggregates multilingual raw documents related to specific research topics from academic databases and open web sources.

### 2. Extraction & Translation Layer (Powered by DeepSeek)
*   **Action**: Executes high-precision cross-lingual translation and Named Entity Recognition (NER).
*   **Role**: Standardizes raw, unstructured data into structured JSON formats, extracting key nodes such as time, locations, and events.

### 3. Logic Validation & Reasoning Layer (Powered by Gemini)
*   **Action**: Leverages massive context windows for cross-validation.
*   **Role**: The Agent feeds the extracted datasets into the context window, automatically comparing hundreds of sources to identify historical discrepancies, outputting a conflict report with a confidence score.

### 4. Knowledge Reconstruction Layer (Powered by Local Codex/Hermes)
*   **Action**: Local knowledge base integration.
*   **Role**: Formats the reasoning results into standardized Markdown cards and writes them directly into the local Obsidian Vault for permanent storage.

## Business Value & Token Consumption
This system significantly reduces the time required for cross-referencing multi-source literature from days to minutes. The continuous ingestion of long-form texts and the complex internal reasoning required for conflict resolution generate a substantial, high-density, and stable demand for API Tokens.

> **Note:** This repository currently serves as a demonstration of the core workflow and prompt chaining logic for the Xiaomi MiMo API application process. The full implementation requires specific API keys for the respective models.
