<div align="center">
<img src="https://img.shields.io/badge/🎁_Gift_Recommendation_Bot-Local_LLM_Powered-blue?style=for-the-badge&labelColor=1a1a2e&color=16213e" alt="Project Banner" width="600"/>

<br/>

<img src="https://img.shields.io/badge/Gemma_4-Ollama-orange?style=flat-square&logo=google&logoColor=white" alt="Gemma 4"/>
<img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Streamlit-Web_UI-red?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/>
<img src="https://img.shields.io/badge/Click-CLI-green?style=flat-square&logo=gnu-bash&logoColor=white" alt="Click CLI"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License"/>

<br/><br/>

<strong>Part of <a href="https://github.com/kennedyraju55/90-local-llm-projects">90 Local LLM Projects</a> collection</strong>

</div>

<br/>
# 🎁 Gift Recommendation Bot

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![LLM](https://img.shields.io/badge/LLM-Ollama%2FGemma4-orange.svg)
![UI](https://img.shields.io/badge/UI-Streamlit-red.svg)

> Find the perfect gift for any occasion with AI-powered personalized suggestions, wishlist management, and an occasion calendar.

## ✨ Features

- **14 Occasions** — Birthday, Christmas, wedding, graduation, and more
- **10 Relationship Types** — Partner, parent, friend, colleague, etc.
- **Budget Aware** — Suggestions within your price range ($5-$10,000)
- **Interest-Based** — Personalized to recipient's hobbies
- **Price Comparison** — Compare prices across retailers
- **Wishlist Management** — Track gift ideas per person
- **Occasion Calendar** — Never miss an important date
- **Detailed Info** — Where to buy and creative presentation ideas
- **Streamlit Web UI** — Full-featured browser interface

## 📦 Installation

```bash
pip install -r requirements.txt
```

## 🚀 CLI Usage

```bash
# Get gift recommendations
python -m gift_recommender.cli recommend --occasion birthday --budget 50 --interests "gaming,cooking"

# Manage wishlists
python -m gift_recommender.cli wishlist-add --person "Mom" --gift "Cookbook" --price "$25"
python -m gift_recommender.cli wishlist-show --person "Mom"

# Occasion calendar
python -m gift_recommender.cli calendar-add --person "Mom" --occasion birthday --date 2025-03-15
python -m gift_recommender.cli calendar-show --days 30
```

## 🌐 Web UI

```bash
streamlit run src/gift_recommender/web_ui.py
```

The web UI provides:
- 🎁 Gift recommendation with form inputs
- 💰 Price comparison tool
- 📋 Wishlist management per person
- 📅 Occasion calendar with reminders

## 🧪 Running Tests

```bash
python -m pytest tests/ -v
```

## 📸 Screenshots

<div align="center">
<table>
<tr>
<td><img src="https://via.placeholder.com/400x250/1a1a2e/e94560?text=CLI+Interface" alt="CLI Interface"/></td>
<td><img src="https://via.placeholder.com/400x250/16213e/e94560?text=Web+UI" alt="Web UI"/></td>
</tr>
<tr>
<td align="center"><em>CLI Interface</em></td>
<td align="center"><em>Streamlit Web UI</em></td>
</tr>
</table>
</div>

## 📁 Project Structure

```
08-gift-recommendation-bot/
├── src/
│   └── gift_recommender/
│       ├── __init__.py       # Package metadata
│       ├── core.py           # Core business logic
│       ├── cli.py            # Click CLI interface
│       ├── web_ui.py         # Streamlit web interface
│       ├── config.py         # Configuration management
│       └── utils.py          # Helper utilities
├── tests/
│   ├── __init__.py
│   ├── test_core.py          # Core logic tests
│   └── test_cli.py           # CLI tests
├── config.yaml               # Default configuration
├── setup.py                  # Package setup
├── requirements.txt          # Dependencies
├── Makefile                  # Common commands
├── .env.example              # Example environment variables
└── README.md                 # This file
```
