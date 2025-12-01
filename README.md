# SmartServe_Multitool_Voice_Agent
Enterprise Support AI Agent – Multi-Agent Workflow with Custom API Tool, Memory, and Observability

# SmartServe Multitool Voice Agent

**Enterprise Support AI Agent – Multi-Agent Workflow with Custom API Tool, Memory & Observability**  

This project is my submission for the **Google x Kaggle 5-Day AI Agents Intensive Capstone Project** under the **Enterprise Agents Track**.  
It demonstrates how AI agents can automate enterprise customer support using a clean multi-agent architecture.

---

## Problem Statement

Enterprises receive thousands of support queries every day: refunds, billing issues, cancellations, product complaints, etc.  
Manual handling increases resolution time, operational cost, and human errors.  

This project automates enterprise customer support using AI agents.

---

## Why Agents?

Agents are the right solution because they can:  
- Classify intents automatically  
- Generate responses dynamically  
- Use custom tools/APIs for fetching order info  
- Maintain conversation context  
- Log activity for observability  

---

## What You Created

The project consists of **four coordinated agents**:  
1. **IntentAgent** – Classifies user messages  
2. **ReplyAgent** – Generates replies  
3. **OrderInfoTool** – Custom API tool for order info  
4. **Memory Agent** – Stores conversation history  
5. **Coordinator** – Orchestrates multi-agent workflow  

Architecture:

User --> Coordinator --> IntentAgent --> Coordinator
Coordinator --> ReplyAgent --> OrderInfoTool --> ReplyAgent
ReplyAgent --> Coordinator --> Memory --> User


---

## Demo

Example interactions:

| User Message | Intent | Urgency | Agent Reply |
|--------------|--------|---------|-------------|
| "I want to cancel my subscription." | cancellation | high | "I can help cancel your subscription. Kindly provide your registered email." |
| "My invoice amount is wrong." | billing | medium | "It seems you have a billing concern. Please send your invoice number." |
| "I need a refund please." | refund | high | "I understand you want a refund. Please share your order ID." |
| "order: 12345" | refund | high | "Order Status: Refund Approved" |

---

## The Build

- **Python 3**  
- Libraries: `numpy`, `pandas`, `matplotlib`  
- Multi-agent architecture with **Coordinator**, **IntentAgent**, **ReplyAgent**, **Memory**  
- Custom tool simulating **API calls**  
- Logging for **observability**  
- Evaluation suite for **automated testing**  

---

## If I Had More Time

- Integrate **real backend API** for order management  
- Add **speech-to-text & text-to-speech** for voice interface  
- Enhance **intent classification** using LLM  
- Add **long-term memory & persistent sessions**  
- Deploy on cloud for **real-time enterprise use**  

---

## How to Run

1. Open the Kaggle notebook or local environment  
2. Run `agent.py` or the notebook cells  
3. Optional: Generate `agent_output.png` using matplotlib for demo visualization  

```bash
python agent.py


