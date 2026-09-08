# Self-Hosted n8n Production Engine

A reliable, 24/7 cloud-hosted **n8n** automation server backed by PostgreSQL and optimized for resource-constrained environments.

## 🚀 Overview

This repository documents and configures the architecture for running a production-grade n8n instance. Rather than relying on local machine execution or unstable free tiers, this setup establishes a persistent workflow orchestration engine capable of handling webhooks, API polling, and heavy multi-step automation pipelines.

## ⚙️ Core Architecture & Tech Stack

* **Workflow Engine:** n8n (Self-hosted)
* **Database:** PostgreSQL (for reliable execution history and credential management)
* **Hosting & Infrastructure:** Render / Docker
* **Optimization:** Memory-capped container parameters to prevent out-of-memory (OOM) crashes under load

## 🛠️ Key Features

* **Persistent Storage:** Uses an external PostgreSQL database instead of SQLite to prevent database locks and data loss during container restarts.
* **Webhook & API Ready:** Instant ingestion endpoints for external webhooks (Telegram bots, CRM events, payment gateways).
* **Environment Isolation:** Uses `.env` configurations to secure API keys, database credentials, and webhook tokens.

## 🚀 Quick Deployment / Local Setup

If you want to spin up this exact n8n infrastructure locally using Docker Compose:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/PabloElch/n8n-self-hosted.git](https://github.com/PabloElch/n8n-self-hosted.git)
   cd n8n-self-hosted

   Configure environment variables:
Create a .env file and set your credentials:

Code snippet
N8N_ENCRYPTION_KEY=your_secure_encryption_key
DB_TYPE=postgresdb
DB_POSTGRESDB_HOST=your_postgres_host
DB_POSTGRESDB_PORT=5432
DB_POSTGRESDB_DATABASE=n8n
DB_POSTGRESDB_USER=your_user
DB_POSTGRESDB_PASSWORD=your_password
Spin up with Docker Compose:

Bash
docker-compose up -d
📄 License
Open-source architecture for robust workflow automation.











   
