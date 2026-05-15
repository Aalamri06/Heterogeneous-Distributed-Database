# Distributed Database Management System

A professional distributed database management system built using:

- Go (Master Node + Worker Node 1)
- Python Flask (Worker Node 2)
- SQLite & Local Storage Engine (Embedded DB per Node)
- HTML/CSS/JavaScript Web Dashboard & API Gateway
- REST API Architecture
- Dynamic Table Management
- Real-Time Worker Monitoring (Heartbeat System)

---

# Project Overview

This project simulates a real-world enterprise distributed database environment where:

- **A Master Node** acts as the central orchestrator and coordinator.
- **Multiple Heterogeneous Worker Nodes** replicate data, handle sharded queries, and manage local storage.
- **A Professional Web GUI** allows dynamic database operations and real-time visualization of cluster health.
- **Advanced Tasks** are integrated including MapReduce distributed querying, Remote OS orchestration, and Write-Through Caching.

The system demonstrates key distributed systems concepts including:
- Distributed databases & Sharding
- Data Replication & Cross-Node Synchronization
- **MapReduce Pattern Execution**
- **Remote Procedure Calls (RPC) / OS Virtualization Control**
- Heterogeneous Multi-node architecture (Go + Python)
- **Write-Through Cache Layer Ingestion**
- Real-time automated Heartbeat monitoring

---

# System Architecture

## Components

### 1. Master Node (Go)
**Responsibilities:**
- Central gateway coordinator.
- Evaluates incoming schemas and routes dynamic CRUD requests.
- Coordinates replication protocols across the active cluster.
- Implements Write-Through Cache validation.

**Technologies:** Golang, net/http, database/sql.

---

### 2. Worker Node 1 (Go)
**Responsibilities:**
- High-performance replica node.
- Implements auto-schema generation (`CREATE TABLE IF NOT EXISTS`) upon payload replication.
- Executes local OS tasks (Remote shutdown, Wallpaper rendering using localized PowerShell wrappers).
- Responds to distributed sub-queries (Map Phase).

**Technologies:** Golang, SQLite Driver, Cross-Origin Resource Sharing (CORS) Middleware.

---

### 3. Worker Node 2 (Python Flask)
**Responsibilities:**
- Secondary replica worker node.
- Simulates a heterogeneous distributed environment ecosystem.
- Exposes native operational hooks for internal system monitoring.
- Manages local SQLite isolated state storage.

**Technologies:** Python, Flask, Flask-CORS, Windows OS Shell utilities.

---

### 4. Professional Web Dashboard (API Gateway Browser)
**Responsibilities:**
- Real-time Node status validation (Automated AJAX Heartbeats running every 3 seconds).
- Interface layout for Remote OS execution.
- Dynamic layout generator for tabular MapReduce results.

**Technologies:** HTML5, CSS3, JavaScript (Async/Await Fetch API), Bootstrap.

---

# Key Features & Added Tasks

## 1. Dynamic Auto-Schema Generation & CRUD
- **Create Dynamic Table:** Emits asynchronous table schema schemas over the system cluster.
- **Dynamic Insert/Update/Delete:** Automatically inspects structures to generate forms, performing data conversion on-the-fly and safely updating target database segments via ID.

## 2. Task 1: Remote OS Control & Orchestration
The client can target any specific backend machine directly through the central interface to perform kernel-level actions:
- **Remote OS Shutdown:** Executes immediate shell termination commands (`shutdown /s /t 1`), switching the live UI status container to **OFFLINE** within 3 seconds.
- **Remote Wallpaper Changer:** Injectively triggers Windows PowerShell environment actions to forcefully refresh and update the target machine's active Desktop Wallpaper layout using image path structures.

## 3. Task 2: Distributed MapReduce Querying
Instead of traditional localized database reads, the system aggregates cross-node chunks using a MapReduce sequence:
- **Map Phase:** Parallel HTTP triggers dispatch requests to worker nodes. Workers extract, clean, and map local structural database tables.
- **Reduce Phase:** The controller framework captures partial node arrays, shuffles records, and aggregates them into a single consolidated, deduplicated layout inside the Web Viewer.

## 4. Bonus Task: Write-Through Cache Ingestion
To optimize system I/O latency operations:
- Data payloads route into a memory-buffered **Cache Node** container first.
- The system executes a safe Write-Through operation, syncing the structural state into the persistent **Main Storage/Workers** before clearing volatile temporary state queues, protecting the cluster from unexpected hardware failure data loss.

---

# Folder Structure

```text
DDB-Project/
│
├── master-node/
│   ├── main.go
│   ├── database.go
│   ├── replication.go
│   ├── monitor.go
│   ├── health.go
│   ├── handlers.go
│   ├── master.db
│   └── go.mod
│
├── worker-node-1/ (Go)
│   ├── main.go
│   ├── database.go
│   ├── handlers.go
│   └── go.mod
│
├── worker-node-2/ (Python)
│   ├── app.py
│   ├── database.py
│   └── requirements.txt
│
├── GUI/
│   ├── main.go
│   ├── templates/
│   │   └── index.html
│   └── go.mod
│
└── README.md