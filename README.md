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

**[CourseLens](https://github.com/Tanmay-Singh-24/courselens)** `Python · LangGraph · Groq · ChromaDB · Streamlit`
- Built a multimodal, agentic RAG study tool that ingests lecture audio (Whisper transcription), YouTube videos, and slide PDFs — including extracted figures — into a unified ChromaDB vector store for cross-source question answering.
- Every answer carries deep-linked citations: audio players seek to the cited timestamp, YouTube links open at the exact moment, and cited slide figures render inline — making claims verifiable at the source.
- Implemented a LangGraph corrective-RAG pipeline where a grader node validates retrieved evidence before generation, enforcing deterministic refusal on off-corpus questions with bounded retries instead of hallucinated answers.
- Backed quality with an automated eval harness (gold question set scoring answer accuracy and refusal correctness), latency/token instrumentation across the pipeline, and a concept-graph "Course Map" that visualizes how topics across sources relate.

**[Concurrent Seat Reservation System](https://github.com/Tanmay-Singh-24/concurrent-seat-reservation)** `C++17 · POSIX (Shared Memory, Semaphores)`
- Built a multi-process seat-booking system on POSIX shared memory (shm_open/mmap) and a named semaphore, with booking agents spawned as real OS processes via fork — synchronization across process boundaries, where std::mutex and std::atomic don't reach by default.
- Demonstrated the lost-update race, then eliminated it: the same seeded workload runs with and without the lock, and a built-in consistency audit turns "no seat is ever double-booked" into an invariant checked by exit code.
- Validated under a 1.2M-request stress suite (15 seeded runs × 16 agents × 5,000 requests) with zero inconsistencies at ~545K guarded operations/second.
- Engineered for crash safety: an unlink-early IPC design that cannot leak kernel objects, surviving kill -9 of any agent — even inside the critical section — with a clean, audited shutdown instead of a system-wide hang.

**[Order Management System](https://github.com/Tanmay-Singh-24/order-management-system)** `C++ · MySQL (InnoDB) · MySQL Connector/C++`
- Designed a normalized 3NF relational schema for customers, products, orders, and order_items using surrogate primary keys and foreign-key constraints with explicit ON DELETE rules (CASCADE/RESTRICT) to enforce referential integrity and eliminate update anomalies.
- Implemented atomic order placement using MySQL transactions (commit/rollback), ensuring all-or-nothing execution across order creation and stock updates and preventing partial or inconsistent order states under failure conditions such as insufficient inventory.
- Built a C++ data-access layer using parameterized queries (prepared statements) to eliminate SQL injection risk, with RAII-based connection management ensuring deterministic cleanup of database resources.
- Strengthened correctness with DECIMAL-based monetary storage to avoid floating-point errors, a CHECK (stock >= 0) constraint as a database-level safety net backing the application's stock check, and automated end-to-end testing validating commit and rollback behavior under success and failure scenarios.

---

![3D Contrib](./profile-3d-contrib/profile-night-rainbow.svg)
