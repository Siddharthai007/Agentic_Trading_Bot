### keys needs to be mention inside the .env
```
POLYGON_API_KEY
GOOGLE_API_KEY
TAVILY_API_KEY
GROQ_API_KEY
PINECONE_API_KEY
```

### for running the fastapi endpoint
```
uvicorn main:app --host 0.0.0.0 --port 8000 --reload

```

### for running the streamlit ui
```
streamlit run streamlit_ui.py

```

### for installing the requirements
```
pip install -r requirements.txt
```

### for creating the env
```
conda create -p env python=3.10 -y
```

### for activate the env through cmd
```
conda activate <env_path>
```
# Agentic Trading Bot  
**Autonomous trading framework for stocks/crypto with agent-based strategies and tool-orchestrated workflows.**

---

## 🚀 Overview  
This project implements an agentic trading bot designed to make autonomous decisions in trading markets (stocks, crypto, etc.). The system uses tool orchestration, modular strategy components, data pipelines, and a feedback loop for adaptivity — aimed at research, prototyping, or production-level trading experiments.

Key features include:  
- 🔹 Agent core – orchestrates trading tools & workflows  
- 🔹 Data ingestion & feature pipelines – market data, indicators, preprocessing  
- 🔹 Strategy modules – signal generation, risk & money management  
- 🔹 Execution layer – interface to broker/API (live or paper)  
- 🔹 Evaluation & back-testing components  

---

## 📂 Project Structure (high-level)


├── agent/ # core agent logic and orchestration

├── data_ingestion/ # scripts for collecting & cleaning market data

├── strategies/ # different trading strategies/modules

├── execution/ # execution logic (broker API, simulation environment)

├── eval/ # back-testing, performance metrics, logging

├── docs/ # architecture diagrams, notes

├── requirements.txt

── setup.py

└── README.md



## 🧩 Features
✔️ Agent-based orchestration

The bot’s core distributes tasks (data fetch → strategy evaluation → order execution → logging) to independent modules, enabling modularity and extendibility.

✔️ Modular strategy and tool pipelines

Swap or add new strategy modules easily (momentum, mean-reversion, machine-learning) and add new tools (risk-manager, portfolio rebalance, trade logger).

✔️ Data ingestion & feature engineering

Scrapes or downloads market data, computes indicators, cleans data, and serves it to strategies in real time or historical mode.

✔️ Execution & simulation layers

Supports live trading via broker APIs and paper/simulated trading for strategy development safely.

✔️ Back-testing & evaluation

Built-in evaluation pipeline provides metrics (Sharpe ratio, drawdown, win-rate, etc.), logs strategy decisions, and produces performance reports.

✔️ Flexible architecture

Designed for experimentation: plug-and-play strategy modules, custom data connectors, swap frameworks (RL, classical ML, rule-based).



## Scheduling / Cron

Use a scheduler (cron, Airflow, Prefect) to run agent periodically (e.g., at market open/close) or monitor live continuously.

## Logging & Monitoring

Use structured logging (JSON) and monitoring dashboards to track trades, P&L, latency, errors, and system health.

## 💡 Future Roadmap

Integrate Reinforcement Learning agent (RL) for strategy generation

Add portfolio optimization & multi-asset support

Real-time streaming data support (WebSocket / Tick data)

Add “agent explainability” module (why the bot made a trade)

Deploy as service with REST API + dashboard UI


