# 🎁 Gift Recommendation Bot

![Python 3.11+](https://img.shields.io/badge/Python-3.11%2B-3776AB?logo=python&logoColor=white)
![License MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Local LLM](https://img.shields.io/badge/LLM-Gemma%204-FF6F00?logo=google&logoColor=white)
![Privacy First](https://img.shields.io/badge/Privacy-First-blueviolet?logo=lock&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Powered-black?logo=ollama&logoColor=white)

**AI-powered gift finder that suggests personalized presents based on recipient, occasion, and budget — running 100% locally with Gemma 4.**

```
+---------------------------------------------------------+
|               GIFT RECOMMENDATION BOT                   |
|                                                         |
|  +----------+    +---------------+    +--------------+  |
|  | User      |--->|  CLI / Web UI |--->| Recommend.   |  |
|  | Input     |<---|  (Rich /      |<---|  Engine      |  |
|  | (occasion |    |  Streamlit)   |    +------+-------+  |
|  |  budget   |    +---------------+           |          |
|  |  person)  |                                v          |
|  +----------+    +---------------+    +--------------+  |
|                  | Wishlist &    |<-->|  Ollama API  |  |
|  +----------+    | Calendar      |    |  (Gemma 4)   |  |
|  | Occasion  |<--| Manager       |    |  :11434      |  |
|  | Calendar  |   +---------------+    +--------------+  |
|  | (JSON)    |                                          |
|  +----------+                                           |
+---------------------------------------------------------+
```

## Features

- **Smart Recommendations** — Get 5-7 personalized gift ideas with price ranges and purchase links
- **14 Occasions** — Birthday, Christmas, anniversary, wedding, graduation, and 9 more built-in
- **10 Relationships** — Partner, parent, sibling, friend, colleague, and more
- **Budget Aware** — Set a dollar limit and get options at different price points
- **Gift Detail Drilldown** — Explore any suggestion for DIY alternatives and presentation ideas
- **Price Comparison** — Compare retailers and get deal tips for any gift idea
- **Wishlist Manager** — Save gift ideas per person with purchase tracking
- **Occasion Calendar** — Never miss a birthday or anniversary with upcoming-event alerts
- **Web UI + CLI** — Beautiful Streamlit dashboard or rich terminal interface
- **100% Local & Private** — Gift lists and personal data never leave your machine

## Quick Start

### Prerequisites

| Requirement | Version |
|-------------|---------|
| Python      | 3.11+   |
| Ollama      | latest  |
| Gemma 4     | via Ollama |

### Install & Run

```bash
# 1. Clone the repository
git clone https://github.com/kennedyraju55/gift-recommendation-bot.git
cd gift-recommendation-bot

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start Ollama and pull Gemma 4
ollama serve &
ollama pull gemma4

# 4a. Launch the Web UI
streamlit run src/gift_recommender/web_ui.py

# 4b. Or use the CLI
python -m gift_recommender.cli recommend --occasion birthday --relationship friend --budget 50
```

### Docker

```bash
docker-compose up
# Web UI at http://localhost:8501
```

## Tech Stack

| Layer        | Technology                          |
|-------------|--------------------------------------|
| LLM          | Gemma 4 via Ollama                  |
| Backend      | Python 3.11, Click CLI              |
| Web UI       | Streamlit                           |
| API          | FastAPI / Uvicorn                   |
| Terminal UI  | Rich (panels, tables, progress)     |
| Config       | PyYAML                              |
| Testing      | pytest, pytest-cov                  |
| Containers   | Docker, Docker Compose              |

## Project Structure

```
gift-recommendation-bot/
├── src/gift_recommender/
│   ├── core.py         # Recommendation engine, wishlists, calendar
│   ├── cli.py          # Click CLI with Rich output
│   ├── web_ui.py       # Streamlit web dashboard
│   ├── api.py          # FastAPI REST endpoints
│   ├── config.py       # YAML configuration loader
│   └── utils.py        # LLM client helpers & utilities
├── common/
│   └── llm_client.py   # Shared Ollama/Gemma 4 client
├── tests/
│   ├── test_core.py    # Unit tests for core logic
│   └── test_cli.py     # CLI integration tests
├── config.yaml         # Occasions, relationships, storage paths
├── requirements.txt    # Python dependencies
├── Dockerfile          # Multi-stage Docker build
├── docker-compose.yml  # Full stack with Ollama
├── Makefile            # Dev shortcuts (install, test, run)
└── setup.py            # Package setup with entry points
```

## Author

**Nrk Raju Guthikonda**
Senior Software Engineer @ Microsoft — Copilot Search Infrastructure

- GitHub: [kennedyraju55](https://github.com/kennedyraju55)
- Dev.to: [kennedyraju55](https://dev.to/kennedyraju55)
- LinkedIn: [nrk-raju-guthikonda](https://linkedin.com/in/nrk-raju-guthikonda-504066a8/)

---

<p align="center">Built with Gemma 4 — part of a 90+ local LLM project portfolio</p>
