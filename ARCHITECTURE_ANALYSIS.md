# BettaFish Architecture Analysis Report

**Project:** BettaFish (微舆 - MicroPublicOpinion)  
**Version:** v1.2.1  
**Date:** November 18, 2024  
**Analysis Type:** Comprehensive Architecture Analysis

---

## Project Overview

BettaFish (微舆, meaning "Micro Public Opinion") is an innovative multi-agent public opinion analysis system built from scratch in Python. The system helps users break through information echo chambers, restore the original state of public opinion, predict future trends, and assist decision-making. Users simply need to pose analysis requirements conversationally, and the system automatically analyzes over 30 mainstream domestic and international social media platforms along with millions of public comments.

The system represents a sophisticated implementation of a multi-agent architecture where specialized AI agents collaborate through a forum-based discussion mechanism. Each agent is equipped with unique toolsets and cognitive models, engaging in chain-of-thought debate moderated by a host agent. This approach avoids the thinking limitations of single models and the homogenization caused by direct communication, generating higher-quality collective intelligence and decision support.

While BettaFish begins with public opinion analysis, its modular design makes it a lightweight, general-purpose data analysis engine that can be adapted to various business scenarios. For example, by simply modifying API parameters and prompts in the agent toolsets, it can be transformed into a financial market analysis system or other domain-specific analysis platforms.

### Main Technologies

**Languages & Core Frameworks:**
- Python 3.11+
- Flask 2.3.3 (web server and orchestration)
- Streamlit 1.28.1 (agent UI interfaces)
- Flask-SocketIO 5.3.6 (real-time communication)

**LLM Integration:**
- OpenAI-compatible API interface (supports multiple LLM providers)
- Default models: Kimi K2 (Insight), Gemini 2.5 Pro (Media/Report), DeepSeek (Query), Qwen (Forum Host)
- Local sentiment analysis models (BERT, GPT-2, transformer-based)

**Databases:**
- PostgreSQL 15 (primary, recommended)
- MySQL (alternative support)
- SQLAlchemy 2.0.35 (ORM and async support)
- asyncpg, asyncmy, aiomysql (async database drivers)

**Web Scraping & Automation:**
- Playwright 1.45.0 (browser automation)
- MediaCrawler (custom multi-platform scraper)
- BeautifulSoup4, lxml, parsel (HTML parsing)

**Search APIs:**
- Tavily API (international news search)
- Bocha AI Search API (multimodal Chinese content search)

**Machine Learning:**
- PyTorch 2.0+ (deep learning)
- Transformers 4.30+ (LLM and sentiment models)
- scikit-learn 1.3+ (traditional ML)
- XGBoost 2.0+ (gradient boosting)

**Data Processing & Visualization:**
- pandas 2.0+, numpy 1.24+
- plotly 5.17+, matplotlib 3.9.0
- wordcloud 1.9.3

**DevOps:**
- Docker & Docker Compose
- uv (fast Python package installer)

---

