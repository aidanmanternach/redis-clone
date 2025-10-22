# Redis Clone (Go Implementation)

A lightweight, educational Redis clone built from scratch in **Go**, inspired by [build-redis-from-scratch.dev](https://www.build-redis-from-scratch.dev/).  
This project explores the internals of how Redis works — including command parsing, TCP networking, and in-memory data storage.

---

## Features

- **RESP Protocol Parsing** — Implements the Redis Serialization Protocol for client-server communication.  
- **Command Execution** — Supports core Redis commands like:
  - `PING`
  - `ECHO`
  - `SET`
  - `GET`
  - `HSET`  
  - `HGET`
- **In-memory Key-Value Store** — Efficient data storage with Go maps.  
- **Concurrent Connections** — Handles multiple clients using Go goroutines.  
- **TCP Server** — Listens on a configurable port and responds like a real Redis instance.  
- **Extensible Command Handlers** — Easily add new commands via a handler map.

---

## Project Structure
redis-clone/  
├── main.go # Entry point for the Redis server  
├── handlers.go # Command handler implementations  
├── resp.go # RESP protocol parsing and encoding  
└── README.md # Project documentation

## Getting Started

### **Prerequisites**
- Go 1.20 or higher
- redis-cli installed

### **Clone the Repository**
```
bash
git clone https://github.com/<your-username>/redis-clone.git
cd redis-clone
```

Run Server
```
go run main.go resp.go handlers.go
```

Connect Using Redis CLI in antoher terminal
```
redis-cli
```

In redis-cli try
```
PING
SET {your_name} Awesome!
GET {your_name}
```

## Learning Goals

This project is for understanding:
 - How Redis handles TCP connections
 - How the RESP protocol encodes/decodes messages
 - How concurrency and shared state work in Go
 - How to structure a networked system from scratch