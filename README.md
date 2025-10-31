# HedgeFund Multi-Agent System

HedgeFund Multi-Agent System is an intelligent investment simulation built for Hugging Face Spaces.  
It leverages multiple cooperative AI agents to perform market analysis, risk evaluation, trading decisions, and cost computation — producing a professional investment report in Markdown and JSON formats.

**Live Demo:** [https://huggingface.co/spaces/Rosehu/day3](https://huggingface.co/spaces/Rosehu/day3)

**Developed as part of the NITA Agentic AI Bootcamp & Hackathon**

---

## Overview

The system simulates how an AI-powered hedge fund can manage and optimize investments through intelligent collaboration.  
It combines real market data and AI reasoning to produce a full investment plan with actionable insights.

**Key Features:**
- Fetches real-time stock data via Yahoo Finance (`yfinance`)
- Generates buy/sell/hold signals
- Performs financial sentiment analysis
- Evaluates risk and trade approvals
- Computes fees, taxes, and net results
- Produces a Markdown report and JSON output for full transparency

---

## Work Overflow (Agents Hierarchy)

| Role | Agent Name | Description |
|------|-------------|--------------|
| Manager | Manager Agent | Coordinates all agents and compiles the final Markdown + JSON report |
| Market | Market Agent | Collects real market data and generates buy/sell/hold signals |
| Analyzer | Analyzer Agent | Performs sentiment analysis on financial news |
| Trader | Trader Agent | Suggests trades based on signals and sentiment |
| Risk | Risk Agent | Approves or rejects trades based on the selected risk level |
| Tax | Tax Agent | Calculates fees, taxes, and the net financial effect of trades |

Each agent operates sequentially to create a coherent and realistic portfolio simulation.

---

## System Input

Users can customize the simulation through:

- **Goal:** Example – "Grow my portfolio safely over 5 days"
- **Starting Money ($):** Example – 10,000
- **Risk Level:** Low / Medium / High
- **Assets:** Comma-separated symbols (e.g., `AAPL, TSLA`)
- **Trading Frequency:** Daily / Weekly
- **Start Date:** Optional (defaults to today)

---

## System Output

Once all agents complete their workflow, the system generates:

1. **Markdown Report (`.md`)**
   - Portfolio Summary
   - Trades Executed (including fees/taxes)
   - Risk Approvals
   - Recommendations

2. **JSON Report (`.json`)**
   - Structured output with all portfolio and trade details

Both reports are stored in the `hedgefund_outputs/` directory.

