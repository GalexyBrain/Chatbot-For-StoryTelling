# Chatbot-For-StoryTelling

A Python storytelling chatbot that generates stories through a chat-style experience.

---

## What’s in this repo

- `AIProject.py` — core chatbot/story-generation logic
- `gui.py` — GUI entry point (chat interface)
- `requirements.txt` — Python dependencies
- `README.md` — project overview

---

## Features (high level)

- Chat-based story generation (interactive storytelling)
- Optional GUI to interact with the bot
- Simple, small project footprint (single-purpose scripts)

---

## Getting started

### 1) Prerequisites

- Python 3.9+ (3.10/3.11 recommended)
- pip (or pipx/uv/poetry if you prefer)

### 2) Clone the repo

```bash
git clone https://github.com/GalexyBrain/Chatbot-For-StoryTelling.git
cd Chatbot-For-StoryTelling
````

### 3) Create a virtual environment (recommended)

**Windows (PowerShell)**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4) Install dependencies

```bash
pip install -r requirements.txt
```

---

## Run the chatbot

### Option A: Run the GUI

```bash
python gui.py
```

If a window opens, you should be able to type prompts (genre, characters, setting, etc.) and get story responses.

### Option B: Run the core script directly

```bash
python AIProject.py
```

If this script is meant to be imported (and not executed), you’ll typically run only the GUI, or you’ll add a small CLI wrapper (see below).

---

## Example prompts you can try

* “Write a fantasy story set in a floating city where memories are currency.”
* “Give me a sci-fi detective story with a twist ending in under 800 words.”
* “Start a children’s bedtime story about a shy dragon. Ask me to choose what happens next.”

---

## Configuration

Some storytelling chatbots use an LLM provider (API key) or local model runtime. If your setup needs credentials:

1. Search the code for keywords like: `API_KEY`, `openai`, `gemini`, `anthropic`, `huggingface`, `dotenv`, `os.environ`.
2. Add environment variables accordingly.

If the project uses a `.env` file, a common pattern is:

```bash
# .env (example)
OPENAI_API_KEY="your_key_here"
```

Then run the program again.

> If you don’t see `.env` support, you can still export env vars in your shell or add it in code (not recommended for committed secrets).

---

## Troubleshooting

* **`ModuleNotFoundError`**: make sure your venv is activated and you installed `requirements.txt`.
* **GUI doesn’t open**: run `python gui.py` from the repo root and check terminal output for errors.
* **It runs but responses are empty/odd**: verify any model/API configuration and try simpler prompts first.

---

## Project structure suggestion (optional improvement)

If you want this to be easier to run and extend, consider:

* Add a `main.py` as a single entry point
* Move logic into a package folder (e.g., `storybot/`)
* Add a `.env.example` (never commit real keys)
* Add basic tests for prompt/response formatting

---

## Contributing

PRs are welcome. A good flow:

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/my-change`
3. Commit changes
4. Open a PR
