# 📈 Stock Prediction Model with n8n Integration

## 🧠 1. Introduction

This project integrates a stock price prediction machine learning model with an automated conversational workflow using [n8n](https://n8n.io/). The goal is to make intelligent stock price predictions easily accessible via a chat interface, powered by OpenAI and automated through n8n’s low-code automation platform.

---

## ❓ 2. Why is it needed?

- ✅ **Accessibility**: Most ML models sit isolated in notebooks or dashboards. With this, users can get predictions through a chat.
- 🔁 **Automation**: Combining n8n and Langchain allows continuous interaction and real-time insights without manual intervention.
- 📊 **Usability**: Perfect for financial analysts, trading bots, or data science learners to test live workflows and automation.

---

## 🧰 3. Tech Stack for the ML Model

| Component       | Description                                         |
|----------------|-----------------------------------------------------|
| `Python`       | Primary programming language                        |
| `Pandas`       | Data manipulation and preprocessing                 |
| `Scikit-learn` | Model training, evaluation (Random Forest Regressor)|
| `yfinance`     | Pulling historical stock data                       |
| `Matplotlib`   | For plotting trends and results                     |
| `Jupyter`      | Development environment for prototyping             |

---

## 🔄 4. n8n Workflow Overview

The workflow enables interaction with the ML model via a conversational agent using Langchain + OpenAI:

### 🔧 Nodes Used:

| Node Type                     | Purpose                                       |
|------------------------------|-----------------------------------------------|
| `When Chat Message Received` | Triggers the workflow on new messages         |
| `AI Agent`                   | Central logic processing unit via Langchain   |
| `OpenAI Chat Model`          | GPT model (e.g. GPT-4o-mini) for responses    |
| `Simple Memory`              | Maintains conversational context              |
| `Calculator`                 | Performs computations if needed               |
| `SerpAPI`                    | Fetches external data (stock news/searches)   |

### 🔄 Workflow Flow:

- The AI Agent intelligently routes queries using tools like calculator, search API, and the ML prediction responses.

---

## 🧾 5. Conclusion

This project bridges predictive finance models and real-world usability through automation. By integrating the model with n8n and OpenAI’s conversational interface, we make financial insights accessible, scalable, and ready for production.

---

## 📁 Files Included

- `Stock Prediction Model with n8n.ipynb`: Full Python code and prediction model
- `n8n_workflow.json`: JSON importable into n8n for end-to-end integration

---

> ⚠️ Note: Before running, make sure your n8n instance has access to Langchain, OpenAI, and optional SerpAPI modules with correct credentials.

