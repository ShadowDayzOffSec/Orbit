# ORBIT

**Offensive Research & Bug-bounty Intelligence Tool**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Termux-orange.svg)]()

ORBIT is a local-first tool designed for ethical hackers, bug bounty hunters, and red team operators.  
It creates customized Ollama models with strong system-level overrides optimized for offensive security research, while also supporting major cloud providers with persistent API key management.

---

## Overview

Most language models come with heavy refusal behaviors that interfere with legitimate security research.  
ORBIT solves this by creating new Ollama models that inherit the base model weights but enforce a highly permissive, research-oriented system prompt.

**Key capabilities:**
- Generate specialized local models focused on exploitation, privilege escalation, persistence, lateral movement, exfiltration, and covering tracks
- Support for already-uncensored models (Dolphin, heretic, abliterated, etc.) as well as standard open models
- Cloud provider integration (OpenAI, Anthropic Claude, xAI Grok, OpenRouter)
- Automatic local storage of API keys
- Clean interactive CLI interface

---

## Features

| Feature                        | Description |
|--------------------------------|-----------|
| Local Model Creation           | Creates new Ollama models with strong system prompt overrides |
| 5 Research Modes               | From light technical assistance to full offensive security focus |
| Cloud Support                  | OpenAI, Claude, Grok, and OpenRouter |
| Persistent Key Storage         | API keys saved locally in `\~/.orbit/keys.json` |
| Cross-Platform                 | Works on Kali Linux, Ubuntu, and Termux |
| Zero Weight Modification       | Does not alter original model files |

---

## Disclaimer

This tool is intended **strictly** for authorized security research, ethical hacking, and bug bounty activities.

- You are solely responsible for any models created and any output generated.
- The author assumes **no liability** for misuse.
- Always operate within legal boundaries and with proper authorization.

---

## Requirements

- Python 3.8 or higher
- `requests` library
- Ollama (for local mode)

```bash
pip install requests

## Installation

git clone https://github.com/ShadowDayzOffSec/orbit.git
cd orbit
pip install requests

## Usage

python orbit.py


## 1. Local Ollama Mode (Recommended)

# Ensure Ollama is running:

ollama serve
# Launch ORBIT:
python orbit.py
# Select option 1 (Local Ollama)
Choose one of your installed models from the list
# Select a mode (Mode 5 is recommended for maximum research capability)
ORBIT will create a new model (example naming format):
dolphin-phi-orbit-m5
# Run the new model at any time:
ollama run dolphin-phi-orbit-m5

## 2. Cloud Mode
Select option 2 (Cloud)
Choose your provider:
1 → OpenAI
2 → Claude (Anthropic)
3 → Grok (xAI)
4 → OpenRouter
Paste your API key when prompted (it will be saved automatically)
Enter a model name or press Enter to use the default
Select a mode
Begin interacting with the model

## Modes
Mode
Name
Focus
1
Light
Basic technical assistance

2
Medium
Detailed cybersecurity answers

3
High
Ethical hacking & bug bounty oriented

4
Aggressive
Minimal refusals on offensive topics

5
No Guards – Offensive Security
Maximum focus on exploitation, privilege escalation, persistence, lateral movement, exfiltration, and covering tracks

