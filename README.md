# Flow_Forge

**Flow_Forge** is a modular workflow automation platform that connects webhooks, Solana blockchain events, and microservices — enabling real-time task execution across multiple systems.

This project explores building a **Zapier-like** architecture with production-grade practices such as event streaming and service isolation.

---

## Key Features

- **Custom Workflow Execution**  
  Trigger actions like sending emails, hitting APIs, or recording blockchain events.

- **Modular Architecture**  
  Each service is independently deployable and communicates via Kafka topics.

- **Solana Blockchain Integration**  
  Automate flows based on on-chain activity using Web3.js.

- **Scalable Messaging Layer**  
  Apache Kafka enables high-throughput, asynchronous task distribution.

- **Type-safe Schema & Data Access**  
  All services use PostgreSQL with Prisma for consistent schema enforcement.

---

## Technical Architecture

| Component      | Technology                                   |
| -------------- | -------------------------------------------- |
| **Frontend**   | Next.js + TypeScript + TailwindCSS           |
| **Backend**    | Node.js + Express (hooks, processor, worker) |
| **Database**   | PostgreSQL + Prisma ORM                      |
| **Messaging**  | Apache Kafka                                 |

---

## System Breakdown

- **Frontend (Dashboard)**  
  Interface to define workflows and manage pipeline execution.

- **Hooks Service**  
  Listens for incoming webhook events and queues them via Kafka.

- **Processor Service**  
  Decides which workflows to execute based on the event and rules.

- **Worker Service**  
  Executes actions like sending emails, updating databases, or interacting with Solana.


---

## Design Goals

- **Asynchronous by design** using Kafka queues
- **Service modularity** for scalability and team collaboration
- **Type-safe across stack** using Prisma + TypeScript
- **Secure trigger mechanisms** via token-protected webhooks


---

## Visual Overview

![Flow_Forge System Design](/frontend/public/flow.png)

_(Architecture event flow from webhooks to DB → Outbox → Worker → Kafka → Processor → (Email / Slack / Blockchain).)_

---

## Why I Built This

I wanted to learn how real-time automation tools like Zapier or n8n work under the hood.  
This project gave me hands-on experience with:

- Building **Kafka-powered** asynchronous systems
- Handling **cross-service communication and scaling**
- Working with **modular backend services** using Node.js + Prisma

---

## Related Skills

- Distributed Systems
- Message Queues (Kafka)
- Backend API Design
- Event-driven Microservices
- Database Design with Prisma + PostgreSQL

---

## Let's Connect

If you're curious about how this works or want to collaborate on similar ideas, feel free to reach out!
