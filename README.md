# Distributed Database Management System

A professional distributed database management system built using:

- Go (Master Node + Worker Node)
- Python Flask (Secondary Worker Node)
- PostgreSQL
- HTML/CSS/JavaScript Dashboard
- REST API Architecture
- Dynamic Table Management
- Real-Time Worker Monitoring

---

# Project Overview

This project simulates a real-world distributed database environment where:

- A Master Node controls the system.
- Multiple Worker Nodes replicate and manage data.
- A professional Web GUI allows dynamic database operations.
- Worker health monitoring detects online/offline nodes.
- Dynamic CRUD operations support any database schema.

The system demonstrates important distributed systems concepts including:

- Distributed databases
- Replication
- Failover simulation
- Multi-node architecture
- RESTful communication
- Real-time monitoring
- Dynamic schema handling

---

# System Architecture

## Components

### 1. Master Node (Go)

Responsibilities:

- Main coordinator
- Handles CRUD requests
- Replicates data to workers
- Monitors worker status
- Sends API requests to worker nodes
- Central database management

Technologies:

- Golang
- PostgreSQL
- net/http
- database/sql

---

### 2. Worker Node 1 (Go)

Responsibilities:

- Replica node
- Stores replicated data
- Responds to health checks
- Receives replicated queries from master

Technologies:

- Golang
- PostgreSQL
- REST API

---

### 3. Worker Node 2 (Python Flask)

Responsibilities:

- Secondary replica node
- Receives replicated data
- Simulates heterogeneous distributed systems
- Responds to health checks

Technologies:

- Python
- Flask
- PostgreSQL

---

### 4. Professional Web Dashboard

Responsibilities:

- Dynamic CRUD operations
- Real-time monitoring
- Dynamic schema rendering
- User interaction
- Distributed system visualization

Technologies:

- HTML5
- CSS3
- JavaScript
- Bootstrap

---

# Features

## Dynamic Table Creation

Users can dynamically create database tables using custom columns.

Example:

```text
name:TEXT,age:INTEGER,email:TEXT
```

---

## Dynamic Insert

The system automatically loads table columns and generates dynamic forms.

Supports:

- Any table structure
- Automatic input generation
- Numeric conversion
- Dynamic JSON handling

---

## Dynamic Select

Users can:

- View any table
- Load records dynamically
- Render columns automatically
- Display records in responsive tables

---

## Dynamic Update

Supports:

- Updating any row
- Dynamic update forms
- Partial updates
- Generic SQL query building

---

## Dynamic Delete

Supports:

- Row deletion by ID
- Dynamic table selection
- API-based deletion

---

## Real-Time Worker Monitoring

The dashboard checks worker status every 3 seconds.

Features:

- Online/offline detection
- Real-time UI updates
- Automatic health checking
- Worker visualization

---

## Replication

The Master Node replicates operations to:

- Worker Node 1 (Go)
- Worker Node 2 (Python Flask)

This simulates distributed database replication.

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
│   └── go.mod
│   └── health.go
│   └── handelers.go
│   └── master.db
│
├── worker-node-1/
│   ├── main.go
│   ├── database.go
│   ├── handlers.go
│   └── go.mod
│
├── worker-node-2/
│   ├── app.py
│   ├── requirements.txt
│   └── database.py
│
├── GUI/
│   ├── main.go
│   ├── templates/
│   │   └── index.html
│   └── go.mod
│
└── README.md
```

---

# Database Design

## PostgreSQL

The project uses PostgreSQL as the distributed database engine.

### Advantages

- Reliable relational database
- SQL support
- ACID compliance
- Multi-node compatibility
- Production-ready architecture

---

# API Endpoints

## Master Node APIs

| Method | Endpoint      | Description          |
| ------ | ------------- | -------------------- |
| POST   | /create-table | Create dynamic table |
| POST   | /insert       | Insert dynamic data  |
| POST   | /select       | Select table records |
| POST   | /update       | Update record        |
| POST   | /delete       | Delete record        |
| POST   | /columns      | Get dynamic columns  |

---

# Real-Time Monitoring

The GUI continuously checks:

- Worker Node 1 status
- Worker Node 2 status

Monitoring interval:

```text
Every 3 seconds
```

Health checks use:

```http
GET /
```

If a node fails:

- UI changes to OFFLINE
- Red status indicator appears
- System continues running

---

# Distributed Systems Concepts Implemented

## 1. Replication

The master node forwards operations to worker nodes.

---

## 2. Fault Detection

The GUI detects worker failures in real-time.

---

## 3. Multi-Node Architecture

The system contains:

- One master node
- Two worker nodes
- Shared distributed communication

---

## 4. Heterogeneous Distributed Environment

The project combines:

- Go services
- Python Flask services

This simulates enterprise distributed systems.

---

# Technologies Used

| Technology   | Purpose                |
| ------------ | ---------------------- |
| Golang       | Backend services       |
| Python Flask | Secondary worker node  |
| PostgreSQL   | Database engine        |
| HTML/CSS     | Frontend UI            |
| JavaScript   | Dynamic frontend logic |
| Bootstrap    | UI styling             |
| REST APIs    | Communication          |

---

# Screenshots

## Dashboard

- Dynamic CRUD operations
- Worker monitoring
- Responsive design
- Real-time updates

## Dynamic Table Viewer

- Automatically generated columns
- Dynamic rendering
- Responsive tables

---

# How To Run

## 1. Start PostgreSQL

Make sure PostgreSQL is running.

---

## 2. Run Master Node

```bash
go run .
```

Port:

```text
8080
```

---

## 3. Run Worker Node 1

```bash
go run .
```

Port:

```text
8081
```

---

## 4. Run Worker Node 2

```bash
python app.py
```

Port:

```text
8082
```

---

## 5. Run GUI

```bash
go run .
```

Port:

```text
8090
```

---

# Future Improvements

Planned improvements include:

- WebSocket live updates
- Leader election
- Automatic failover
- Docker deployment
- Authentication system
- Role-based access control
- Load balancing
- Sharding
- Kubernetes deployment
- Logging system
- Distributed transactions

---

# Educational Value

This project demonstrates practical implementation of:

- Distributed systems
- Database replication
- Dynamic SQL handling
- Multi-language backend systems
- API communication
- Full-stack development
- Real-time monitoring systems

---

# Author

## Abdullah Aly

Computer Science Student

Distributed Systems & Backend Development Enthusiast

Skills demonstrated:

- Golang
- Python
- PostgreSQL
- REST APIs
- Distributed Databases
- Full Stack Development
- System Architecture

---

# License

This project is developed for educational and professional portfolio purposes.

