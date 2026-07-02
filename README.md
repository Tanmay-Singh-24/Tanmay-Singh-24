# Hi, I'm Tanmay Singh 👋

B.Tech CSE (AIML) · 4th Year · VIT Bhopal

I build projects at the intersection of AI and systems programming — from multi-agent RAG pipelines with LangChain and LangGraph to concurrent systems and relational databases in C++. Currently preparing for campus placements with a focus on AI engineering.

---

### Languages
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

### Agentic AI & RAG
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-111111?style=flat&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)

### Tools & Databases
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat&logo=cmake&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

### Projects

**Order Management System** `C++ · MySQL · MySQL Connector/C++`
- Designed a normalized 3NF relational schema for customers, products, orders, and order_items using surrogate primary keys and foreign-key constraints with explicit ON DELETE rules (CASCADE/RESTRICT) to enforce referential integrity and eliminate update anomalies.
- Implemented atomic order placement using MySQL transactions (commit/rollback), ensuring all-or-nothing execution across order creation and stock updates and preventing partial or inconsistent order states under failure conditions such as insufficient inventory.
- Built a C++ data-access layer using parameterized queries (prepared statements) to eliminate SQL injection risk, with RAII-based connection management ensuring deterministic cleanup of database resources.
- Strengthened correctness guarantees using InnoDB-backed ACID transactions, DECIMAL-based monetary storage to avoid floating-point errors, and automated end-to-end testing validating commit and rollback behavior under success and failure scenarios.

**Concurrent Seat Reservation System** *(in progress)* `C++ · POSIX (Shared Memory, Semaphores)`
- Building a multi-process seat-booking system using POSIX shared memory (mmap) for inter-process communication, with booking agents spawned via fork.
- Eliminating double-booking race conditions by guarding the critical section with semaphores, demonstrating mutual exclusion across concurrent processes.
- Reproducing and resolving a classic race condition (lost-update problem) to demonstrate the need for synchronization on shared state.
- Adding signal handling for clean release of shared-memory and semaphore resources on process termination.

**Multi-Agent RAG Workflow** *(in progress)* `Python · LangChain · LangGraph · ChromaDB · FastAPI · GCP`
- Developing a production RAG-powered document assistant with a multi-agent architecture using LangGraph for stateful, multi-step reasoning workflows.
- Agents communicate through a shared state graph — a retrieval agent fetches relevant chunks from ChromaDB, a grading agent filters low-relevance results, and a generation agent synthesizes the final answer.
- Exposing the pipeline via a FastAPI REST API with automated CI/CD deployment on GCP.

---

![3D Contrib](./profile-3d-contrib/profile-night-rainbow.svg)
