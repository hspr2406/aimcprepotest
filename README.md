# AI Demo Project

A beginner-friendly demo project exploring AI capabilities using the Claude API.

## Overview

This project demonstrates how to interact with AI models programmatically — a first step into building AI-powered applications. It covers basic API usage, sending prompts, and handling responses.

> **Note:** This demo will be presented in online mode.

## Features

- Connect to the Claude AI API
- Send prompts and receive AI-generated responses
- Simple, readable code for learning purposes

## Getting Started

### Prerequisites

- Python 3.8+
- An [Anthropic API key](https://console.anthropic.com/)

### Installation

```bash
git clone https://github.com/hspr2406/aimcprepotest.git
cd aimcprepotest
pip install anthropic
```

### Usage

Set your API key as an environment variable:

```bash
export ANTHROPIC_API_KEY=your_api_key_here
```

Run the demo:

```bash
python main.py
```

## Example

```python
import anthropic

client = anthropic.Anthropic()

message = client.messages.create(
    model="claude-sonnet-4-6",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Hello, Claude! What can you do?"}
    ]
)

print(message.content[0].text)
```

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
