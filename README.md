# 🚢 Popeye — Multi-Container Microservices Deployment with Docker

[![Technology: Docker](https://img.shields.io/badge/Technology-Docker%20%26%20Swarm-2496ED.svg)](https://www.docker.com/)
[![Module: B-DOP-200](https://img.shields.io/badge/Epitech-B--DOP--200-blue.svg)](https://www.epitech.eu/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Epitech: Tek1](https://img.shields.io/badge/Epitech-Tek1-005696.svg)](https://www.epitech.eu/)

> **Popeye is an orchestration project containerizing a distributed voting application**, leveraging Docker Compose and Docker Swarm for service isolation, state persistence, and inter-container networking.

---

## 🏛️ Application Architecture

The system coordinates five microservices:

```text
[Poll Frontend (Python/Flask)]  ──(Redis queue)──►  [Worker (.NET / Java)]
                                                            │
                                                     (Upsert votes)
                                                            ▼
[Result Frontend (Node.js)]     ◄──(Read votes)───  [PostgreSQL DB]
```

### Components:
1. **Poll:** Python Flask web UI where users cast votes.
2. **Redis:** In-memory queue storing raw incoming votes.
3. **Worker:** Background worker polling Redis and committing votes to PostgreSQL.
4. **PostgreSQL:** Persistent relational database holding voter tallies.
5. **Result:** Real-time web application displaying voting results.

---

## 🛠️ Usage

```bash
# Launch with Docker Compose
docker-compose up --build
```

---

## 📜 License

Licensed under the **MIT License with attribution** to Lucas Lhomme (Crabe).
