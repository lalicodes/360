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
| Streaming        | Apache Kafka Streams + Flink for inline fraud rules and stream intelligence |
| Analytics        | Snowflake for transaction warehousing and dashboard queries          |
| Security         | OAuth2, JWT, TLS, Vault, Keycloak, mTLS via Istio                    |
| Monitoring       | Prometheus, Grafana, Jaeger, ELK, OpenTelemetry                      |
| DevOps           | Docker, Kubernetes, Terraform, Pulumi, GitHub Actions, ArgoCD        |

---

## How It Works – System Workflow

1. **Transaction Input** → `$6,500` in `Spain`, `3:14 AM` sent to Go backend  
2. **Double-entry Ledger** → Debit + Credit → Apache Kafka topic `transaction_topic`  
3. **Fraud Detection** → XGBoost score `0.92` → SHAP explains anomaly  
4. **Streaming Rules** → Apache Kafka Streams detect late-night high-value anomalies  
5. **Policy Check** → OPA + Rego block transaction based on user trust level  
6. **GPT-4 Audit** →  
   > _"Flagged for $6,500 at 3:14 AM in a never-before-used country."_  
7. **Vector DB Memory** → GPT summaries embedded in Pinecone for semantic retrieval  
8. **Admin Dashboard** → Risk score: 87%, Geo heatmaps, exportable logs  
9. **Finance Assistant & Chatbot** →  
   - “Was my card used in Canada?” → GPT answers  
   - “How to save?” → GPT: “Dining is 35% of budget. Target: $150/week.”  
10. **Security Flow** →  
    - Auth via **OAuth2 + JWT**  
    - Secrets managed in **HashiCorp Vault**  
    - **TLS/mTLS** across all backend traffic via **Istio**  
    - Identity and access handled via **Keycloak + OpenFGA**  
11. **Monitoring** → Prometheus/Grafana metrics, Jaeger tracing, ELK logs  
12. **CI/CD** → GitHub Actions triggers ArgoCD auto-deploy to Kubernetes

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
  <img src="https://img.shields.io/badge/Stream%20Processing-Flink-orange?style=for-the-badge&logo=apacheflink" />
  <img src="https://img.shields.io/badge/Messaging-RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq" />
  <img src="https://img.shields.io/badge/Secrets-Vault-yellow?style=for-the-badge&logo=hashicorp" />
</p>

<p align="center"><strong> Frontend & UX</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react" />
  <img src="https://img.shields.io/badge/UI-Tailwind%20CSS-38B2AC?style=for-the-badge&logo=tailwindcss" />
  <img src="https://img.shields.io/badge/Charts-Chart.js-F5788D?style=for-the-badge&logo=chartdotjs" />
  <img src="https://img.shields.io/badge/DataViz-D3.js-F9A03C?style=for-the-badge&logo=d3dotjs" />
  <img src="https://img.shields.io/badge/Chatbot-Dialogflow-orange?style=for-the-badge&logo=dialogflow" />
</p>

<p align="center"><strong> Observability & Security</strong></p>
<p align="center">
  <img src="https://img.shields.io/badge/Metrics-Prometheus-orange?style=for-the-badge&logo=prometheus" />
  <img src="https://img.shields.io/badge/Dashboard-Grafana-F46800?style=for-the-badge&logo=grafana" />
  <img src="https://img.shields.io/badge/Tracing-Jaeger-FFCC00?style=for-the-badge&logo=jaeger" />
  <img src="https://img.shields.io/badge/Logs-ELK%20Stack-005571?style=for-the-badge&logo=elasticsearch" />
  <img src="https://img.shields.io/badge/Telemetry-OpenTelemetry-755EBE?style=for-the-badge&logo=opentelemetry" />
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

## ⚙️ Execution Phases

1. **Local Setup**: Docker Compose (Apache Kafka, PostgreSQL, backend)  
2. **Transaction Engine**: Ledger, FX, Kafka events  
3. **Fraud Pipeline**: Kafka → Python → SHAP  
4. **Streaming Rules**: Apache Kafka Streams + Flink logic  
5. **Audit Generation**: GPT-4 fraud summaries + red teaming  
6. **Policy Enforcement**: OPA + Rego + OpenFGA  
7. **Vector Memory**: LangChain + Pinecone for semantic search  
8. **Analytics**: Snowflake queries + dashboards  
9. **Finance Assistant & Chatbot**: GPT-4 guidance  
10. **Security**: OAuth2, Vault, TLS/mTLS, Keycloak, Istio  
11. **Monitoring**: Prometheus, Grafana, ELK, Jaeger  
12. **CI/CD**: GitHub Actions + ArgoCD deployment

---

## 👤 Author

**Lali Krishnan**  
🔗 [github.com/lalicodes](https://github.com/lalicodes)

---

## 📄 License

MIT License. Educational simulation only. All data is fake.

---

> **360 is not just a demo — it’s a full simulation of enterprise banking intelligence.**
