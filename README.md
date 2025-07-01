# TCP Chat Application

This is a simple terminal-based TCP chat application built in C using POSIX socket programming on Linux. The goal was to explore low-level network communication and implement a basic chat system using the client-server model.

---

## 🔧 What It Does

The project allows multiple clients to connect to a central server over TCP and chat with each other in real time. The server listens for incoming connections, handles each client, and broadcasts messages to all connected users.

It's a lightweight, console-based application — no GUI, just the good old terminal doing all the work.

---
 data is sent and received over a network, how to manage multiple connections, and how the client-server model works in real applications.

---

## ⚙️ Technologies Used

- **C (POSIX)**
- **Linux Terminal**
- **TCP Sockets**
  - `socket()`
  - `bind()`
  - `listen()`
  - `accept()`
  - `connect()`
  - `send()`
  - `recv()`
  - `close()`

---

## 🧭 How It Works

### Server
- Binds to a specific port and listens for connections.
- Accepts incoming client connections using `accept()`.
- For every connected client, it waits for messages and forwards them to other clients.

### Client
- Connects to the server using an IP address and port number.
- Sends messages typed by the user.
- Displays messages received from other clients.

---

## 🚀 How to Run It

Make sure you're on a Linux machine with GCC installed.

### 1. Compile the Code

```bash
gcc server.c -o server
gcc client.c -o client
