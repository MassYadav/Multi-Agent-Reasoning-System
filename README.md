# 🚀 Production-Ready Multi-Agent Reasoning System
## Scalable MLOps Implementation for Real-Time AI Simulation

### 💡 Project Overview
This repository contains a **production-focused implementation** of a Multi-Agent Reasoning System designed for scalable deployment. The system simulates historical figures (like Plato and Aristotle) using RAG and **LangGraph**, exposing the agent functionality as a **low-latency, RESTful API with WebSockets**. The implementation heavily focuses on achieving **MLOps maturity, system optimization, and high-availability deployment**.

<p align="center">
    <img src="static/diagrams/system_architecture.png" alt="Architecture Diagram" width="600">
</p>

### 📐 Production Architecture & Technology Stack
The system is engineered for reliability and speed, covering the full LLMOps lifecycle:

* **Agent Orchestration:** **LangGraph** (For complex, stateful multi-agent workflows).
* **API & Real-Time:** **FastAPI** & **WebSockets** (Enabling real-time, low-latency communication).
* **Memory & Database:** **MongoDB** (Unified store for **long-term memory (Vector Store)** and **LangGraph Checkpointing**).
* **LLMOps & Monitoring:** **Opik** (Implemented for prompt monitoring, versioning, and automated agent evaluation).
* **Inference Backend:** Utilized **GroqCloud** for high-speed LLM inference, minimizing latency.
* **Deployment:** **Docker** and **Kubernetes (HPA)** (Ensuring portable deployment and cost-optimized, high-availability scaling).

### 🎯 Key Achievements & Quantified Results
The microservice was rigorously optimized and deployed to validate its production readiness, demonstrating the following metrics:

* **Low-Latency Performance:** Implemented the agent as a RESTful API, optimized for real-time response generation via WebSockets.
* **Quality Metrics:** Achieved the following agent evaluation metrics using the OPik framework:
    * **Answer Relevance:** **0.9**
    * **Context Precision:** **0.65**
* **Scalability:** Deployed the microservice using **Kubernetes Horizontal Pod Autoscaling (HPA)** to ensure resources scale elastically with demand, preventing service disruption during peak load.

### 📂 Project Structure (MLOps Pipeline View)
The repository is intentionally structured to represent a complete MLOps workflow, demonstrating production setup, deployment, and monitoring:

```bash
.
├── 01_Agent_Microservice/   # Core agent logic, RAG pipelines, and core FastAPI service.
├── 02_Frontend_Game_UI/     # Front-end interface for interaction.
├── 03_Kubernetes_GCP/       # K8s Deployment YAMLs, Service, and HPA configuration files.
├── 04_Containerization/     # Dockerfile and environment setup for containerizing the microservice.
├── static/                  # System diagrams and visual assets.
└── README.md