<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?font=Inter&size=22&duration=2000&pause=1000&color=ADD8E6&center=true&vCenter=true&width=600&lines=360+Financial+Intelligence+System;AI-Powered+Fraud+Detection;Enterprise+Banking+Simulation" alt="Typing SVG" />
</p>

# 360: AI-Powered Fraud Detection & Financial Intelligence Platform

360 is an enterprise-grade simulation of a modern banking system, the real-time architecture of FinTechs. It features full-stack transaction processing, real-time AI fraud detection, explainable audit reports via GPT-4, policy enforcement with Open Policy Agent, and a user-centric dashboard complete with an AI-driven chatbot and personal finance assistant.

---

## Project Objective


- Replicate real-world financial transaction systems with secure, intelligent components  
- Showcase enterprise tooling (Kafka, K8s, Prometheus, GPT, OPA) in a real use-case  
- Provide a flagship project for candidates applying to big tech and fintech roles  

---

## Core Features

| Category         | Feature                                                              |
|------------------|----------------------------------------------------------------------|
| Transactions     | Simulated card payments with double-entry ledger                     |
| AI/ML            | Fraud detection using XGBoost + SHAP explanation                     |
| GPT-4            | Summarized audit narratives, risk profiles, and red team test cases  |
| Policy           | AML/KYC/compliance enforcement with OPA and Rego                     |
| User Interaction | Smart banking chatbot with Dialogflow + GPT-4 fallback               |
| Finance UX       | AI personal assistant for budgets, spending insights, savings goals  |
| Security         | OAuth2, JWT, Vault, TLS for end-to-end encryption and secrets        |
| Monitoring       | Prometheus, Grafana, Jaeger, ELK for full observability              |
| DevOps           | Docker, Kubernetes, Terraform, GitHub Actions, ArgoCD (optional)     |

---

## How It Works – Full System Workflow
<p align="center">
  <img src="https://img.shields.io/badge/Status-Simulation--Ready-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Backed%20By-GPT--4-9cf?style=for-the-badge&logo=openai" />
  <img src="https://img.shields.io/badge/Streaming-Kafka-red?style=for-the-badge&logo=apachekafka" />
  <img src="https://img.shields.io/badge/Deployment-Kubernetes-326CE5?style=for-the-badge&logo=kubernetes" />
</p>
### 1. Transaction Input
- User enters dummy card info via frontend (card number, amount, receiver)
- Frontend sends request to Go backend: `/api/transactions`

### 2. Transaction Recording
- Backend maps card → user
- Checks internal balance (PostgreSQL)
- Records debit + credit entries (double-entry ledger)
- Saves transaction row
- Publishes event to Kafka: `transaction_topic`

### 3. Fraud Detection + Scoring
- Python service subscribes to `transaction_topic`
- Predicts fraud score via XGBoost model
- Generates SHAP explanation (e.g. unusual location, large amount, past behavior)
- Flags txns with score > 0.85, saves to `fraud_flags`
- Publishes event to `fraud_flagged_topic`

### 4. OPA Compliance Enforcement
- Policy engine receives transaction payload
- Applies Rego rules: geo-blocks, limits, KYC check
- If violation: txn is rejected + saved in `policy_violations`

### 5. GPT-4 Audit Generation
- GPT receives SHAP + fraud context + policy info
- Generates natural language explanation  
  _Example:_  
  > "This transaction was flagged for $6,500 at 3 AM in a country not previously visited by the user."
- GPT module generates:
  - Audit logs (stored)
  - Risk profile summaries (per user)
  - Red-team adversarial test cases

### 6. Dashboard Visualization (Admin Panel)
- Frontend fetches:
  - Transaction history
  - Live fraud flags
  - GPT summaries
  - Compliance violations
- Displays:
  - Risk dashboards
  - User risk scores
  - Interactive visualizations (Chart.js, D3)
  - Exportable logs (PDF/CSV)

### 7. AI Personal Finance Assistant
- Tracks categories: food, travel, entertainment, savings
- GPT-4 gives:
  - Budget tips
  - Expense insights
  - Smart savings goals

### 💬 8. Banking Chatbot (Dialogflow + GPT-4)
- Users can ask:
  - “What’s my current balance?”
  - “Was my card used in Canada?”
  - “How can I improve savings?”
- If unsupported, fallback to GPT-4

### 9. Security Layer
- JWT-authenticated API calls
- Keycloak for SSO + admin roles
- Vault manages secrets (OpenAI, DB, TLS keys)
- TLS encryption across backend services

### 10. Observability Stack
- Prometheus: collects metrics (txns/min, fraud rate, GPT latency)
- Grafana: dashboards (fraud spike, top users, performance)
- Jaeger: full trace of request from API → Fraud → GPT → DB
- ELK (Kibana): search logs per user, txn ID, or fraud type

### 11. Infrastructure & CI/CD
- Docker containers per service
- Kubernetes orchestrates scaling, health, restarts
- GitHub Actions auto-build and deploy branches
- ArgoCD (optional): GitOps-based continuous delivery
- Terraform or Pulumi: Cloud setup (DB, cluster, secrets)

---

## Folder Structure

```
/360
├── api/                 # Go services (transaction, policy)
├── fraud/               # Python model: XGBoost + SHAP
├── gpt/                 # GPT integration microservice
├── policy/              # OPA engine and Rego rules
├── dashboard/           # React admin dashboard
├── chatbot/             # Dialogflow or GPT integration
├── finance-assistant/   # Budget logic + GPT reports
├── infra/               # Terraform, K8s configs, secrets
├── monitoring/          # Prometheus, Grafana, Jaeger setup
└── README.md
```


---

## Execution Phases

1. **Local Setup**: Docker Compose for DB, Kafka, Go, GPT  
2. **Transaction API + Ledger**  
3. **Kafka Streaming Layer**  
4. **Fraud Engine + SHAP**  
5. **Policy Enforcement with OPA**  
6. **GPT-4 Summarization & Risk Profiling**  
7. **Dashboard + Charts + Exports**  
8. **Chatbot + NLP Setup**  
9. **Finance Assistant + Smart Alerts**  
10. **Observability: Prometheus, Grafana, Jaeger, ELK**  
11. **Security: OAuth2, Vault, TLS**  
12. **Kubernetes + GitHub Actions Deployment**

---

## Author

**Lali Krishnan**  
Email: [lalikrishnanhere@gmail.com](mailto:lalikrishnanhere@gmail.com)  
GitHub: [github.com/lalicodes](https://github.com/lalicodes)

---

## 📄 License

MIT License. This is an educational simulation project. All data is fake and used for demo purposes only.

---

> 360 gives you a complete simulation of how world-class financial systems work: streaming, compliance, AI audits, and real-time insights — ideal for aspiring engineers targeting fintech, big tech, and enterprise platforms.

