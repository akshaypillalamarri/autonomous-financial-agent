# 🐺 Wolfie: Autonomous Financial Intelligence Agent

**Built by Akshay Pillalamarri**

> *An autonomous AI agent that proactively hunts for market alpha, analyzes analyst sentiment, and delivers high-conviction stock reports via Telegram.*

---

## 📖 Project Overview
Wolfie is not a passive chatbot; it is an **active agent** built on the Moltbot runtime. It wakes up daily, connects to the live web via Brave Search, and uses **Google Gemini 2.0 Flash** to perform complex financial analysis.

Unlike standard screeners, Wolfie uses a **Dynamic Hunter Protocol** to identify *new* stock upgrades from major institutional banks (Goldman Sachs, Morgan Stanley) rather than watching a static list.

## 🚀 Key Features
* **Dynamic Asset Discovery:** Automatically identifies "Fresh Kills" (new analyst upgrades) every morning.
* **Real-Time Web Access:** Bypasses LLM knowledge cutoffs using the **Brave Search API** for live market data.
* **Sentiment Analysis:** Correlates specific stock news with the global "Fear & Greed Index."
* **Rate Limit Engineering:** Implements batch-querying logic to maximize API efficiency and prevent `429 Rate Limit` errors on free-tier plans.
* **Secure Architecture:** Runs locally with environment-variable managed credentials (Zero-trust architecture).

## 🛠️ Tech Stack
| Component | Technology Used |
| :--- | :--- |
| **Runtime** | Node.js (Moltbot Framework) |
| **LLM Brain** | Google Gemini 2.0 Flash |
| **Search Tool** | Brave Search API |
| **Interface** | Telegram Bot API |
| **Config** | JSON5 & .env Management |

## ⚙️ How It Works
1.  **Wake Up:** The agent initializes via a local batch script (`WakeWolfie.bat`).
2.  **The Hunt:** It executes a broad search query for *"top stock analyst upgrades major banks today"*.
3.  **The Filter:** It filters out penny stocks and low-conviction plays, isolating top-tier institutional moves.
4.  **The Verdict:** It uses Chain-of-Thought prompting to determine a `BULLISH` or `WAIT` verdict based on the catalyst.
5.  **Delivery:** A structured report is pushed asynchronously to a private Telegram channel.

## 💻 Installation & Setup

```bash
# 1. Clone the repository
git clone [https://github.com/akshaypillalamarri/autonomous-financial-agent.git](https://github.com/akshaypillalamarri/autonomous-financial-agent.git)

# 2. Install dependencies
cd autonomous-financial-agent
pnpm install

# 3. Configure Secrets (Create a .env file)
# Note: You need your own API keys for Gemini, Brave, and Telegram.
# DO NOT commit your keys to GitHub.

```
🧠 Skills Demonstrated
Prompt Engineering: Designed "Wolfie's" persona and strict output protocols to prevent hallucinations.

API Integration: Connected multiple distinct services (Search, LLM, Messaging) into a cohesive pipeline.

System Administration: Managed local runtime environments, CLI tools, and version control.

Financial Logic: Programmed logic to distinguish between noise and significant market catalysts.


Disclaimer: This project is for educational purposes and demonstrates software engineering capabilities. It is not financial advice.
