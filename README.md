# Micro_go

A high-performance, concurrent microservices architecture built with **Go**, leveraging **gRPC** for internal service-to-service communication and **GraphQL** as the unified API gateway layer for clients.

---

## 🚀 Architecture Overview

This project demonstrates a production-grade blueprint for modern distributed systems. By decoupling the client-facing API from internal logic, it achieves massive scalability and low-latency processing.

*   **API Gateway (GraphQL):** Serves as the single entry point for clients, offering flexible, strongly-typed queries and mutations while aggregating data from backend services.
*   **Internal Communication (gRPC & Protocol Buffers):** Low-overhead, multiplexed HTTP/2 streams connecting internal microservices for ultra-fast communication.
*   **Service Isolation:** Each microservice operates within its own bounded context, maintaining high cohesion and loose coupling.

---

## 🛠️ Tech Stack & Core Libraries

*   **Language:** Go (Golang)
*   **API Layer:** GraphQL
*   **RPC Framework:** gRPC / Protocol Buffers (`protobuf`)
*   **Transport Protocol:** HTTP/2 (gRPC internal), HTTP/1.1 (GraphQL external)

---

## 📦 Project Structure

```text
.
├── gateway/        # GraphQL API Gateway (translates GraphQL requests to gRPC)
├── services/       # Independent backend microservices
│   ├── service_a/  # Microservice A business logic & gRPC server
│   └── service_b/  # Microservice B business logic & gRPC server
└── proto/          # Protocol Buffer definitions (.proto files) and generated Go code
