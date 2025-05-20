<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?font=Inter&size=22&duration=2000&pause=1000&color=ADD8E6&center=true&vCenter=true&width=600&lines=360+Financial+Intelligence+System;AI-Powered+Fraud+Detection;Enterprise+Banking+Simulation" alt="Typing SVG" />
</p>

# 360: AI-Powered Fraud Detection & Financial Intelligence Platform

**360** is an enterprise-grade simulation of a modern banking system, reflecting the real-time architecture of FinTechs. It features full-stack transaction processing, real-time AI fraud detection, explainable audit reports via GPT-4, policy enforcement with Open Policy Agent, and a user-centric dashboard complete with an AI-driven chatbot, personal finance assistant, and intelligent fraud memory search via vector embeddings.

---

## Project Objective

- Simulate secure, intelligent financial transaction systems  
- Demonstrate enterprise-grade tools (Apache Kafka, K8s, GPT, OPA, Istio, Snowflake)  
- Provide a flagship project for candidates applying to fintech and backend roles  

---

## Core Features

| Category         | Feature                                                              |
|------------------|----------------------------------------------------------------------|
| Transactions     | Simulated card payments with double-entry ledger                     |
| AI/ML            | Real-time fraud detection using XGBoost + SHAP                       |
| GPT-4            | Risk summaries, red team test generation, and finance advice         |
| Policy           | AML/KYC/compliance enforcement with OPA, Rego, and OpenFGA           |
| Vector DB        | Pinecone + LangChain for fraud memory and semantic search            |
| User Interaction | Dialogflow chatbot + GPT fallback for smart Q&A                      |
| Finance UX       | GPT-powered budgeting, savings assistant, and semantic tips          |
| Streaming        | Apache Kafka Streams for inline fraud rules and stream intelligence |
| Analytics        | Snowflake for transaction warehousing and dashboard queries          |
| Security         | OAuth2, JWT, TLS, Vault, Keycloak, mTLS via Istio                    |
| Monitoring       | Prometheus, Grafana, Jaeger, ELK, OpenTelemetry                      |
| DevOps           | Docker, Kubernetes, Terraform, Pulumi, GitHub Actions, ArgoCD        |

---

## ⚙️ How It Works – System Workflow

---

### 1. **Transaction Input**
> User initiates a card payment of **$6,500**, location: **Spain**, time: **3:14 AM**

- Data is sent to the **Go-based backend API**
- Contains amount, timestamp, user metadata, and location
- Simulates real-world payment requests in high-risk scenarios (e.g., late hours, foreign country)

---

### 2. **Double-entry Ledger**
> Ensures all transactions are recorded with both debit and credit for financial integrity.

- A ledger entry is created using **accounting principles** (e.g., debit user, credit merchant)
- Event is **published to Apache Kafka** → Topic: `transaction_topic`
- Enables **event-driven streaming** for downstream fraud analysis and policy checks

---

### 3. **Fraud Detection**
> Machine Learning kicks in with real-time risk scoring.

- Message from Kafka is consumed by a **Python-based fraud engine**
- **XGBoost model** returns a score (e.g., `0.92` → high risk)
- **SHAP explainability** outputs the factors:
  - ⏰ Unusual time
  - 🌍 Foreign location
  - 💸 Large amount

---

### 4. **Streaming Rules (Kafka Streams)**
> Detect fraud patterns on the fly, even before ML completes.

- **Apache Kafka Streams** processes event data in real time
- Inline logic flags:
  - High-value transactions at night
  - Unusual spending patterns
- Enables **early-stage filtering and alerting**

---

### 5. **Policy Check (OPA + Rego + OpenFGA)**
> Enforces compliance and access control.

- **OPA + Rego** evaluates KYC, AML, and business rules
- Example rule: Block unverified users spending abroad
- **OpenFGA** ensures only authorized users can override, view, or intervene

---

### 6. **GPT-4 Audit Summary**
> Converts raw ML and rule outputs into human-readable explanations.

```
"Flagged for $6,500 at 3:14 AM in a never-before-used country."
```

- GPT-4 summarizes flagged events in natural language
- Also supports **red team test simulations** for security audits

---

### 7. **Vector Memory (Pinecone + LangChain)**
> Enables search and recall of similar fraud cases via vector embeddings.

- GPT audit outputs and metadata are **embedded and stored in Pinecone**
- **LangChain** powers semantic retrieval and memory
  - Example query: “Find transactions similar to the Spain one”
- Supports fraud research, assistant queries, and recommendations

---

### 8. **Admin Dashboard**
> Visual analytics for fraud risk, locations, and actions.

- Built with **React + Tailwind CSS + D3.js**
- Displays:
  - 🟠 Risk score (e.g., 87%)
  - 🗺️ Geo heatmaps for flagged regions
  - 📄 Exportable logs, audit summaries, and risk explanations

---

### 9. 💬 **Finance Assistant & Chatbot**
> GPT-powered interaction for users and admins.

- **Dialogflow chatbot** for banking FAQs
- **GPT-4 fallback** for deeper answers like:
  - “Was my card used in Canada?” → GPT checks vector memory
  - “How can I save money?” → GPT says: “Dining = 35% of budget. Set weekly target: $150.”

---

### 10. **Security Flow**
> End-to-end security for all services and users.

-  **OAuth2 + JWT** for authentication and session management  
-  **HashiCorp Vault** for managing all secrets securely  
-  **TLS/mTLS** across services using **Istio** service mesh  
-  **Keycloak + OpenFGA** for user roles, identity, and policy enforcement

---

### 11. **Monitoring & Observability**
> Tracks metrics, traces, and logs across all microservices.

- 📊 Metrics: **Prometheus + Grafana**
- 📦 Logs: **ELK Stack** (Elasticsearch, Logstash, Kibana)
- 🕵️ Tracing: **Jaeger**
- 📡 Telemetry: **OpenTelemetry**

---

### 12. **CI/CD Automation**
> Continuous delivery from GitHub to Kubernetes.

-  **GitHub Actions** builds Docker containers on push  
-  **ArgoCD** automatically deploys to the Kubernetes cluster  
-  Ensures zero-downtime and infrastructure as code deployment


---

## 📦 Stack Highlights

<p align="center"><strong> Intelligence & Machine Learning</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Backed%20By-GPT--4-black?style=for-the-badge&logo=openai" />
  <img src="https://img.shields.io/badge/Fraud%20Model-XGBoost-success?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Explainability-SHAP-blueviolet?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Feature%20Store-Feast-darkgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Model%20Tracking-MLflow-blue?style=for-the-badge&logo=mlflow" />
  <img src="https://img.shields.io/badge/LangChain-RAG-orange?style=for-the-badge&logo=langchain" />
  <img src="https://img.shields.io/badge/Vector%20DB-Pinecone-04d9ff?style=for-the-badge&logo=pinecone" />
</p>

<p align="center"><strong> Backend & APIs</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/API-Go-00ADD8?style=for-the-badge&logo=go" />
  <img src="https://img.shields.io/badge/FastAPI-Python-3776AB?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/gRPC-Protobuf-5C2D91?style=for-the-badge&logo=protobuf" />
  <img src="https://img.shields.io/badge/OpenAPI-Swagger-brightgreen?style=for-the-badge&logo=swagger" />
  <img src="https://img.shields.io/badge/Policy%20Engine-OPA-4B8BBE?style=for-the-badge&logo=openpolicyagent" />
  <img src="https://img.shields.io/badge/Auth-OpenFGA-0052CC?style=for-the-badge" />
</p>

<p align="center"><strong> Data & Streaming</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Database-PostgreSQL-blue?style=for-the-badge&logo=postgresql" />
  <img src="https://img.shields.io/badge/Cache-Redis-red?style=for-the-badge&logo=redis" />
  <img src="https://img.shields.io/badge/Warehouse-Snowflake-4BACC6?style=for-the-badge&logo=snowflake" />
  <img src="https://img.shields.io/badge/Streaming-Apache%20Kafka-red?style=for-the-badge&logo=apachekafka" />
  <img src="https://img.shields.io/badge/Kafka%20Streams-ksqlDB-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Kafka%20Connect-CDC%20Pipelines-FF9900?style=for-the-badge&logo=apachekafka" />
  <img src="https://img.shields.io/badge/Debezium-Real--time%20DB%20Change%20Capture-darkred?style=for-the-badge&logo=debezium" /
  <img src="https://img.shields.io/badge/Secrets-Vault-yellow?style=for-the-badge&logo=hashicorp" />
</p>

<p align="center"><strong> Frontend & UX</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react" />
  <img src="https://img.shields.io/badge/UI-Tailwind%20CSS-38B2AC?style=for-the-badge&logo=tailwindcss" />
  <img src="https://img.shields.io/badge/Charts-Chart.js-F5788D?style=for-the-badge&logo=chartdotjs" />
  <img src="https://img.shields.io/badge/DataViz-D3.js-F9A03C?style=for-the-badge&logo=d3dotjs" />
</p>

<p align="center"><strong> Messaging & AI Chatbot</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Messaging-Kafka%20Topics-red?style=for-the-badge&logo=apachekafka" />
  <img src="https://img.shields.io/badge/NLP-Dialogflow-orange?style=for-the-badge&logo=dialogflow" />
 <img src="https://img.shields.io/badge/LLM-GPT--4_Fallback-black?style=for-the-badge&logo=chatgpt" />
  <img src="https://img.shields.io/badge/Memory-LangChain%20+%20Pinecone-04d9ff?style=for-the-badge&logo=langchain" />
</p>

<p align="center"><strong> Monitoring & Security</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Metrics-Prometheus-orange?style=for-the-badge&logo=prometheus" />
  <img src="https://img.shields.io/badge/Dashboard-Grafana-F46800?style=for-the-badge&logo=grafana" />
  <img src="https://img.shields.io/badge/Tracing-Jaeger-FFCC00?style=for-the-badge&logo=jaeger" />
  <img src="https://img.shields.io/badge/Logs-ELK%20Stack-005571?style=for-the-badge&logo=elasticsearch" />
  <img src="https://img.shields.io/badge/Service%20Mesh-Istio-blue?style=for-the-badge&logo=istio" />
  <img src="https://img.shields.io/badge/Auth-Keycloak-purple?style=for-the-badge&logo=keycloak" />
</p>

<p align="center"><strong> DevOps & Infra</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Container-Docker-2496ED?style=for-the-badge&logo=docker" />
  <img src="https://img.shields.io/badge/Orchestration-Kubernetes-326CE5?style=for-the-badge&logo=kubernetes" />
  <img src="https://img.shields.io/badge/IaC-Terraform-purple?style=for-the-badge&logo=terraform" />
  <img src="https://img.shields.io/badge/IaC-Pulumi-ED8B00?style=for-the-badge&logo=pulumi" />
  <img src="https://img.shields.io/badge/CI/CD-GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions" />
  <img src="https://img.shields.io/badge/Delivery-ArgoCD-1E6CFF?style=for-the-badge&logo=argo" />
</p>


---

## 📁 Folder Structure

```
/360
├── api/                 # Go services (transactions, policies)
├── fraud/               # XGBoost + SHAP fraud engine
├── gpt/                 # GPT-4 audit generation service
├── vector/              # LangChain + Pinecone setup
├── policy/              # OPA, OpenFGA, Rego rules
├── dashboard/           # React frontend for admin UI
├── chatbot/             # Dialogflow + GPT fallback
├── finance-assistant/   # GPT-based finance advisor
├── stream/              # Kafka Streams + Flink jobs
├── warehouse/           # Snowflake integration setup
├── infra/               # Docker, K8s, Istio, Terraform, Vault
├── monitoring/          # Prometheus, Grafana, Jaeger, ELK
└── README.md
```

---

## Execution Phases

1. **Local Setup**  
   Containerized environment using **Docker Compose** to spin up Kafka, PostgreSQL, and backend microservices for simulation.

2. **Transaction Engine**  
   Simulates card payments using a **double-entry ledger**, **FX conversion**, and streams all events to Kafka topics.

3. **Fraud Pipeline**  
   Consumes Kafka events via a **Python-based engine** with **XGBoost** scoring and **SHAP**-powered explainability.

4. **Streaming Rules**  
   Applies real-time fraud heuristics using **Kafka Streams** for pattern detection and filtering.

5. **Audit Generation**  
   Uses **GPT-4** to convert flagged events into natural language summaries and **red team test cases** for compliance.

6. **Policy Enforcement**  
   Evaluates AML/KYC rules with **OPA (Rego)** and handles authorization with **OpenFGA** for granular access control.

7. **Vector Memory Search**  
   Embeds and indexes audit logs into **Pinecone**, enabling **semantic recall** using **LangChain**.

8. **Analytics Layer**  
   Pipes structured transactions into **Snowflake** for queryable warehousing, dashboard metrics, and trend visualization.

9. **Finance Assistant & Chatbot**  
   Combines **Dialogflow** for quick Q&A with **GPT-4 fallback** for deep analysis, budget advice, and user assistance.

10. **Security Layer**  
    Implements **OAuth2**, **Vault**, **TLS/mTLS**, and **Keycloak** with **Istio** service mesh for end-to-end secure architecture.

11. **Monitoring & Observability**  
    Tracks metrics, logs, and traces via **Prometheus**, **Grafana**, **Jaeger**, **OpenTelemetry**, and the **ELK Stack**.

12. **CI/CD Pipeline**  
    Uses **GitHub Actions** for build/test and **ArgoCD** for GitOps-based deployment to Kubernetes clusters.

---

## 👤 Author

**Lali Krishnan**  
🔗 [github.com/lalicodes](https://github.com/lalicodes)

---

## 📄 License

MIT License. Educational simulation only. All data is fake.

---

> **360 is not just a demo — it’s a full simulation of enterprise banking intelligence.**
