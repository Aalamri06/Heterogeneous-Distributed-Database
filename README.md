#  Distributed Database Management System (DDBMS)

A robust, highly available, and heterogeneous distributed database management system engineered from the ground up to demonstrate modern distributed systems paradigms. The architecture combines a high-performance orchestration layer with polyglot worker nodes to achieve real-time schema virtualization, distributed query parallelization, and remote node management.

---

## 🚀 Key Architectural Paradigms Demonstrated

- **Heterogeneous Node Orchestration:** Seamlessly coordinates services written in strongly-typed compiled languages (**Go**) and dynamically-typed interpreted languages (**Python**) over standard network protocols.
- **Dynamic Schema Virtualization:** Eliminates rigid migration pipelines by evaluating raw database schemas at runtime and broadcasting auto-generation payloads across isolated cluster nodes.
- **Distributed Query Aggregation (MapReduce):** Implements a decentralized map-reduce engine that distributes workload scanning tasks to individual worker nodes before shuffling and reducing datasets at the gateway level.
- **Resilient Heartbeat & Health Monitoring:** Utilizes an asynchronous polling infrastructure to track data replica health, network partitions, and cluster state changes in real time.
- **Asynchronous Write-Through Cache Ingestion:** Lowers network I/O latency barriers by accepting fast volatile data buffering while strictly guaranteeing data persistence via atomic pipeline flushing.

---

## 🗺️ System Topology & Component Deep-Dive

### 1. Central Coordinator / Master Node (Go)
The Master Node functions as the cluster's intelligent central nervous system and API Gateway. It is responsible for intercepting client requests, determining data placement strategies, handling transaction parsing, and coordinating cross-node synchronization.
- **State Engine:** Parses structural JSON definitions and automatically builds abstract query definitions.
- **Replication Manager:** Ensures absolute cluster data consistency by routing data payloads to multiple database endpoints concurrently.
- **Tech Stack:** Golang, `net/http` routing fabric, `database/sql` driver abstraction.

---

### 2. Replica Node 1 (Go Backend)
A low-latency worker node designed to execute data-intensive storage operations and local system configurations.
- **Auto-Schema Generation:** Intercepts incoming writes and dynamically invokes `CREATE TABLE IF NOT EXISTS` routines if a target relation is missing from the local catalog.
- **Kernel-Level Integration:** Exposes low-level interfaces to interact directly with the local operating system shell environment safely via managed sub-processes.
- **Tech Stack:** Golang, SQLite Embedded Storage Architecture, Cross-Origin Resource Sharing (CORS) security handlers.

---

### 3. Replica Node 2 (Python Flask Backend)
A modular pythonic microservice designed to showcase polyglot interoperability inside a modern distributed cluster environment.
- **Data Isolation:** Operates an independent storage partition, isolating processing faults from Replica Node 1.
- **Runtime Environment:** Leverages native runtime hooks to execute operating system automation scripts triggered by the central coordinator.
- **Tech Stack:** Python, Flask Engine, Werkzeug WSGI server, Flask-CORS, Windows Native Shell abstractions.

---

### 4. Enterprise Cluster Dashboard & Web GUI
A unified control center giving system administrators full visibility into cluster operations, partition structures, and automated metrics tracking.
- **Automated Heartbeats:** Utilizes non-blocking asynchronous JavaScript threads to ping nodes every **3 seconds**, altering cluster layout charts visually without requiring full-page browser updates.
- **Dynamic Structural Rendering:** Reads generic server responses and compiles tabular relational representations of distributed records on-the-fly.
- **Tech Stack:** HTML5, CSS3, Modern ES6+ JavaScript (Async/Await Fetch Architecture), Bootstrap Grid System.

---

## 🛠️ Advanced Technical Capabilities

### 🔍 Distributed MapReduce Engine
Traditional single-node queries suffer from hardware ceilings when reading massive datasets. This project addresses this bottleneck via a custom MapReduce data processing pipeline:
- **The Map Phase:** The coordinator dispatches parallel non-blocking scanning orders to all active replica ports. Each worker processes its localized SQLite segment independently, selecting records and formatting data.
- **The Shuffle & Reduce Phase:** The workers return independent data arrays to the coordinator. The Master Node then cleanses, deduplicates, flattens, and shuffles the records into a single coherent, unified global view returned seamlessly to the UI.

### 💾 Write-Through Cache Ingestion Layer
To shield physical hard drive structures from volatile traffic spikes, an optimized ingestion wrapper was added:
- Payloads hit an ultra-fast, volatile internal memory buffer first (**The Cache Layer**), returning a near-instant success flag to the client application.
- The system immediately triggers a **Write-Through Flush**, streaming the transaction records down to the persistent storage structures on the worker disks. 
- Once data integrity is securely confirmed on the storage layers, the temporary volatile buffers are automatically purged to prevent stale memory leaks.

### 🖥️ Remote Kernel & Environment Orchestration
This system includes explicit structural hooks to monitor and control the host servers' actual physical infrastructure directly through network requests:
- **Remote OS Power Control:** Dispatches hardware-level power triggers (`shutdown /s /t 1`) straight into the worker node's operating system environment. The instant the process terminates, the frontend monitoring fabric registers the node failure and flips its status container to **OFFLINE** within 3 seconds.
- **Active Environment Re-Rendering:** Passes image path structures via query parameters to dynamic PowerShell system engines. This programmatically manipulates active operating system registry keys to forcefully refresh user desktop wallpapers on the target node machine remotely.

---

## 📂 Project Structural Tree

```text
DDB-Project/
│
├── master-node/           # Central Coordinating Routing Engine
│   ├── main.go            # Entry point for the master API fabric
│   ├── database.go        # Schema tracking logic
│   ├── replication.go     # Cross-node transactional broadcast mechanics
│   ├── monitor.go         # Worker heartbeat orchestration
│   ├── health.go          # Node status parsing
│   ├── handlers.go        # Client request endpoint controllers
│   ├── master.db          # Metadata catalog storage
│   └── go.mod
│
├── worker-node-1/         # High-Performance Compiled Worker (Go)
│   ├── main.go            # Engine initialization
│   ├── database.go        # Isolated local SQLite state controller
│   ├── handlers.go        # Execution handlers for storage & kernel hooks
│   └── go.mod
│
├── worker-node-2/         # Heterogeneous Interpreted Worker (Python)
│   ├── app.py             # Flask engine configuration & API endpoints
│   ├── database.py        # Independent storage layout management
│   └── requirements.txt   # Microservice dependencies
│
├── GUI/                   # Dashboard Server Node
│   ├── main.go            # Frontend presentation server
│   ├── templates/
│   │   └── index.html     # High-fidelity dashboard application layer
│   └── go.mod
│
└── README.md              # Documentation Asset
